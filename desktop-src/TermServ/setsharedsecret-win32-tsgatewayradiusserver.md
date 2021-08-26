---
title: SetSharedSecret-Methode der Win32_TSGatewayRADIUSServer Klasse
description: Legt die SharedSecret-Eigenschaft für diesen REMOTE AUTHENTICATION DIAL-IN USER SERVICE (RADIUS)-Server fest.
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- SetSharedSecret-Remotedesktopdienste
- SetSharedSecret-Methode Remotedesktopdienste , Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer klasse Remotedesktopdienste , SetSharedSecret-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9d6c37b4826b451a932ff282b451c77aef22c91e92a6c47cd3907ce2705371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008650"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a>SetSharedSecret-Methode der Win32 \_ TSGatewayRADIUSServer-Klasse

Legt die **SharedSecret-Eigenschaft** für diesen REMOTE AUTHENTICATION DIAL-IN USER SERVICE (RADIUS)-Server fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SharedSecret* \[ In\]
</dt> <dd>

Neues gemeinsames Geheimnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

