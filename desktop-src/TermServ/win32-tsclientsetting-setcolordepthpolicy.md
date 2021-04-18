---
title: Setcolordepthpolicy-Methode der Win32_TSClientSetting-Klasse
description: Die setcolordepthpolicy-Methode legt die ColorDepthPolicy-Eigenschaft für die-Klasse fest.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Setcolordepthpolicy-Methode Remotedesktopdienste
- Setcolordepthpolicy-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setcolordepthpolicy-Methode
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
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391851"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a>Setcolordepthpolicy-Methode der Win32- \_ Klasse tsclientsetting

Die **setcolordepthpolicy** -Methode legt die **ColorDepthPolicy** -Eigenschaft für die-Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ColorDepthPolicy* \[ in\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **setcolordepthpolicy** -Eigenschaft, die angibt, ob die Einstellung für die maximale Farbe des Benutzers überschrieben werden soll.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Aktivieren Sie die-Eigenschaft.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Deaktivieren Sie die-Eigenschaft.

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

 

