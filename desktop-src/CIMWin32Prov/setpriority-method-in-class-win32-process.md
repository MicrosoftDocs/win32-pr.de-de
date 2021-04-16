---
description: Die SetPriority-&\# 32; Die WMI-Klassenmethode versucht, die Ausführungs Priorität des Prozesses zu ändern.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: SetPriority-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524144"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>SetPriority-Methode der Win32- \_ Prozess Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetPriority** versucht, die Ausführungs Priorität des Prozesses zu ändern.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Priorität* \[ in\]
</dt> <dd>

Neue Prioritäts Klasse für den Prozess. Beachten Sie, dass sich diese Werte von denen unterscheiden, die in der **Priority** -Eigenschaft des [**Win32- \_ Prozesses**](win32-process.md)explizit angegeben sind

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>Im **Leerlauf** (64)


</dt> <dd>

Wird für einen Prozess mit Threads angegeben, die nur ausgeführt werden, wenn sich das System im Leerlauf befindet. Die Threads des Prozesses werden von den Threads eines Prozesses, der in einer höheren Prioritäts Klasse ausgeführt wird, z. b. einem Bildschirmschoner, vorzeitig entfernt. Die Klasse mit der inaktiven Priorität wird von untergeordneten Prozessen geerbt.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>Niedriger als **Normal** (16384)


</dt> <dd>

Gibt einen Prozess an, der über eine Priorität oberhalb der inaktiven Prioritäts **\_ \_ Klasse**, aber unterhalb der **normalen \_ Prioritäts \_ Klasse**

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Wird für einen Prozess ohne besondere Planungsanforderungen angegeben.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Höher als normal** (32768)


</dt> <dd>

Gibt einen Prozess mit Priorität oberhalb der **normalen \_ Prioritäts \_ Klasse** an, aber unterhalb der **\_ \_ Klasse mit hoher Priorität**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Hohe Priorität** (128)


</dt> <dd>

Wird für einen Prozess angegeben, der zeitkritische Aufgaben ausführt, die sofort ausgeführt werden müssen. Die Threads des Prozesses haben Vorrang vor den Threads von Prozessen in den Prioritätsklassen mit normaler oder Leerlaufpriorität. Ein Beispiel hierfür ist die Aufgabenliste, die beim Aufrufen durch den Benutzer schnell reagieren muss, unabhängig von der Last des Betriebssystems. Verwenden Sie extrem Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, da eine Klasse mit hoher Priorität fast alle verfügbaren CPU-Zeit verwenden kann.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)


</dt> <dd>

Wird für einen Prozess mit der höchsten möglichen Priorität angegeben. Die Threads des Prozesses haben Vorrang vor den Threads aller anderen Prozesse, einschließlich der Betriebssystem Prozesse, von denen wichtige Aufgaben ausgeführt werden. Beispielsweise kann ein echt Zeit Prozess, der für mehr als ein sehr kurzes Intervall ausgeführt wird, dazu führen, dass Datenträger Caches nicht geleert werden oder die Maus nicht reagiert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unzureichende Berechtigungen** (3)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

Der **Pfad wurde nicht gefunden** (9).
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Sonstige** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Um die Priorität auf "Realtime" festzulegen, muss der Aufrufer über die Berechtigung " **seinkreasebasepriorityprivilege** " (**SE \_ Inc \_ Base \_ priority \_**) verfügen. Ohne diese Berechtigung kann die höchste Priorität auf "hohe Priorität" festgelegt werden.

## <a name="examples"></a>Beispiele

Das Beispiel [Ändern der Priorität eines laufenden Prozesses](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript ändert die Priorität einer laufenden Instanz von Notepad.exe von normal auf höher.

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

 

