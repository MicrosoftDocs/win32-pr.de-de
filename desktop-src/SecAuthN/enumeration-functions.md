---
description: Wenn Ihr Netzwerkanbieter das Durchsuchen seiner Netzwerkressourcen unterstützen muss, sollte er die folgenden Funktionen implementieren. MPR ruft diese Funktionen auf, um die Ressourcen aufzuzählen.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Enumerationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f119256c4976e393795b45caf2fab9e7cec5353fed54718ef0be8db994ef2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008238"
---
# <a name="enumeration-functions"></a>Enumerationsfunktionen

Wenn Ihr Netzwerkanbieter das Durchsuchen seiner Netzwerkressourcen unterstützen muss, sollte er die folgenden Funktionen implementieren. MPR ruft diese Funktionen auf, um die Ressourcen aufzuzählen.

Ein Netzwerkanbieter ist nicht erforderlich, um eine der Enumerationsfunktionen zu implementieren. Wenn ein Netzwerkanbieter jedoch entweder [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)oder [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)implementiert, muss er auch die anderen beiden Enumerationsfunktionen implementieren.



| Funktion                                                     | Beschreibung                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Öffnet eine Enumeration von Netzwerkressourcen oder vorhandenen Verbindungen.                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Führt eine Enumeration für ein handle aus, das von [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)zurückgegeben wird.                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Schließt eine Enumeration.                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Bestimmt, ob der Anbieter der richtige Anbieter ist, der auf eine Anforderung für eine angegebene Netzwerkressource antwortet, und gibt Informationen zum Typ der Ressource zurück. |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Gibt das übergeordnete Element einer angegebenen Netzwerkressource in der Durchsuchenhierarchie zurück.                                                                                         |



 

 

 



