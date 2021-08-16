---
description: Implementieren von Kontextmenüerweiterungen
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementieren von Kontextmenüerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090f37b4cf77f9508e8c149ef6389297c561e1a4e574ef767f3a5e5c7e07fe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194683"
---
# <a name="implementing-context-menu-extensions"></a>Implementieren von Kontextmenüerweiterungen

Die WPD-Namespaceerweiterung unterstützt erweiterbare Kontextmenüs (oder Kontextmenüs). Dies sind die Menüs, die angezeigt werden, wenn ein Benutzer mit der rechten Maustaste auf ein Objekt klickt, z. B. eine Datei oder einen Ordner. Einige WPD-Anwendungen nutzen diese erweiterbaren Menüs, um Vorgänge für geräteseitige Inhalte (oder Objekte, die sich auf dem Gerät befinden) zu unterstützen.

Erweiterbare Kontextmenüs werden von den in der folgenden Tabelle beschriebenen Schnittstellen unterstützt. Weitere Informationen zu diesen Schnittstellen finden Sie im Windows SDK.



| Schnittstelle           | Beschreibung                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | Die Windows Vista Shell ruft die Methoden in dieser Schnittstelle auf, um das neue Kontextmenü mit dem angegebenen Objekt zu erstellen oder zusammenzuführen. |
| Idataobject         | Wird verwendet, um das PIDL-Array des Kontextmenüs an den Kontextmenühandler zu übergeben.                                                    |
| IPropertySetStorage | Diese Schnittstelle wird verwendet, um WPD-Eigenschaften für das angegebene Objekt abzurufen.                                                    |
| IPropertyStorage    | Diese Schnittstelle wird auch verwendet, um WPD-Eigenschaften für das angegebene Objekt abzurufen.                                               |
| IShellExtInit       | Initialisiert die Windows Vista Shell-Erweiterungen für das Kontextmenü.                                                       |
| Istream             | Zu liefernde .                                                                                                            |



 

Kontextmenüs für WPD werden wie jedes andere Kontextmenü in Windows Vista implementiert. Wenn Sie bereits einen Kontextmenühandler implementiert haben, können Sie Ihren vorhandenen Code so ändern, dass er geräteseitigen Inhalt unterstützt. Wenn Sie noch nie einen Kontextmenühandler erstellt haben, lesen Sie das Thema Erstellen von Kontextmenühandlern im Windows SDK.

Die beiden Punkte, an denen sich ein WPD-Kontextmenühandler von jedem anderen Handler unterscheidet, sind die Handlerregistrierung und die Unterstützung von geräteseitigem Inhalt.

 

 



