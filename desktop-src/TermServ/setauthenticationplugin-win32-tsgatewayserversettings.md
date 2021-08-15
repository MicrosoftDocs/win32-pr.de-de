---
title: SetAuthenticationPlugin-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt das aktuelle Authentifizierungs-Plug-In für den Remotedesktop Gatewayserver (RD-Gateway) fest.
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- SetAuthenticationPlugin-Remotedesktopdienste
- SetAuthenticationPlugin-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings klasse Remotedesktopdienste , SetAuthenticationPlugin-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1da91b281e8a47c2663fe09f6b7f172dca8d4d246f0fe708139fe859955a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058548"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a>SetAuthenticationPlugin-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Legt das aktuelle Authentifizierungs-Plug-In für den Remotedesktop Gatewayserver (RD-Gateway) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PluginName* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Name des neuen aktuellen Authentifizierungs-Plug-Ins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen die [**RecycleRpcApplicationPools-Methode**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) aufrufen, damit das Authentifizierungs-Plug-In funktioniert.

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
</dt> <dt>

[**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

