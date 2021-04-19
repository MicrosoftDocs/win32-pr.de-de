---
title: Hinzufügen, löschen und Ersetzen von Ressourcen
description: In diesem Thema wird erläutert, wie Ressourcen hinzugefügt, gelöscht oder ersetzt werden.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342285"
---
# <a name="adding-deleting-and-replacing-resources"></a>Hinzufügen, löschen und Ersetzen von Ressourcen

Anwendungen müssen häufig Ressourcen in ausführbaren Dateien hinzufügen, löschen oder ersetzen. Zum Ausführen dieser Aufgaben können zwei Methoden verwendet werden. Der erste besteht darin, die Ressourcen Definitionsdatei zu bearbeiten, die Ressourcen neu zu kompilieren und die neu kompilierten Ressourcen der ausführbaren Datei der Anwendung hinzuzufügen. Die zweite Methode besteht darin, die Ressourcen Daten direkt in die ausführbare Datei der Anwendung zu kopieren.

Wenn Sie z. b. eine englischsprachige Anwendung für die Verwendung in Norwegen lokalisieren möchten, ist es möglicherweise erforderlich, das englische Dialogfeld durch eine norwegische zu ersetzen. Ein Entwickler erstellt ein entsprechendes Dialogfeld, indem er einen Dialogfeld-Editor verwendet oder eine Vorlage in der Ressourcen Definitionsdatei schreibt. Der Entwickler kompiliert dann die Ressourcen neu und fügt die neuen Ressourcen der ausführbaren Datei der Anwendung hinzu.

Wenn ein entsprechendes Dialogfeld in Binär Form vorhanden ist, kann der Entwickler die Daten jedoch mithilfe der folgenden Funktionen direkt in die zu Lokalisier Ende ausführbare Datei kopieren. Die [**beginupdateresource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) -Funktion erstellt ein Aktualisierungs Handle für die ausführbare Datei, deren Ressourcen geändert werden sollen. Die [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) -Funktion verwendet dieses Handle, um eine Ressource in der ausführbaren Datei hinzuzufügen, zu löschen oder zu ersetzen. Die [**endupdateresource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) -Funktion schließt das handle.

Nachdem ein Aktualisierungs Handle für eine ausführbare Datei von [**beginupdateresource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)erstellt wurde, kann eine Anwendung [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) wiederholt verwenden, um Änderungen an den Ressourcen Daten vorzunehmen. Jeder **UpdateResource** -Aufrufe trägt zu einer internen Liste von Ergänzungen, Löschungen und Ersetzungen bei, schreibt die Daten jedoch nicht in die ausführbare Datei. Direkt vor dem Schließen des Aktualisierungs Handles schreibt [**endupdateresource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) die akkumulierten Änderungen in die ausführbare Datei.

Manchmal muss eine Anwendung Ressourcen aus einer anderen Datei kopieren. Das [Aktualisieren von Ressourcen](using-resources.md) zeigt ein Beispiel für das Abrufen der Ressourcen Daten und ihrer Größe aus einer Datei.

 

 




