---
title: InitialProgram-Methode der Win32_TSEnvironmentSetting-Klasse
description: Mit der InitialProgram-Methode werden Start Programm Eigenschaften wie Name, Arbeitsverzeichnis und Pfad des Programms so festgelegt, dass Sie sofort nach der Anmeldung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) gestartet werden.
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- InitialProgram-Methode Remotedesktopdienste
- InitialProgram-Methode Remotedesktopdienste, Win32_TSEnvironmentSetting-Klasse
- Win32_TSEnvironmentSetting-Klasse Remotedesktopdienste, InitialProgram-Methode
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337508"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>InitialProgram-Methode der Win32- \_ Klasse tsenvironmentsetting

Mit der **InitialProgram** -Methode werden Start Programm Eigenschaften wie Name, Arbeitsverzeichnis und Pfad des Programms so festgelegt, dass Sie sofort nach der Anmeldung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) gestartet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Initialprogrampath* \[ in\]
</dt> <dd>

Der Name und der Pfad des Start Programms.

</dd> <dt>

*Startin* \[ in\]
</dt> <dd>

Der Pfad zum Arbeitsverzeichnis des Start Programms.

</dd> </dl>

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

 

