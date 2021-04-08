---
title: Setcolortiefe-Methode der Win32_TSClientSetting-Klasse
description: Die setcolortiefe-Methode legt die colortiefe-Eigenschaft für die-Klasse fest.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Setcolortiefe-Methode Remotedesktopdienste
- Setcolortiefe-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setcolortiefe-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957055"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Setcolortiefe-Methode der Win32- \_ Klasse tsclientsetting

Die **setcolortiefe** -Methode legt die **colortiefe** -Eigenschaft für die-Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Colortiefe* \[ in\]
</dt> <dd>

Der neue Wert für die **colortiefe** -Eigenschaft.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

8 Bits pro Pixel

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

15 Bits pro Pixel

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

16 Bits pro Pixel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 Bits pro Pixel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5@@**


</dt> <dd>

32 Bits pro Pixel

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

[**Win32- \_ tsclientsetting**](win32-tsclientsetting.md)
</dt> </dl>

 

