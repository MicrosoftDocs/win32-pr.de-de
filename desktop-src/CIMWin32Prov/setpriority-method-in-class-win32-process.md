---
description: SetPriority&\# 32; Die WMI-Klassenmethode versucht, die Ausführungspriorität des Prozesses zu ändern.
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
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675569"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>SetPriority-Methode der Win32 \_ Process-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** versucht, die Ausführungspriorität des Prozesses zu ändern.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Priorität* \[ In\]
</dt> <dd>

Neue Prioritätsklasse für den Prozess. Beachten Sie, dass sich diese Werte von denen unterscheiden, die explizit in der **Priority-Eigenschaft** von [**Win32 \_ Process**](win32-process.md)angegeben sind.

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Leerlauf** (64)


</dt> <dd>

Wird für einen Prozess mit Threads angegeben, die nur ausgeführt werden, wenn sich das System im Leerlauf befindet. Die Threads des Prozesses werden durch die Threads eines Prozesses vorzeitig beendet, der in einer Klasse mit höherer Priorität ausgeführt wird, z. B. einem Bildschirmschoner. Die Klasse mit Leerlaufpriorität wird von untergeordneten Prozessen geerbt.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>Below Normal (16384) **(Unter normal** (16384))


</dt> <dd>

Gibt einen Prozess an, der **prioritätsüber IDLE \_ PRIORITY \_ CLASS**, aber unter **NORMAL PRIORITY CLASS \_ \_ verfügt.**

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Wird für einen Prozess ohne besondere Planungsanforderungen angegeben.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Über Normal** (32768)


</dt> <dd>

Gibt einen Prozess an, der prioritätsmäßig über **NORMAL \_ PRIORITY \_ CLASS**, aber **unterHALB von HIGH PRIORITY CLASS \_ \_ verfügt.**

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Hohe Priorität** (128)


</dt> <dd>

Wird für einen Prozess angegeben, der zeitkritische Aufgaben ausführt, die sofort ausgeführt werden müssen. Die Threads des Prozesses haben Vorrang vor den Threads von Prozessen in den Prioritätsklassen mit normaler oder Leerlaufpriorität. Ein Beispiel ist die Aufgabenliste, die beim Aufruf durch den Benutzer schnell reagieren muss, unabhängig von der Auslastung des Betriebssystems. Verwenden Sie äußerste Sorgfalt bei der Verwendung der Klasse mit hoher Priorität, da eine Anwendung mit hoher Priorität fast die gesamte verfügbare CPU-Zeit nutzen kann.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Echtzeit** (256)


</dt> <dd>

Wird für einen Prozess mit der höchsten möglichen Priorität angegeben. Die Threads des Prozesses sind den Threads aller anderen Prozesse voraus, einschließlich Betriebssystemprozessen, die wichtige Aufgaben ausführen. Beispielsweise kann ein Echtzeitprozess, der für mehr als ein sehr kurzes Intervall ausgeführt wird, dazu führen, dass Datenträgercaches nicht geleert werden oder eine Maus nicht reagiert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Erfolgreicher Abschluss** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unzureichende Berechtigungen** (3)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

**Pfad nicht gefunden** (9)
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Sonstige** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Um die Priorität auf Realtime festzulegen, muss der Aufrufer **über SeIncreaseBasePriorityPrivilege** ( SE INC BASE PRIORITY PRIVILEGE )**\_ \_ \_ \_ verfügen.** Ohne diese Berechtigung kann die höchste Priorität auf "Hohe Priorität" festgelegt werden.

## <a name="examples"></a>Beispiele

Im VbScript-Beispiel [Ändern der Priorität eines ausgeführten Prozesses](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) wird die Priorität einer ausgeführten Instanz von Notepad.exe von Normal in Oberhalb von Normal geändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Win32-Prozess**](win32-process.md)
</dt> </dl>

 

