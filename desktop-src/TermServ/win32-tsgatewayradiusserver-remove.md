---
title: Remove-Methode der Win32_TSGatewayRADIUSServer Klasse
description: Entfernt den aktuellen Remote Authentication Dial-In User Service (RADIUS)-Server.
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Entfernen der Remotedesktopdienste
- Remove method Remotedesktopdienste , Win32_TSGatewayRADIUSServer interface
- Win32_TSGatewayRADIUSServer schnittstelle Remotedesktopdienste , Remove-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a9ea6a9f2bdb4fada3fed38952988c0284b5bc4055503784c232255586407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126574"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a>Remove-Methode der Win32 \_ TSGatewayRADIUSServer-Klasse

Entfernt den aktuellen Remote Authentication Dial-In User Service (RADIUS)-Server.

## <a name="syntax"></a>Syntax


```mof
uint32 Remove();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

