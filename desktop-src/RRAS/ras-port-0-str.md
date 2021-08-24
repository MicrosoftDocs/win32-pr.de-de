---
title: RAS_PORT_0 -Struktur (Rassapi.h)
description: Die RAS \_ PORT \_ 0-Struktur enthält Informationen, die einen RAS-Port beschreiben.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 Ras-Struktur
- PRAS_PORT_0 Strukturzeiger RAS
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67891ccd65aaa56fc41dd077ae46bd4bf61f816cdc02afeb65964886cbaf9562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673130"
---
# <a name="ras_port_0-structure"></a>\_RAS-PORT \_ 0-Struktur

\[Diese Version der **\_ RAS-Port \_ 0-Struktur** wird ab version Windows Vista nicht mehr unterstützt. Verwenden Sie stattdessen den [**neueren \_ RAS-PORT \_ 0,**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) der in mprapi.h definiert ist.\]

Die **RAS \_ PORT \_ 0-Struktur** enthält Informationen, die einen RAS-Port beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a>Member

<dl> <dt>

**wszPortName**
</dt> <dd>

Eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Ports angibt, z. B. "COM1".

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Eine auf NULL terminierte Unicode-Zeichenfolge, die den Typ des Geräts angibt, auf dem die Verbindung hergestellt wurde, z. B. Modem oder ISDN. Die Liste der Gerätetypen, die in diesem Member angegeben werden können, enthält alle auf dem Server installierten Gerätetypen, einschließlich Drittanbietergeräten.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Eine auf NULL terminierte Unicode-Zeichenfolge, die den Namen des Geräts angibt, auf dem die Verbindung hergestellt wurde, z. B. "9600" oder "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Gibt eine auf NULL terminierte Unicode-Zeichenfolge an, die den Namen des mediums angibt, das für die Verbindung verwendet wird, z. B. *"lauter"* oder *"attributapi".*

</dd> <dt>

**reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Flags**
</dt> <dd>

Gibt einen Satz von Bitflags an, die die Art der verbindung an diesem Port angeben. Dieser Member kann eine Kombination der folgenden Flags sein.



| Wert                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**GATEWAY \_ AKTIV**</dt> </dl>             | Wenn dieses Flag festgelegt ist, ist das NetBIOS-Gateway auf dem Server aktiv.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ PRESENT**</dt> </dl>    | Wenn dieses Flag festgelegt ist, wird der Messenger-Dienst auf dem Remoteclient ausgeführt.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PORT \_ MULTILINKED**</dt> </dl>       | Wenn dieses Flag festgelegt ist, ist der Port mehrfach mit anderen Ports verknüpft. Verwenden Sie diese Informationen, um den Verbindungsstatus als Multilinkport anzuzeigen. <br/> Bei einem Multilinkport enthält die [**\_ RAS-PORTSTATISTIK-Struktur \_**](ras-port-statistics-str.md) zwei Statistiksätze: einen für den Port allein und einen für die kombinierten Ports in der Multilinkverbindung.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**CLIENTCLIENT FÜR DEN CLIENT \_**</dt> </dl>                         | Wenn dieses Flag festgelegt ist, hat der Remoteclient eine Verbindung mithilfe von PPP hergestellt. Wenn dieses Flag nicht festgelegt ist, ist der Remoteclient über das AMB-Protokoll verbunden.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**\_REMOTEÜBERWACHUNG**</dt> </dl>                | Wenn dieses Flag festgelegt ist, wird der RemoteListen-Parameter des NetBIOS-Gateways auf dem Server auf 1 festgelegt.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**BENUTZER \_ AUTHENTIFIZIERT**</dt> </dl> | Wenn dieses Flag festgelegt ist, wird ein Remoteclient mit dem Server verbunden, und der Benutzer wurde authentifiziert. Überprüfen Sie dieses Flag, um sicherzustellen, dass ein Client tatsächlich mit einem Port verbunden ist.<br/>                                                                                                                                                                                                   |



 

Wenn die Flags MESSENGER PRESENT, GATEWAY ACTIVE und REMOTE LISTEN festgelegt sind, verwenden Sie den Messenger-Dienst, um eine Verwaltungsnachricht an \_ \_ den \_ Remoteclient zu senden. Wenn MESSENGER PRESENT und REMOTE LISTEN festgelegt sind, GATEWAY ACTIVE jedoch nicht, senden Sie Nachrichten nur von dem RAS-Server, mit dem der Client \_ \_ verbunden \_ ist, an den Client.

</dd> <dt>

**wszUserName**
</dt> <dd>

Eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Remotebenutzers angibt, der mit diesem Port verbunden ist.

</dd> <dt>

**wszComputer**
</dt> <dd>

Eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Remoteclientcomputers angibt.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Gibt die Zeit in Sekunden ab dem 1. Januar 1970 an, die der Client an diesem Port mit dem RAS-Server verbunden hat. Verwenden Sie die Standardzeitfunktionen, um diesen Wert für die Anzeige zu formatieren.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Gibt eine auf NULL terminierte Unicode-Zeichenfolge an, die den Namen der Domäne angibt, in der der Remotebenutzer authentifiziert wurde. Diese Zeichenfolge ist nur der Domänenname ohne Präfix \\ \\ "".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Gibt ein Flag ungleich 0 an, wenn der diesem Port zugeordnete RAS-Server ein erweiterter Server wie Windows 2000 Advanced Server ist. Verwenden Sie diese Informationen, um den Namen des Servers zu bestimmen, der über die Benutzerkontodatenbank verfügt. Wenn der RAS-Server ein erweiterter Server ist, erhalten Sie den Namen des Benutzerkontoservers, indem Sie das Präfix " " mit dem Namen verketten, der im \\ \\ **wszLogonDomain-Mitglied zurückgegeben** wird. Dies liegt daran, dass für einen erweiterten Server der Name der lokalen Anmeldedomäne mit dem Servernamen identisch ist. Wenn der RAS-Server eine Arbeitsstation ist, verwenden Sie die [**RasAdminGetUserAccountServer-Funktion,**](rasadmingetuseraccountserver.md) um den Namen des Benutzerkontoservers zu erhalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**\_RAS-PORT \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_ \_ RAS-PORTSTATISTIK**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





