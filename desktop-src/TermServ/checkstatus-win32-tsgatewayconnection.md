---
title: CheckStatus-Methode der Win32_TSGatewayConnection-Klasse
description: Überprüft den Status einer Remotedesktop Gateway-Serververbindung (RD-Gateway) mit einem anderen Computer und bestimmt, ob der Zielcomputer für den Lastenausgleich konfiguriert ist.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- CheckStatus-Methode Remotedesktopdienste
- CheckStatus-Methode Remotedesktopdienste , Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste , CheckStatus-Methode
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
ms.openlocfilehash: c1056bbbd072a22310aa1c01cc92064819f13577018ed24c46e747f9a86b3566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942167"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>CheckStatus-Methode der Win32 \_ TSGatewayConnection-Klasse

Überprüft den Status einer Remotedesktop Gateway-Serververbindung (RD-Gateway) mit einem anderen Computer und bestimmt, ob der Zielcomputer für den Lastenausgleich konfiguriert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerName* \[ In\]
</dt> <dd>

Der Name des RD-Quellgatewayservers, von dem aus die Verbindung überprüft wird.

</dd> <dt>

*EndPointName* \[ In\]
</dt> <dd>

Der Name des Zielservers (endpunkt), auf den der Zugriff vom Quellserver aus überprüft wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden möglichen Rückgabewerte zurück.

<dl> <dt>


</dt> <dd>

0

Der Verbindungsstatus ist OK. Der Endpunkt ist erreichbar und für den Lastenausgleich konfiguriert.

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

Ein Statusfehler ist aufgetreten. Der Endpunkt ist erreichbar, aber der RPC/HTTP-Lastenausgleichsdienstdienst (RPCHTTPLBS) wird auf dem Zielcomputer nicht gestartet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

