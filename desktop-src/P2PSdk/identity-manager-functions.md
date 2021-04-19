---
description: Die Peer Identity Manager-API verwendet die folgenden Funktionen.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Identity Manager-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea56df6500239141038f76ba312b84148581f8f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360548"
---
# <a name="identity-manager-functions"></a>Identity Manager-Funktionen

Die Peer Identity Manager-API verwendet die folgenden Funktionen.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer Name"**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Erstellt einen neuen Namen auf der Grundlage des vorhandenen namens der angegebenen Peer Identität und-Klassifizierung. Allerdings wird eine neue Identität nicht durch einen Aufrufen von "Peer-up- [**Peer Name**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)" erstellt.                                                                                                     |
| [**Peer Enumgroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Erstellt ein peerenumerationshandle, das verwendet wird, um alle Peer Gruppen aufzulisten, die einer bestimmten Peer Identität zugeordnet sind, und gibt es zurück.                                                                                                                                                                          |
| [**Peer-Identitäts dentitäten**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Erstellt und gibt ein peerenumerationshandle zurück, mit dem alle Peer Identitäten aufgelistet werden, die zu einem bestimmten Benutzer gehören.                                                                                                                                                                                |
| [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Gibt eine Enumeration frei, z. b. einen Datensatz oder eine Member-Enumeration, und hebt die Zuordnung aller der-Enumeration zugeordneten Ressourcen auf.                                                                                                                                                                   |
| [**"Peer"-Daten**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Hebt die Zuordnung eines Datenblocks auf und gibt ihn an den Speicherpool zurück.                                                                                                                                                                                                                                         |
| [**"Peer-GetItemCount"**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Gibt die Anzahl der Elemente in einer Peer Enumeration zurück.                                                                                                                                                                                                                                                    |
| [**"Peer GetNextItem"**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Gibt eine bestimmte Anzahl von Elementen aus einer Peer Enumeration zurück.                                                                                                                                                                                                                                            |
| [**"Peer Identity"**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Erstellt eine neue Peer Identität und gibt Ihren Namen zurück. Der Name der Peer Identität muss in allen nachfolgenden Aufrufen an den Peer Identity Manager, die Peer Gruppierung oder die PNRP-Funktionen, die im Namen der Peer Identität ausgeführt werden, weitergegeben werden. Der Peer-Identitäts Name gibt an, welche Peer Identität verwendet wird. |
| [**"Peer Identity"**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Löscht eine Peer Identität. Dies schließt das Entfernen aller Zertifikate, der privaten Schlüssel und aller Gruppeninformationen ein, die einer bestimmten Peer Identität zugeordnet sind.                                                                                                                                                   |
| [**Peer Identity-Export**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Ermöglicht es einem Benutzer, eine Peer Identität zu exportieren. Der Benutzer kann dann die Peer Identität auf einen anderen Computer übertragen.                                                                                                                                                                                       |
| [**"Peer Identity tygetcryptkey"**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Ruft ein Handle für einen Kryptografiedienstanbieter (CSP) ab.                                                                                                                                                                                                                                          |
| [**"Peer Identity tygetdefault"**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Ruft den für den aktuellen Benutzer festgelegten Standard Peer Namen ab.                                                                                                                                                                                                                                              |
| [**"Peer Identity Name"**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Gibt den anzeigen amen der Peer Identität zurück.                                                                                                                                                                                                                                                        |
| [**"Peer Identity tygetxml"**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Gibt eine Beschreibung der Peer Identität zurück, die dann an Dritte weitergegeben und zum einladen einer Peer Identität in eine Peer Gruppe verwendet werden kann. Diese Informationen werden als XML-Fragment zurückgegeben.                                                                                                           |
| [**"Peer Identity"**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importiert eine Peer Identität. Wenn die Peer Identität auf einem Computer vorhanden ist, wird **Peer \_ E \_ bereits \_ vorhanden** sein.                                                                                                                                                                                        |
| [**"Peer Identity Name"**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Ändert den anzeigen Amen für eine angegebene Peer Identität. Der Anzeige Name ist der lesbare Name.                                                                                                                                                                                                |



 

 

 



