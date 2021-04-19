---
description: Implementieren von Eigenschaften Blatt Erweiterungen
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementieren von Eigenschaften Blatt Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369080"
---
# <a name="implementing-property-sheet-extensions"></a>Implementieren von Eigenschaften Blatt Erweiterungen

Die WPD-Namespace Erweiterung unterstützt erweiterbare Eigenschaften Blätter. Dies sind die Eigenschaften Dialogfelder, die angezeigt werden, wenn ein Benutzer mit der rechten Maustaste auf ein Objekt, z. b. eine Datei oder einen Ordner, klickt und **Eigenschaften** auswählt. Einige WPD-Anwendungen nutzen diese erweiterbaren Eigenschaften Blätter, um die Eigenschaften für Geräte seitigen Inhalt (oder Objekte, die sich auf dem Gerät befinden) anzuzeigen.

Erweiterbare Eigenschaften Blätter werden von den in der folgenden Tabelle beschriebenen Schnittstellen unterstützt. Weitere Informationen zu diesen Schnittstellen finden Sie in der Windows SDK.



| Schnittstelle           | BESCHREIBUNG                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Wird verwendet, um das PIDL-Array des Kontextmenüs an den Kontextmenü Handler zu übergeben.      |
| IPropertySetStorage | Diese Schnittstelle wird verwendet, um WPD-Eigenschaften für das angegebene Objekt abzurufen.      |
| IPropertyStorage    | Diese Schnittstelle wird auch zum Abrufen von WPD-Eigenschaften für das angegebene Objekt verwendet. |
| Ishellextinit       | Initialisiert die Windows Vista-Shellerweiterungen für das Kontextmenü.         |
| Ishellpropsheetext  | Unterstützt das Hinzufügen von Eigenschaften Blatt Erweiterungen.                              |



 

Eigenschaften Blätter für WPD werden wie jedes andere Eigenschaften Blatt in Windows Vista implementiert. Wenn Sie bereits einen Eigenschaften Blatt Handler implementiert haben, können Sie den vorhandenen Code so ändern, dass er den Geräte seitigen Inhalt unterstützt. Wenn Sie noch nie einen Kontextmenü Handler erstellt haben, lesen Sie das Thema Erstellen von Eigenschaften Blatt Handlern in der Windows SDK.

Die zwei Punkte, an denen ein WPD-Eigenschaften Blatt Handler von einem anderen Handler abweicht, ist die Handlerregistrierung und die Unterstützung von Geräte seitigem Inhalt.

 

 



