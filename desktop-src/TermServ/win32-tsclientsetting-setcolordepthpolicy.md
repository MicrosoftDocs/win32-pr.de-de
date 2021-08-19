---
title: SetColorDepthPolicy-Methode der Win32_TSClientSetting-Klasse
description: Die SetColorDepthPolicy-Methode legt die ColorDepthPolicy-Eigenschaft für die -Klasse fest.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- SetColorDepthPolicy-Methode Remotedesktopdienste
- SetColorDepthPolicy-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , SetColorDepthPolicy-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ecb53500a65c997ace21865492a0a473c2799bd38a3876c4676aaea4120610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999840"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a>SetColorDepthPolicy-Methode der Win32 \_ TSClientSetting-Klasse

Die **SetColorDepthPolicy-Methode** legt die **ColorDepthPolicy-Eigenschaft** für die -Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ColorDepthPolicy* \[ In\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **SetColorDepthPolicy-Eigenschaft,** die angibt, ob die Maximale Farbeinstellung des Benutzers überschrieben werden soll.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Aktivieren Sie die -Eigenschaft.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Deaktivieren Sie die -Eigenschaft.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

