---
title: SetFallbackPrintDriverType-Methode der Win32_TerminalServiceSetting-Klasse
description: Die SetFallbackPrintDriverType-Methode legt die FallbackPrintDriverType-Eigenschaft für die -Klasse fest.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- SetFallbackPrintDriverType-Methode Remotedesktopdienste
- SetFallbackPrintDriverType-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , SetFallbackPrintDriverType-Methode
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
ms.openlocfilehash: d39033a34c75ea94f365ae690b1ac6fe4cd61663e9cd6db19f2cd2c232bd8c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137863"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>SetFallbackPrintDriverType-Methode der Win32 \_ TerminalServiceSetting-Klasse

Die **SetFallbackPrintDriverType-Methode** legt die **FallbackPrintDriverType-Eigenschaft** für die -Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FallbackPrintDriverType* \[ In\]
</dt> <dd>

Legt die **FallbackPrintDriverType-Eigenschaft** fest, die neue Remotedesktopdienste Verbindungen zulässt oder ablehnt.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Keine Fallbacktreiber.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Beste Schätzung.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Beste Schätzung. Wenn keine Übereinstimmung gefunden wird, wird ein Fallback auf Hewlett-Packard Printer Control Language (PCL) angezeigt.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Beste Schätzung. Wenn keine Übereinstimmung gefunden wird, fallbacken Sie auf Postscript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Beste Schätzung. Wenn keine Übereinstimmung gefunden wird, zeigen Sie sowohl PS- als auch PCL-Treiber an.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

