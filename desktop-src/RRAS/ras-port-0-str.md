---
title: RAS_PORT_0 Struktur (rassapi. h)
description: Die Struktur des RAS- \_ Ports \_ 0 enthält Informationen, die einen RAS-Port beschreiben.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 Struktur-RAS
- PRAS_PORT_0-Struktur Zeiger RAS
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
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517882"
---
# <a name="ras_port_0-structure"></a>RAS- \_ Port \_ 0-Struktur

\[Diese Version der **RAS- \_ Port \_ 0** -Struktur wird ab Windows Vista nicht unterstützt. Verwenden Sie stattdessen den neueren [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) , der in MPRAPI. h definiert ist.\]

Die Struktur des **RAS- \_ Ports \_ 0** enthält Informationen, die einen RAS-Port beschreiben.

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

**wszportname**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Ports angibt, z. b. "COM1".

</dd> <dt>

**wszde vicetype**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Typ des Geräts angibt, auf dem die Verbindung hergestellt wurde (z. b. Modem oder ISDN). Die Liste der Gerätetypen, die in diesem Mitglied angegeben werden können, umfasst alle auf dem Server installierten Gerätetypen, einschließlich der Geräte von Drittanbietern.

</dd> <dt>

**wszdevicename**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Geräts angibt, auf dem die Verbindung hergestellt wurde, z. b. "Hayes 9600" oder "PCIMACISDN1".

</dd> <dt>

**wszmedianame**
</dt> <dd>

Gibt eine auf NULL endende Unicode-Zeichenfolge an, die den Namen des Mediums angibt, das für die Verbindung verwendet wird, z. b. *rasser* oder *RASTAPI*.

</dd> <dt>

**bleiben**
</dt> <dd>

Reserviert.

</dd> <dt>

**Flags**
</dt> <dd>

Gibt einen Satz von Bitflags an, die die Art der Verbindung angeben, die auf diesem Port hergestellt wird. Dieser Member kann eine Kombination der folgenden Flags sein.



| Wert                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**Gateway \_ aktiv**</dt> </dl>             | Wenn dieses Flag festgelegt ist, ist das NetBIOS-Gateway auf dem Server aktiv.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**Messenger \_ vorhanden**</dt> </dl>    | Wenn dieses Flag festgelegt ist, wird der Messenger-Dienst auf dem Remote Client ausgeführt.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**Port ( \_ multiverknüpft)**</dt> </dl>       | Wenn dieses Flag festgelegt ist, wird der Port mehrfach mit anderen Ports verknüpft. Verwenden Sie diese Informationen, um den Verbindungsstatus als mehrfach verknüpften Port anzuzeigen. <br/> Bei einem mehrfach verknüpften Port enthält die Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) zwei Sätze von Statistiken: eine für den Port allein und eine für die kombinierten Ports in der Verbindung mit mehreren Links.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**PPP- \_ Client**</dt> </dl>                         | Wenn dieses Flag festgelegt ist, stellt der Remote Client eine Verbindung mit PPP her. Wenn dieses Flag nicht festgelegt ist, ist der Remote Client über das AMB-Protokoll verbunden.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**Remote \_ Überwachung**</dt> </dl>                | Wenn dieses Flag festgelegt ist, wird der remotelisten-Parameter des NetBIOS-Gateways auf dem Server auf 1 festgelegt.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**Benutzer \_ authentifiziert**</dt> </dl> | Wenn dieses Flag festgelegt ist, wird ein Remote Client mit dem Server verbunden, und der Benutzer wurde authentifiziert. Aktivieren Sie dieses Flag, um sicherzustellen, dass ein Client tatsächlich mit einem Port verbunden ist.<br/>                                                                                                                                                                                                   |



 

\_ \_ \_ Verwenden Sie den Messenger-Dienst, um eine administrative Nachricht an den Remote Client zu senden, wenn der Messenger vorhanden ist, das Gateway aktiv ist und die remoteüberwachungsflags festgelegt sind. Wenn Messenger \_ vorhanden ist und Remote Überwachung \_ festgelegt ist, das Gateway jedoch \_ nicht aktiv ist, senden Sie Nachrichten nur von dem RAS-Server, mit dem der Client verbunden ist, an den Client.

</dd> <dt>

**wszUserName**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Remote Benutzers angibt, der mit diesem Port verbunden ist.

</dd> <dt>

**wszcomputer**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Remote Client Computers angibt.

</dd> <dt>

**dwstarungessiontime**
</dt> <dd>

Gibt die Zeit in Sekunden ab dem 1. Januar 1970 an, die der Client mit dem RAS-Server auf diesem Port verbunden hat. Verwenden Sie die Standardzeit Funktionen, um diesen Wert für die Anzeige zu formatieren.

</dd> <dt>

**wszlogondomain**
</dt> <dd>

Gibt eine NULL-terminierte Unicode-Zeichenfolge an, die den Namen der Domäne angibt, in der der Remote Benutzer authentifiziert wurde. Diese Zeichenfolge ist nur der Domänen Name und ohne das \\ \\ Präfix "".

</dd> <dt>

**"f"-Server**
</dt> <dd>

Gibt ein Flag an, das ungleich 0 (null) ist, wenn der diesem Port zugeordnete RAS-Server ein erweiterter Server wie Windows 2000 Advanced Server ist. Verwenden Sie diese Informationen, um den Namen des Servers zu ermitteln, der über die Benutzerkonten Datenbank verfügt. Wenn der RAS-Server ein erweiterter Server ist, erhalten Sie den Namen des Benutzerkonto Servers, indem Sie das Präfix "" mit dem Namen verketten, der \\ \\ im **wszlogondomain** -Member zurückgegeben wird. Dies liegt daran, dass für einen erweiterten Server der Name der lokalen Anmelde Domäne mit dem Servernamen identisch ist. Wenn es sich bei dem RAS-Server um eine Arbeitsstation handelt, verwenden Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion, um den Namen des Benutzerkonto Servers abzurufen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RAS- \_ Port \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md)
</dt> <dt>

[**Rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**Rasadminportenum**](rasadminportenum.md)
</dt> </dl>

 

 





