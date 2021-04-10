---
title: Setfallbackprintdrivertype-Methode der Win32_TerminalServiceSetting-Klasse
description: Die setfallbackprintdrivertype-Methode legt die fallbackprintdrivertype-Eigenschaft für die-Klasse fest.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Setfallbackprintdrivertype-Methode Remotedesktopdienste
- Setfallbackprintdrivertype-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setfallbackprintdrivertype-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040930"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Setfallbackprintdrivertype-Methode der Win32 \_ terminalservicesetts-Klasse

Die **setfallbackprintdrivertype** -Methode legt die **fallbackprintdrivertype** -Eigenschaft für die-Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fallbackprintdrivertype* \[ in\]
</dt> <dd>

Legt die **fallbackprintdrivertype** -Eigenschaft fest, die neue Remotedesktopdienste Verbindungen zulässt oder ablehnt.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Keine Fall Back Treiber.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Beste Schätzung.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Beste Schätzung. Wenn keine Entsprechung gefunden wird, Fall Back auf Hewlett-Packard-druckersteuerungsprache (PCL).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Beste Schätzung. Wenn keine Entsprechung gefunden wird, Fall Back auf PostScript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Beste Schätzung. Wenn keine Entsprechung gefunden wird, zeigen Sie sowohl PS-als auch PCL-Treiber an.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

