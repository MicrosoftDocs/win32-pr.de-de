---
title: SetName-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Legt die Name-Eigenschaft für diesen RADIUS-Server (Remote Authentication Dial-In User Service fest.
ms.assetid: 2dabc6fb-7740-4039-9bbd-5b2490fe5988
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste , Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste , SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a2e24c9ba9bbdb5648da92640fe5b81361e1760deefc4c626ef7e029a40f15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009044"
---
# <a name="setname-method-of-the-win32_tsgatewayradiusserver-class"></a>SetName-Methode der Win32 \_ TSGatewayRADIUSServer-Klasse

Legt die **Name-Eigenschaft** für diesen RADIUS-Server (Remote Authentication Dial-In User Service) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Neuer Name.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

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

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

