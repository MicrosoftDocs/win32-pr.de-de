---
description: Delete&\# 8194; Die WMI-Klassenmethode löscht einen geplanten Auftrag.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Delete-Methode der Win32_ScheduledJob Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3f0269929cf7a854044e65c56080594dce7f44620099c68bb9399bd56c9b20f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504690"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a>Delete-Methode der Win32 \_ ScheduledJob-Klasse

Die **Delete** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht einen geplanten Auftrag.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Der Pfad wurde nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**Der Dienst wurde nicht gestartet.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**Andere**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ScheduledJob**](win32-scheduledjob.md)
</dt> </dl>

 

