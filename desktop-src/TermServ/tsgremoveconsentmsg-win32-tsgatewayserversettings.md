---
title: TSGRemoveConsentMsg-Methode der Win32_TSGatewayServerSettings-Klasse
description: Entfernt die Verwaltungsmeldung für den Gatewayserver. | TSGRemoveConsentMsg-Methode der Win32_TSGatewayServerSettings-Klasse
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.tgt_platform: multiple
keywords:
- TSGRemoveConsentMsg-Remotedesktopdienste
- TSGRemoveConsentMsg-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , TSGRemoveConsentMsg-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee41bc88a653cd1529b94d2c939b77dd112591bd42e5f001e4fe5742bb3f92e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755992"
---
# <a name="tsgremoveconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a>TSGRemoveConsentMsg-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Entfernt die Verwaltungsmeldung für den Gatewayserver.

## <a name="syntax"></a>Syntax


```mof
uint32 TSGRemoveConsentMsg();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

