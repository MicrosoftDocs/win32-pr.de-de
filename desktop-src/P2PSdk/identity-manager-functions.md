---
description: Die Peer Identity Manager-API verwendet die folgenden Funktionen.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Identity Manager-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a640aa7250cdf34fed7440d955a8de8ac7ac1a58316bef3f6e97b3564ac7fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518570"
---
# <a name="identity-manager-functions"></a>Identity Manager-Funktionen

Die Peer Identity Manager-API verwendet die folgenden Funktionen.



| Funktion                                                           | Beschreibung                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Erstellt einen neuen Namen basierend auf dem vorhandenen Namen der angegebenen Peeridentität und des angegebenen Klassifizierers. Eine neue Identität wird jedoch nicht durch einen Aufruf von [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)erstellt.                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Erstellt ein Peerenumerationshandle, das zum Aufzählen aller Peergruppen verwendet wird, die einer bestimmten Peeridentität zugeordnet sind, und gibt dieses zurück.                                                                                                                                                                          |
| [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Erstellt ein Peerenumerationshandle, das zum Aufzählen aller Peeridentitäten eines bestimmten Benutzers verwendet wird, und gibt dieses zurück.                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Gibt eine Enumeration frei, z. B. einen Datensatz oder eine Memberenumeration, und hebt die Zuordnung aller Ressourcen auf, die der Enumeration zugeordnet sind.                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Hebt die Zuordnung eines Datenblocks auf und gibt ihn an den Speicherpool zurück.                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Gibt die Anzahl der Elemente in einer Peerenumeration zurück.                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Gibt eine bestimmte Anzahl von Elementen aus einer Peerenumeration zurück.                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Erstellt eine neue Peeridentität und gibt ihren Namen zurück. Der Name der Peeridentität muss in allen nachfolgenden Aufrufen an die Peeridentitäts-Manager-, Peergruppierungs- oder PNRP-Funktionen übergeben werden, die im Namen der Peeridentität ausgeführt werden. Der Peeridentitätsname gibt an, welche Peeridentität verwendet wird. |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Löscht eine Peeridentität. Dies schließt das Entfernen aller Zertifikate, privaten Schlüssel und aller Gruppeninformationen ein, die einer angegebenen Peeridentität zugeordnet sind.                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Ermöglicht es einem Benutzer, eine Peeridentität zu exportieren. Der Benutzer kann dann die Peeridentität auf einen anderen Computer übertragen.                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Ruft ein Handle für einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) ab.                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Ruft den Standard-Peernamen ab, der für den aktuellen Benutzer festgelegt ist.                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Gibt den Anzeigenamen der Peeridentität zurück.                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Gibt eine Beschreibung der Peeridentität zurück, die dann an Dritte übergeben und verwendet werden kann, um eine Peeridentität in eine Peergruppe einzuladen. Diese Informationen werden als XML-Fragment zurückgegeben.                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importiert eine Peeridentität. Wenn die Peeridentität auf einem Computer vorhanden ist, wird **PEER \_ E ALREADY \_ \_ EXISTS** zurückgegeben.                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Ändert den Anzeigenamen für eine angegebene Peeridentität. Der Anzeigename ist der für Menschen lesbare Name.                                                                                                                                                                                                |



 

 

 



