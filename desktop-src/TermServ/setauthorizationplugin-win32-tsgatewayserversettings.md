---
title: Setauthorizationplugin-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt das aktuelle Autorisierungs-Plug-in für den Remotedesktop Gateway-Server (RD-Gateway) fest.
ms.assetid: 236c9cca-4efc-433a-8f1f-e3044e0588b3
ms.tgt_platform: multiple
keywords:
- Setauthorizationplugin-Methode Remotedesktopdienste
- Setauthorizationplugin-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setauthorizationplugin-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthorizationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdb3cb07a7c0a30e84245a2d22e383dea168247
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518173"
---
# <a name="setauthorizationplugin-method-of-the-win32_tsgatewayserversettings-class"></a>Setauthorizationplugin-Methode der Win32-Klasse "t- \_ gatewayserversettings"

Legt das aktuelle Autorisierungs-Plug-in für den Remotedesktop Gateway-Server (RD-Gateway) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAuthorizationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PluginName* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Name des neuen aktuellen Autorisierungs-Plug-ins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen die Methode [**recyclerpcapplicationpools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) aufzurufen, damit das Autorisierungs-Plug-in funktioniert.

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**Recyclerpcapplicationpools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

