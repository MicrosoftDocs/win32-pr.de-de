---
title: InitialProgram-Methode der Win32_TSEnvironmentSetting-Klasse
description: Die InitialProgram-Methode legt Eigenschaften des Startprogramms wie Name, Arbeitsverzeichnis und Pfad des Programms so fest, dass sie unmittelbar nach der Anmeldung beim Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server gestartet werden.
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- InitialProgram-Methode Remotedesktopdienste
- InitialProgram-Methode Remotedesktopdienste , Win32_TSEnvironmentSetting-Klasse
- Win32_TSEnvironmentSetting Klasse Remotedesktopdienste , InitialProgram-Methode
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
ms.openlocfilehash: 9d13aaa0e4dfb4e0d16bea89bf871a7a890c0f375fd928e70fd99aed20c003be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126993"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>InitialProgram-Methode der Win32 \_ TSEnvironmentSetting-Klasse

Die **InitialProgram-Methode** legt Eigenschaften des Startprogramms wie Name, Arbeitsverzeichnis und Pfad des Programms so fest, dass sie unmittelbar nach der Anmeldung beim Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) gestartet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InitialProgramPath* \[ In\]
</dt> <dd>

Der Name und Pfad des Startprogramms.

</dd> <dt>

*Startin* \[ In\]
</dt> <dd>

Der Pfad zum Arbeitsverzeichnis des Startprogramms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

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

 

