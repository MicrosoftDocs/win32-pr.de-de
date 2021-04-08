---
title: Setclientwallpaper-Methode der Win32_TSEnvironmentSetting-Klasse
description: Die setclientwallpaper-Methode legt die ClientWallPaper-Eigenschaft fest.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Setclientwallpaper-Methode Remotedesktopdienste
- Setclientwallpaper-Methode Remotedesktopdienste, Win32_TSEnvironmentSetting-Klasse
- Win32_TSEnvironmentSetting-Klasse Remotedesktopdienste, setclientwallpaper-Methode
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741257"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Setclientwallpaper-Methode der Win32- \_ Klasse "tsenvironmentsetting"

Die **setclientwallpaper** -Methode legt die **ClientWallPaper** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientWallPaper* \[ in\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **ClientWallPaper** -Eigenschaft, die angibt, ob das Hintergrundbild (oder Hintergrundbild) auf dem Client angezeigt wird.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Das Hintergrundbild (oder Hintergrundbild) wird auf dem Client nicht angezeigt.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Das Hintergrundbild (oder Hintergrundbild) wird auf dem Client angezeigt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

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

[**Win32- \_ tsenvironmentsetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

