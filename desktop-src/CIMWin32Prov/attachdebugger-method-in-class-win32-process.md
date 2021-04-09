---
description: Startet den Debugger, der derzeit für diesen Prozess registriert ist.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: AttachDebugger-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860768"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>AttachDebugger-Methode der Win32- \_ Prozess Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode " **AttachDebugger** " startet den Debugger, der derzeit für diesen Prozess registriert ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss**
</dt> <dd>

0

Erfolgreicher Abschluss.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.

</dd> <dt>

**Unzureichende Berechtigungen**
</dt> <dd>

3

Der Benutzer verfügt nicht über ausreichende Berechtigungen.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Unbekannter Fehler.

</dd> <dt>

**Der Pfad wurde nicht gefunden**
</dt> <dd>

9

Der angegebene Pfad ist nicht vorhanden.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Der angegebene Parameter ist ungültig.

</dd> <dt>

**Andere**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Prozess**](win32-process.md)
</dt> </dl>

 

