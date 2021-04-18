---
description: Implementieren von Kontextmenü Erweiterungen
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementieren von Kontextmenü Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347600"
---
# <a name="implementing-context-menu-extensions"></a>Implementieren von Kontextmenü Erweiterungen

Die WPD-Namespace Erweiterung unterstützt erweiterbare Kontextmenüs (oder Verknüpfungs Menüs). Dies sind die Menüs, die angezeigt werden, wenn ein Benutzer mit der rechten Maustaste auf ein Objekt, z. b. eine Datei oder einen Ordner, klickt. Einige WPD-Anwendungen profitieren von diesen erweiterbaren Menüs, um Vorgänge für Geräte seitigen Inhalt (oder Objekte, die sich auf dem Gerät befinden) zu unterstützen.

Erweiterbare Kontextmenüs werden von den in der folgenden Tabelle beschriebenen Schnittstellen unterstützt. Weitere Informationen zu diesen Schnittstellen finden Sie in der Windows SDK.



| Schnittstelle           | BESCHREIBUNG                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | Die Windows Vista-Shell Ruft die Methoden in dieser Schnittstelle auf, um das neue Kontextmenü mit dem angegebenen Objekt zu erstellen oder zusammenzuführen. |
| IDataObject         | Wird verwendet, um das PIDL-Array des Kontextmenüs an den Kontextmenü Handler zu übergeben.                                                    |
| IPropertySetStorage | Diese Schnittstelle wird verwendet, um WPD-Eigenschaften für das angegebene Objekt abzurufen.                                                    |
| IPropertyStorage    | Diese Schnittstelle wird auch zum Abrufen von WPD-Eigenschaften für das angegebene Objekt verwendet.                                               |
| Ishellextinit       | Initialisiert die Windows Vista-Shellerweiterungen für das Kontextmenü.                                                       |
| IStream             | , Um bereitgestellt zu werden.                                                                                                            |



 

Kontextmenüs für WPD werden wie jedes andere Kontextmenü in Windows Vista implementiert. Wenn Sie bereits einen Kontextmenü Handler implementiert haben, können Sie den vorhandenen Code so ändern, dass er den Geräte seitigen Inhalt unterstützt. Wenn Sie noch nie einen Kontextmenü Handler erstellt haben, lesen Sie das Thema Erstellen von Kontextmenü Handlern in der Windows SDK.

Die zwei Punkte, an denen ein WPD-Kontextmenü Handler von einem anderen Handler abweicht, ist die Handlerregistrierung und die Unterstützung von Geräte seitigem Inhalt.

 

 



