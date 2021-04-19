---
title: Fehler Codes für die Windows-Animation (Winerror. h)
description: Wenn ein Fehler auftritt, gibt die Windows-Animation einen Code als HRESULT-Wert zurück. Dieser Abschnitt enthält eine Liste der Fehlercodes, die für die Windows-Animation spezifisch sind. Eine Liste allgemeiner com-Fehlercodes finden Sie unter COM-Fehlercodes.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342424"
---
# <a name="windows-animation-error-codes"></a>Fehler Codes für Windows-Animationen

Wenn ein Fehler auftritt, gibt die Windows-Animation einen Code als **HRESULT** -Wert zurück. Dieser Abschnitt enthält eine Liste der Fehlercodes, die für die Windows-Animation spezifisch sind. Eine Liste allgemeiner com-Fehlercodes finden Sie unter [com-Fehlercodes](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**Fehler beim Erstellen der Benutzeroberfläche. \_ \_ \_**
</dt> <dd> <dl> <dt>

0x802a0001
</dt> <dt>



Das Objekt konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**Benutzeroberfläche \_ E \_ Herunterfahren \_ aufgerufen**
</dt> <dd> <dl> <dt>

0x802a0002
</dt> <dt>



Die [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) -Methode wurde im Animations-Manager aufgerufen und bewirkt, dass der Animations-Manager heruntergefahren wurde und alle Animations Variablen und Storyboards, die für die Freigabe erstellt wurden.

> [!Note]  
> Nach dem [**herunter**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)fahren können keine Methoden für ein Animations Objekt aufgerufen werden.

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**Benutzeroberfläche \_ E unzulässig \_ \_**
</dt> <dd> <dl> <dt>

0x802a0003
</dt> <dt>



Diese Methode kann während dieser Art von Rückruf nicht aufgerufen werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI- \_ E- \_ Objekt \_ versiegelt**
</dt> <dd> <dl> <dt>

0x802a0004
</dt> <dt>



Dieses Objekt wurde versiegelt, sodass diese Änderung nicht mehr zulässig ist.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_E/a- \_ Wert \_ nicht \_ festgelegt**
</dt> <dd> <dl> <dt>

0x802a0005
</dt> <dt>



Der angeforderte Wert wurde nie festgelegt und kann daher nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_E/a-Wert wurde \_ \_ nicht \_ bestimmt**
</dt> <dd> <dl> <dt>

0x802a0006
</dt> <dt>



Der angeforderte Wert kann nicht bestimmt werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**Benutzeroberfläche \_ E \_ ungültige \_ Ausgabe**
</dt> <dd> <dl> <dt>

0x802a0007
</dt> <dt>



Ein Rückruf hat einen ungültigen Ausgabeparameter zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI \_ E \_ boolescher Wert \_ erwartet**
</dt> <dd> <dl> <dt>

0x802a0008
</dt> <dt>



Ein Rückruf hat einen anderen Erfolgs Code als s "OK" oder "false" zurückgegeben \_ \_ .


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**Benutzeroberfläche \_ E, \_ anderer \_ Besitzer**
</dt> <dd> <dl> <dt>

0x802a0009
</dt> <dt>



Ein Parameter, dessen Besitzer dieses-Objekt sein sollte, ist im Besitz eines anderen-Objekts.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_mehrdeutige UI E- \_ \_ Match**
</dt> <dd> <dl> <dt>

0x802a000a
</dt> <dt>



Es wurden mehrere Elemente mit den Suchkriterien übereinstimmen.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI \_ E \_ FP- \_ Überlauf**
</dt> <dd> <dl> <dt>

0x802a000b
</dt> <dt>



Ein Gleit Komma Überlauf ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI \_ E \_ falscher \_ Thread**
</dt> <dd> <dl> <dt>

0x802a000c
</dt> <dt>



Diese Methode kann nur von dem Thread aufgerufen werden, der das Objekt erstellt hat.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI \_ E \_ Storyboard \_ aktiv**
</dt> <dd> <dl> <dt>

0x802a0101
</dt> <dt>



Das Storyboard befindet sich zurzeit im Zeitplan.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI \_ E \_ Storyboard wird \_ nicht \_ abgespielt**
</dt> <dd> <dl> <dt>

0x802a0102
</dt> <dt>



Das Storyboard wird nicht abgespielt.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI \_ E \_ \_ Keyframe \_ nach \_ Ende starten**
</dt> <dd> <dl> <dt>

0x802a0103
</dt> <dt>



Der Keyframe "Start" kann nach dem endend-Keyframe auftreten.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**E-End-Keyframe der Benutzeroberfläche \_ \_ \_ \_ nicht \_ bestimmt**
</dt> <dd> <dl> <dt>

0x802a0104
</dt> <dt>



Es ist möglicherweise nicht möglich, die Endzeit des Keyframes zu ermitteln, wenn der Start-Keyframe erreicht wird.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI- \_ E- \_ Schleifen \_ überlappend**
</dt> <dd> <dl> <dt>

0x802a0105
</dt> <dt>



Zwei wiederholte Teile eines Storyboards können sich überlappen.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI- \_ E- \_ Übergang \_ \_ wird bereits verwendet**
</dt> <dd> <dl> <dt>

0x802a0106
</dt> <dt>



Der Übergang wurde bereits einem anderen Storyboard hinzugefügt oder wurde einem Storyboard hinzugefügt, das die Wiedergabe abgeschlossen hat und freigegeben wurde.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI- \_ E- \_ Übergang \_ nicht \_ im \_ Storyboard**
</dt> <dd> <dl> <dt>

0x802a0107
</dt> <dt>



Der Übergang wurde keinem Storyboard hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**Übertragung der UI \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x802a0108
</dt> <dt>



Der Übergang könnte den Anfang eines anderen Übergangs im Storyboard in Eclipse übertragen.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI \_ E \_ Zeit \_ vor dem \_ letzten \_ Update**
</dt> <dd> <dl> <dt>

0x802a0109
</dt> <dt>



Die angegebene Zeit ist älter als die Zeit, die an das letzte Update weitergegeben wurde.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI- \_ E-Timer-Client ist \_ \_ \_ bereits \_ verbunden**
</dt> <dd> <dl> <dt>

0x802a010a
</dt> <dt>



Dieser Client ist bereits mit einem Timer verbunden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista und Platt Form Update für Windows Vista \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz zur Windows-Animation](windows-animation-reference.md)
</dt> </dl>

 

