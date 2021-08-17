---
title: MoveDown-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Verschiebt diesen RADIUS-Server (Remote Authentication Dial-In User Service) um eine Position nach unten in der Prioritätsreihenfolge.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- MoveDown-Methode Remotedesktopdienste
- MoveDown-Methode Remotedesktopdienste , Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer Klasse Remotedesktopdienste , MoveDown-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acee402af28ed62c5f4627972b083d1fd5c3ed7f49b02a058fb4f2562ffbd681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138165"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a>MoveDown-Methode der Win32 \_ TSGatewayRADIUSServer-Klasse

Verschiebt diesen RADIUS-Server (Remote Authentication Dial-In User Service) um eine Position nach unten in der Prioritätsreihenfolge. Diese Methode erhöht die **Priority-Eigenschaft** des aktuellen RADIUS-Servers und dekrementiert die **Priority-Eigenschaft** des RADIUS-Servers, der dem aktuellen RADIUS-Server folgt.

## <a name="syntax"></a>Syntax


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

