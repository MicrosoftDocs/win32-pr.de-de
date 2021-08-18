---
title: SetColorDepth-Methode der Win32_TSClientSetting-Klasse
description: Die SetColorDepth-Methode legt die ColorDepth-Eigenschaft für die -Klasse fest.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- SetColorDepth-Methode Remotedesktopdienste
- SetColorDepth-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , SetColorDepth-Methode
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
ms.openlocfilehash: da2c7f31ef04fdfb9dcbfee5e1ca3dcec1386a7dbd0c20824b00bdfe41ac6d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999860"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>SetColorDepth-Methode der Win32 \_ TSClientSetting-Klasse

Die **SetColorDepth-Methode** legt die **ColorDepth-Eigenschaft** für die -Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ColorDepth* \[ In\]
</dt> <dd>

Der neue Wert für die **ColorDepth-Eigenschaft.**

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

<span id="3"></span>**3**


</dt> <dd>

16 Bits pro Pixel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 Bits pro Pixel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

32 Bits pro Pixel

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

