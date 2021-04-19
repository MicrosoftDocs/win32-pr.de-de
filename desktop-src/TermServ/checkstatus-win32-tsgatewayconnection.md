---
title: CheckStatus-Methode der Win32_TSGatewayConnection-Klasse
description: Hiermit wird der Status einer Remotedesktop Gateway-Server Verbindung (RD-Gateway) zu einem anderen Computer überprüft und ermittelt, ob der Bereitstellungs Zielcomputer für den Lastenausgleich konfiguriert ist.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- CheckStatus-Methode Remotedesktopdienste
- CheckStatus-Methode Remotedesktopdienste, Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste, checkStatus-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339545"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>CheckStatus-Methode der Win32- \_ Klasse "tgatewayconnection"

Hiermit wird der Status einer Remotedesktop Gateway-Server Verbindung (RD-Gateway) zu einem anderen Computer überprüft und ermittelt, ob der Bereitstellungs Zielcomputer für den Lastenausgleich konfiguriert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* \[ in\]
</dt> <dd>

Der Name des Quell RD-Gateway Servers, von dem die Verbindung geprüft wird.

</dd> <dt>

*EndpointName* \[ in\]
</dt> <dd>

Der Name des Zielservers (der Endpunkt), auf den der Zugriff vom Quell Server aus geprüft wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden möglichen Rückgabewerte zurück.

<dl> <dt>


</dt> <dd>

0

Der Verbindungsstatus lautet "OK". Der Endpunkt ist erreichbar und für den Lastenausgleich konfiguriert.

</dd> <dt>


</dt> <dd>

1

Der Verbindungsstatus ist unbekannt. Höchstwahrscheinlich ist eine Ausnahme aufgetreten.

</dd> <dt>


</dt> <dd>

0x80075c34

Der Endpunkt ist entweder nicht erreichbar oder nicht für den Lastenausgleich konfiguriert.

</dd> <dt>


</dt> <dd>

0x80075c32

Status Fehler. Der Endpunkt ist erreichbar, aber der RPC/HTTP-Lasten Ausgleichs Dienst (rpchttplsb) wurde auf dem Bereitstellungs Zielcomputer nicht gestartet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-"- \_ gatewayconnection"**](win32-tsgatewayconnection.md)
</dt> </dl>

 

