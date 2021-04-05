---
title: Enumauthorizationplugins-Methode der Win32_TSGatewayServerSettings-Klasse
description: Listet alle registrierten Autorisierungs-Plug-Ins auf.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Enumauthorizationplugins-Methode Remotedesktopdienste
- Enumauthorizationplugins-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enumauthorizationplugins-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d955c08f5e4f91547751b0f177681ad2abd57c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859297"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Enumauthorizationplugins-Methode der Win32-Klasse "t- \_ gatewayserversettings"

Listet alle registrierten Autorisierungs-Plug-Ins auf.

## <a name="syntax"></a>Syntax


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pluginnames* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein **Zeichen** folgen Array, das die Namen der registrierten Autorisierungs-Plug-ins empfängt.

</dd> <dt>

*CLSIDs* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein **Zeichen** folgen Array, das die CLSIDs der registrierten Autorisierungs-Plug-ins empfängt.

</dd> <dt>

*Beschreibungen* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein **Zeichen** folgen Array, das die Beschreibungen der registrierten Autorisierungs-Plug-ins empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

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
</dt> </dl>

 

