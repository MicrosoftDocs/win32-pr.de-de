---
title: DisconnectUser-Methode der Win32_TSGatewayConnection -Klasse (Tsünthenticationengine.h)
description: Trennt alle Verbindungen des angegebenen Benutzers vom Remotedesktop Gatewayserver (RD-Gateway).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- DisconnectUser-Remotedesktopdienste
- DisconnectUser-Methode Remotedesktopdienste , Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection klasse Remotedesktopdienste , DisconnectUser-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d31c7c89d285aed576024c551b07766a7387938762d60c252dec43e491037e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130995"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>DisconnectUser-Methode der Win32 \_ TSGatewayConnection-Klasse

Trennt alle Verbindungen des angegebenen Benutzers vom Remotedesktop Gatewayserver (RD-Gateway).

## <a name="syntax"></a>Syntax


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserName* \[ In\]
</dt> <dd>

Der Benutzername im **\\** _*Domain*UserName-Format,_ dessen Verbindungen getrennt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                       |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                             |
| Header<br/>                   | <dl> <dt>Tsünthenticationengine.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

