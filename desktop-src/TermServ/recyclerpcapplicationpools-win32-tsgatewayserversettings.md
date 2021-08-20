---
title: RecycleRpcApplicationPools-Methode der Win32_TSGatewayServerSettings Klasse
description: Verwendet die RPC-Anwendungspools in IIS wieder.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- RecycleRpcApplicationPools-Remotedesktopdienste
- RecycleRpcApplicationPools-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , RecycleRpcApplicationPools-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03be03b67e0e6e5c40c73624a08d8a8898022e73f1c716085eefe456f3623d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127927"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a>RecycleRpcApplicationPools-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Verwendet die RPC-Anwendungspools in IIS wieder.

## <a name="syntax"></a>Syntax


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Das Aufrufen dieser Methode führt dazu, dass alle vorhandenen Verbindungen getrennt werden.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

