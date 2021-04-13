---
title: Disconnectprotocol-Methode der Win32_TSGatewayConnection-Klasse
description: Trennt alle Verbindungen des angegebenen Protokolls vom Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Disconnectprotocol-Methode Remotedesktopdienste
- Disconnectprotocol-Methode Remotedesktopdienste, Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste, disconnectprotocol-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340827"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a>Disconnectprotocol-Methode der Win32- \_ Klasse "tgatewayconnection"

Trennt alle Verbindungen des angegebenen Protokolls vom Remotedesktop Gateway-Server (RD-Gateway).

## <a name="syntax"></a>Syntax


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolName* \[ in\]
</dt> <dd>

Der Protokoll Name für eine bestimmte Verbindung. Dies kann über die **ProtocolName** -Eigenschaft der Win32-Klasse " **\_ tgatewayconnection** " abgerufen werden.

<dt>

TS
</dt> <dd>

Das Protokoll für den RD-Gateway Server.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

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

 

