# projet-TODO-LIST
todo: list = []
# FONCTION 1 : ajoute_tache


def ajoute_tache(todo: list) -> list:
    
	"""
    Demande à l'utilisateur de saisir les informations d'une tâche
    et l'ajoute dans la TODO list.
	:param todo: Le tableau contenant toutes les tâches existantes.
    :type todo: list
    :return: Le tableau mis à jour avec la nouvelle tâche ajoutée.
    :rtype: list
    """


nom: str = input("Entrez le nom de la tâche : ")
date: str = input("Entrez la date d'échéance sous format aaaammjj ")
priorite: int = input("Entrez la priorité de 1 à 5 (5 = très urgent) : ")
nouvelle_tache: dict = {
        "nom": nom,
        "date": date,
        "priorite": priorite,
        "etat": False
    }
todo.append(nouvelle_tache)
print("Tâche", + nom, "ajoutée avec succès !")
return todo

# FONCTION 2: elimine_tache
def elimine_tache(todo: list) -> list:
    
	"""
    Demande à l'utilisateur de saisir le nom d'une tâche
    et la supprime de la TODO list.
	:param todo: Le tableau contenant toutes les tâches.
    :type todo: list
    :return: Le tableau mis à jour sans la tâche supprimée.
    :rtype: list
	"""

nom_a_supprimer: str = input("Entrez le nom de la tâche à supprimer : ")

# on crée un nv tab sans la tache et on garde toute les taches dont le nom est different du nom a supprimer
nouveau_todo: list = []
tache_trouvee: bool = False

# On parcourt chaque tâche du tableau
i: int = 0
    while i < len(todo):
        tache: dict = todo[i]
        # Si le nom de cette tâche est différent du nom à supprimer, on la garde
        if tache["nom"] != nom_a_supprimer:
            nouveau_todo.append(tache)
        else:
            tache_trouvee = True
        i = i + 1

    
# On affiche un message selon si la tâche a été trouvée ou non
if tache_trouvee:
        print("Tâche", nom_a_supprimer, "supprimée avec succès !")
    else:
        print("Aucune tâche avec le nom ", nom_a_supprimer, "n'a été trouvée.")
return nouveau_todo

# FONCTION 3: termine_tache
def termine_tache(todo: list) -> list:
	
	""" 
	demande a l'utilisateur le nom de la tache, pour qu'elle change
	son etat a True (tache terminer).
	:param todo: le tab avec toutes les taches
	:type todo: list
	:return: le tab avec les taches mis a jours (etat = True, pour les taches terminer)
	:rtype: list
	"""
nom_termine: str = input("entrez le nom de la tache a marquer comme terminée :")
tache_trouve: bool = False
# on parcourt chaque tache du tab
i: int = 0
while i < len (todo)
	# si le nom de la tache = au nom recherché 
	if todo[i]["nom"] = nom_termine:
	# on met l'etat a TRUE
	todo[i]["etat"] = True
	tache_trouve = True
	print("tache", nom_termine, "est marqué comme terminé")
i = i + 1

