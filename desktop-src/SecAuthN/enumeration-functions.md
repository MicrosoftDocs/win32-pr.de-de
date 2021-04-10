---
description: Wenn Ihr Netzwerkanbieter das Durchsuchen der Netzwerkressourcen unterstützen muss, sollten die folgenden Funktionen implementiert werden. MPR ruft diese Funktionen auf, um die Ressourcen aufzuzählen.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Enumerationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041670"
---
# <a name="enumeration-functions"></a>Enumerationsfunktionen

Wenn Ihr Netzwerkanbieter das Durchsuchen der Netzwerkressourcen unterstützen muss, sollten die folgenden Funktionen implementiert werden. MPR ruft diese Funktionen auf, um die Ressourcen aufzuzählen.

Es ist nicht erforderlich, dass ein Netzwerkanbieter eine der-Enumerationsfunktionen implementiert. Wenn ein Netzwerkanbieter jedoch entweder " [**npopenenum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)", " [**npoumresource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)" oder " [**npcloseenum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)" implementiert, muss er auch die anderen beiden Enumerationsfunktionen implementieren.



| Funktion                                                     | BESCHREIBUNG                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Npopenum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Öffnet eine Enumeration von Netzwerkressourcen oder vorhandenen Verbindungen.                                                                                                  |
| [**Npumschlag Resource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Führt eine Enumeration für ein von [**npopenum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)zurück gegebenes Handle aus.                                                                                   |
| [**Npcloseenum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Schließt eine Enumeration.                                                                                                                                              |
| [**Npgetresourceinformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Bestimmt, ob der Anbieter der richtige Anbieter ist, um auf eine Anforderung für eine angegebene Netzwerkressource zu antworten, und gibt Informationen über den Ressourcentyp zurück. |
| [**Npgetresourceparent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Gibt das übergeordnete Element einer angegebenen Netzwerkressource in der durchsuchen-Hierarchie zurück.                                                                                         |



 

 

 



