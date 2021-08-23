---
description: NLA-Clients können Netzwerkkonfigurationsinformationen systemweit aufzeichnen, sodass zukünftige Abfragen die angegebenen Konfigurationsinformationen unabhängig davon zurückgeben können, ob das Netzwerk aktiv ist.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrieren einer Dienstinstanz mit NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623f28d30d02cd3a1266e173dbe28270f377a55c3f59f8ff095cf3d023a80eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641680"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrieren einer Dienstinstanz mit NLA

NLA-Clients können Netzwerkkonfigurationsinformationen systemweit aufzeichnen, sodass zukünftige Abfragen die angegebenen Konfigurationsinformationen unabhängig davon zurückgeben können, ob das Netzwerk aktiv ist. Diese Funktion ermöglicht es NLA-Clients, eine konsistente Benutzeroberfläche für Netzwerkinformationen in mehreren Anwendungen zu beeinflussen.

## <a name="parameters"></a>Parameter

Verwenden Sie die [**WSASetService-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) um eine Dienstinstanz beim Netzwerkspeicherorts-Dienstanbieter zu registrieren. Um eine Dienstinstanz ordnungsgemäß zu registrieren, müssen bestimmte Parameter der **WSASetService-Funktion** mit den entsprechenden Informationen festgelegt werden, wie in diesem Abschnitt erläutert. Als Kurzreferenz verfügt die **WSASetService-Funktion** über die folgende Syntax:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Geben Sie für den *lpqsRegInfo-Parameter* eine [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) aus einem NLA-SP-Abfrageergebnis oder gemäß den Anforderungen einer NLA-SP-Abfrage an, wie in Abfragen von [NLA angegeben.](querying-nla-2.md)

Folgende Vorgänge werden für *den essOperation-Parameter* unterstützt:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE \_ REGISTER
</dt> <dd>

Das netzwerkdefiniert in der [**WSAQUERYSET-Struktur,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) das in *lpqsRegInfo* bereitgestellt wird, wird für den aktiven Benutzer persistent gemacht, indem die Netzwerkinstanz in der Registrierungsstruktur für den aktuellen Benutzer gespeichert wird, wodurch Identitätswechsel ermöglicht werden.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ DELETE
</dt> <dd>

Wenn das in der [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) in *lpqsRegInfo* definierte Netzwerk persistent ist, wird es entfernt.

</dd> </dl>

Der im *essOperation-Parameter* angegebene Vorgang kann durch die folgenden Optionen geändert werden, die mit binärer OR-Logik angegeben werden können:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_NLA-BENUTZERFREUNDLICHER \_ NAME
</dt> <dd>

Bei Verwendung mit RNRSERVICE REGISTER wird das \_ *lpszComment-Feld* des in *lpqsRegInfo* definierten Netzwerks auf Gültigkeit überprüft und dauerhaft gespeichert. Bei Verwendung mit RNRSERVICE DELETE und dem definierten Netzwerk mit einem Benutzerfreundlichen Namen wird der Name entfernt, aber der \_ Netzwerkeintrag bleibt erhalten.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA \_ ALLUSERS \_ NETWORK
</dt> <dd>

Bei Verwendung mit RNRSERVICE REGISTER wird der Eintrag dauerhaft unter HKEY LOCAL MACHINE gespeichert, wodurch er während Abfragen für alle Benutzer auf dem \_ \_ lokalen Computer verfügbar \_ ist. Bei Verwendung mit RNRSERVICE \_ DELETE wird das angegebene Netzwerk aus HKEY LOCAL MACHINE \_ \_ entfernt. Wenn das angegebene Netzwerk nicht vorhanden ist, wird ein Fehler zurückgegeben. Um ein Netzwerk aus der Registrierungsstruktur des aktuellen Benutzers zu löschen, darf dieses Flag nicht angegeben werden. Dieses Flag ist nur im Sicherheitskontext eines lokalen Systemadministrators gültig.

</dd> </dl>

NLA unterstützt die folgenden Fehlercodes für [**WSASetService-Funktionsaufrufe:**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

| Fehler             | Bedeutung                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Ein erfolgreicher Aufruf der [**WSAStartup-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsastartup) zum Initialisieren der NLA wurde nicht ausgeführt.                                                                  |
| WSAEACCESS        | NLA \_ ALLUSERS \_ NETWORK wurde in *dwControlFlags* angegeben, jedoch nicht im Sicherheitskontext eines lokalen Systemadministrators.                                                |
| WSAEALREADY       | Das angegebene Netzwerk wird bereits dauerhaft auf die angeforderte Weise gespeichert, und es wurden keine Flags in *dwControlFlags* angegeben, um auf eine Aktualisierung des vorhandenen Eintrags hindeuten zu können. |
| WSAEAFNOSUPPORT   | Es wurde eine Protokollfamilie angegeben, für die keine Unterstützung besteht. In NLA werden nur IP-Protokollfamilien unterstützt.                                                             |
| WSAEPFNOSUPPORT   | Es wurde ein Protokoll angegeben, für das keine Unterstützung besteht. In NLA wird nur das IP-Protokoll unterstützt.                                                                              |



 

 

 



