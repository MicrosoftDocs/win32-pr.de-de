---
description: NLA-Clients können Netzwerk Konfigurationsinformationen auf systemweite Basis aufzeichnen, sodass zukünftige Abfragen die angegebenen Konfigurationsinformationen unabhängig davon zurückgeben können, ob das Netzwerk aktiv ist.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrieren einer Dienst Instanz bei NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348550"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrieren einer Dienst Instanz bei NLA

NLA-Clients können Netzwerk Konfigurationsinformationen auf systemweite Basis aufzeichnen, sodass zukünftige Abfragen die angegebenen Konfigurationsinformationen unabhängig davon zurückgeben können, ob das Netzwerk aktiv ist. Diese Funktion ermöglicht es NLA-Clients, eine konsistente Netzwerk Informations Benutzer-Benutzer Funktionalität über mehrere Anwendungen hinweg zu beeinflussen.

## <a name="parameters"></a>Parameter

Verwenden Sie die [**wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) -Funktion, um eine Dienst Instanz beim Network Location Awareness Service-Anbieter zu registrieren. Um eine Dienst Instanz ordnungsgemäß zu registrieren, müssen bestimmte Parameter der **wsasetservice** -Funktion mit den entsprechenden Informationen festgelegt werden, wie in diesem Abschnitt erläutert wird. Die **wsasetservice** -Funktion weist die folgende Syntax auf:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Geben Sie für den *lpqsreginfo* -Parameter eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur entweder aus einem NLA SP-Abfrageergebnis an, oder erstellen Sie die Anforderungen einer NLA SP-Abfrage, wie unter [Abfragen von NLA](querying-nla-2.md)angegeben.

Folgende Vorgänge werden für den Parameter " *ESS Operation* " unterstützt:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>rnrservice- \_ Registrierung
</dt> <dd>

Das in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur in *lpqsreginfo* angegebene Netzwerk wird für den aktiven Benutzer persistent gemacht, indem die Netzwerk Instanz in der Registrierungs Struktur für den aktuellen Benutzer gespeichert wird, wodurch der Identitätswechsel ermöglicht wird.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>rnrservice \_ Löschen
</dt> <dd>

Wenn das in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur in *lpqsreginfo* angegebene Netzwerk persistent ist, wird es entfernt.

</dd> </dl>

Der im Parameter " *ESS Operation* " angegebene Vorgang kann mit den folgenden Optionen geändert werden, die mit binary oder Logic angegeben werden können:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA-Anzeige \_ \_ Name
</dt> <dd>

Bei Verwendung mit rnrservice- \_ Register wird das *lpszcomment* -Feld des in *lpqsreginfo* definierten Netzwerks auf Gültigkeit überprüft und dauerhaft gespeichert. Bei Verwendung mit rnrservice \_ delete und dem definierten Netzwerk mit einem anzeigen Amen wird der Anzeige Name entfernt, aber der Netzwerk Eintrag bleibt intakt.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA- \_ ALLUSERS- \_ Netzwerk
</dt> <dd>

Bei Verwendung mit dem rnrservice- \_ Register wird der Eintrag dauerhaft unter HKEY \_ local \_ Machine gespeichert, sodass er während der Abfragen für alle Benutzer auf dem lokalen Computer verfügbar ist. Bei Verwendung mit rnrservice \_ Delete wird das angegebene Netzwerk von HKEY \_ Local Machine entfernt \_ . Wenn das angegebene Netzwerk nicht vorhanden ist, wird ein Fehler zurückgegeben. Um ein Netzwerk aus der Registrierungs Struktur des aktuellen Benutzers zu löschen, darf dieses Flag nicht angegeben werden. Dieses Flag ist nur im Sicherheitskontext eines lokalen Systemadministrators gültig.

</dd> </dl>

NLA unterstützt die folgenden Fehlercodes für [**wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) -Funktionsaufrufe:

| Fehler             | Bedeutung                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Ein erfolgreicher Rückruf der [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion zum Initialisieren der NLA wurde nicht ausgeführt.                                                                  |
| Wsaeaccess        | Das Netzwerk "NLA \_ ALLUSERS" \_ wurde in " *dwcontrolflags* " angegeben, während es sich nicht im Sicherheitskontext eines lokalen Systemadministrators befand.                                                |
| Wsaebereits       | Das angegebene Netzwerk wurde bereits dauerhaft in der angeforderten Weise gespeichert, und in *dwcontrolflags* wurden keine Flags angegeben, um ein Update für den vorhandenen Eintrag anzugeben. |
| WSAEAFNOSUPPORT   | Es wurde eine Protokollfamilie angegeben, für die keine Unterstützung vorhanden ist. In NLA werden nur IP-Protokoll Familien unterstützt.                                                             |
| Wsaepf NoSupport   | Es wurde ein Protokoll angegeben, für das keine Unterstützung vorhanden ist. In NLA wird nur das IP-Protokoll unterstützt.                                                                              |



 

 

 



