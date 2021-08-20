---
title: SetTSRedirectorMode-Methode der Win32_TSSessionDirectory Klasse
description: Legt den Wert fest, um anzugeben, ob der Server als Remotedesktopdienste fungieren soll.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- SetTSRedirectorMode-Remotedesktopdienste
- SetTSRedirectorMode-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory klasse Remotedesktopdienste , SetTSRedirectorMode-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6350d4b9a4858991616d45eb2b1092fe406c59b55b11c494a7f19be53dbb60ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127276"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a>SetTSRedirectorMode-Methode der Win32 \_ TSSessionDirectory-Klasse

Legt den Wert fest, um anzugeben, ob der Server als Remotedesktopdienste fungieren soll.

## <a name="syntax"></a>Syntax


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TSRedirValue* \[ In\]
</dt> <dd>

Typ: **uint32**

Gibt an, ob der Server als Remotedesktopdienste fungieren soll. Dies kann einer der folgenden Werte sein.

<dt>

0
</dt> <dd>

Der Server wird als Remotedesktopdienste fungieren.

</dd> <dt>

1
</dt> <dd>

Der Server wird nicht als Remotedesktopdienste fungieren.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

