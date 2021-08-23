---
title: EnumAuthorizationPlugins-Methode der Win32_TSGatewayServerSettings-Klasse
description: Listet alle registrierten Autorisierungs-Plug-Ins auf.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- EnumAuthorizationPlugins-Methode Remotedesktopdienste
- EnumAuthorizationPlugins-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste , EnumAuthorizationPlugins-Methode
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
ms.openlocfilehash: 40447b6befd3042c766b4bd312619563617119b114c329867bfc3ca0b3e7bfce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574630"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>EnumAuthorizationPlugins-Methode der Win32 \_ TSGatewayServerSettings-Klasse

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

*Plug-In-Namen* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein  Zeichenfolgenarray, das die Namen der registrierten Autorisierungs-Plug-Ins empfängt.

</dd> <dt>

*CLSIDs* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein  Zeichenfolgenarray, das die CLSIDs der registrierten Autorisierungs-Plug-Ins empfängt.

</dd> <dt>

*Beschreibungen* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein  Zeichenfolgenarray, das die Beschreibungen der registrierten Autorisierungs-Plug-Ins empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

