---
title: Hinzufügen, Löschen und Ersetzen von Ressourcen
description: In diesem Thema wird erläutert, wie Ressourcen hinzugefügt, gelöscht oder ersetzt werden.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c23375dbfff770a22b96ef7cb517af1c0b8d40579d6919a31a8136e1691474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735293"
---
# <a name="adding-deleting-and-replacing-resources"></a>Hinzufügen, Löschen und Ersetzen von Ressourcen

Anwendungen müssen häufig Ressourcen in ausführbaren Dateien hinzufügen, löschen oder ersetzen. Für diese Aufgaben können zwei Methoden verwendet werden. Die erste besteht in der Bearbeitung der Ressourcendefinitionsdatei, dem erneuten Kompilieren der Ressourcen und dem Hinzufügen der neu kompilierten Ressourcen zur ausführbaren Datei der Anwendung. Die zweite Methode besteht im Kopieren der Ressourcendaten direkt in die ausführbare Datei der Anwendung.

Um beispielsweise eine englischsprachige Anwendung für die Verwendung in Norwegen zu lokalisieren, kann es erforderlich sein, das Dialogfeld Englisch durch eine Anwendung zu ersetzen, die Norwegisch verwendet. Ein Entwickler erstellt ein entsprechendes Dialogfeld, indem er einen Dialogfeld-Editor verwendet oder eine Vorlage in die Ressourcendefinitionsdatei schreibt. Der Entwickler kompiliert dann die Ressourcen neu und fügt die neuen Ressourcen der ausführbaren Datei der Anwendung hinzu.

Wenn ein entsprechendes Dialogfeld in binärer Form vorhanden ist, kann der Entwickler die Daten jedoch mithilfe der folgenden Funktionen direkt in die ausführbare Datei kopieren, die lokalisiert wird. Die [**BeginUpdateResource-Funktion**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) erstellt ein Updatehand handle für die ausführbare Datei, deren Ressourcen geändert werden sollen. Die [**UpdateResource-Funktion**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) verwendet dieses Handle, um eine Ressource in der ausführbaren Datei hinzuzufügen, zu löschen oder zu ersetzen. Die [**EndUpdateResource-Funktion**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) schließt das Handle.

Nachdem ein Updatehand handle für eine ausführbare Datei von [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)erstellt wurde, kann eine Anwendung [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) wiederholt verwenden, um Änderungen an den Ressourcendaten vorzunehmen. Jeder Aufruf von **UpdateResource** trägt zu einer internen Liste von Ergänzungen, Löschungen und Ersetzungen bei, schreibt die Daten jedoch nicht in die ausführbare Datei. Unmittelbar vor dem Schließen des Updatehandpunkts schreibt [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) die kumulierten Änderungen in die ausführbare Datei.

Manchmal muss eine Anwendung Ressourcen aus einer anderen Datei kopieren. [Das Aktualisieren von](using-resources.md) Ressourcen zeigt ein Beispiel für das Abrufen der Ressourcendaten und ihrer Größe aus einer Datei.

 

 




