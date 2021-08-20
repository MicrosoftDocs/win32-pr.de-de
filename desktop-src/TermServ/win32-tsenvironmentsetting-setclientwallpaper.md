---
title: SetClientWallPaper-Methode der Win32_TSEnvironmentSetting-Klasse
description: Die SetClientWallPaper-Methode legt die ClientWallPaper-Eigenschaft fest.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- SetClientWallPaper-Methode Remotedesktopdienste
- SetClientWallPaper-Methode Remotedesktopdienste , Win32_TSEnvironmentSetting-Klasse
- Win32_TSEnvironmentSetting Klasse Remotedesktopdienste , SetClientWallPaper-Methode
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
ms.openlocfilehash: c6b314148bf630dace88c08b532cf80d2bed68d9e41f5566a198a79eef6e52a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126854"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>SetClientWallPaper-Methode der Win32 \_ TSEnvironmentSetting-Klasse

Die **SetClientWallPaper-Methode** legt die **ClientWallPaper-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientWallPaper* \[ In\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **ClientWallPaper-Eigenschaft,** die angibt, ob das Hintergrundbild (oder Hintergrundbild) auf dem Client angezeigt wird.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Das Hintergrundbild (oder Hintergrundbild) wird auf dem Client nicht angezeigt.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Das Hintergrundbild (oder Hintergrundbild) wird auf dem Client angezeigt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

