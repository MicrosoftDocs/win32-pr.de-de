---
title: Windows Animationsfehlercodes (Winerror.h)
description: Wenn ein Fehler auftritt, gibt Windows Animation einen Code als HRESULT-Wert zurück. Dieser Abschnitt enthält eine Liste der Fehlercodes, die für Windows Animation spezifisch sind. Eine Liste der allgemeinen COM-Fehlercodes finden Sie unter COM-Fehlercodes.
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
ms.openlocfilehash: 44d725874de9c511558cef6ebbe8652905a7f5dac6372230385eaa3253ba3454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513660"
---
# <a name="windows-animation-error-codes"></a>Windows Animationsfehlercodes

Wenn ein Fehler auftritt, gibt Windows Animation einen Code als **HRESULT-Wert** zurück. Dieser Abschnitt enthält eine Liste der Fehlercodes, die für Windows Animation spezifisch sind. Eine Liste der allgemeinen COM-Fehlercodes finden Sie unter [COM-Fehlercodes.](/windows/desktop/com/com-error-codes)

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI \_ E \_ CREATE \_ FAILED**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



Das Objekt konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI \_ E \_ SHUTDOWN \_ CALLED**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



Die [**Shutdown-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) wurde für den Animations-Manager aufgerufen, wodurch der Animations-Manager heruntergefahren und alle erstellten Animationsvariablen und Storyboards freigegeben werden.

> [!Note]  
> Nach [**dem Herunterfahren**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)können keine Methoden für ein Animationsobjekt aufgerufen werden.

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI \_ E \_ ILLEGAL \_ REENTRANCY**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



Diese Methode kann während dieser Art von Rückruf nicht aufgerufen werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI \_ E \_ OBJECT \_ SEALED**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Dieses Objekt wurde versiegelt, sodass diese Änderung nicht mehr zulässig ist.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_BENUTZEROBERFLÄCHEN-E-WERT \_ \_ NICHT \_ FESTGELEGT**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



Der angeforderte Wert wurde nie festgelegt und kann daher nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_BENUTZEROBERFLÄCHEN-E-WERT \_ \_ NICHT \_ BESTIMMT**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



Der angeforderte Wert kann nicht bestimmt werden.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI \_ E \_ INVALID \_ OUTPUT**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Ein Rückruf hat einen ungültigen Ausgabeparameter zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**\_UI E \_ BOOLEAN \_ ERWARTET**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Ein Rückruf hat einen anderen Erfolgscode als S \_ OK oder S FALSE \_ zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI \_ E \_ DIFFERENT \_ OWNER**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Ein Parameter, der sich im Besitz dieses Objekts befinden soll, befindet sich im Besitz eines anderen -Objekts.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI \_ E \_ \_ MEHRDEUTIGE ÜBEREINSTIMMUNG**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Mehrere Elemente stimmten mit den Suchkriterien überein.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI \_ E \_ FP \_ OVERFLOW**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Ein Gleitkommaüberlauf ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI \_ E \_ WRONG \_ THREAD**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Diese Methode kann nur aus dem Thread aufgerufen werden, der das Objekt erstellt hat.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI \_ E \_ STORYBOARD \_ ACTIVE**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



Das Storyboard befindet sich derzeit im Zeitplan.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI E STORYBOARD NOT PLAYING (UI \_ E \_ STORYBOARD WIRD NICHT \_ \_ WIEDERGEGEBEN)**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



Das Storyboard wird nicht wiedergegeben.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI \_ E \_ START \_ KEYFRAME \_ AFTER \_ END**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



Der Startschlüsselrahmen kann nach dem Ende des Keyframes auftreten.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI \_ E \_ END \_ KEYFRAME \_ NOT \_ DETERMINED**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Es ist möglicherweise nicht möglich, die Endzeit des Keyframes zu bestimmen, wenn der Startschlüsselrahmen erreicht wird.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_ \_ ÜBERLAPPENDE E-SCHLEIFEN DER BENUTZEROBERFLÄCHE \_**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Zwei wiederholte Teile eines Storyboards können sich überlappen.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**\_BENUTZEROBERFLÄCHEN-E-ÜBERGANG \_ \_ BEREITS \_ VERWENDET**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



Der Übergang wurde bereits einem anderen Storyboard oder einem Storyboard hinzugefügt, das die Wiedergabe abgeschlossen und veröffentlicht hat.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**\_BENUTZEROBERFLÄCHEN-E-ÜBERGANG \_ \_ NICHT IM \_ \_ STORYBOARD**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



Der Übergang wurde keinem Storyboard hinzugefügt.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI \_ E \_ TRANSITION \_ ECLIPSED**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



Der Übergang kann den Anfang eines anderen Übergangs im Storyboard verfinsteren.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI \_ E \_ TIME \_ BEFORE \_ LAST \_ UPDATE**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



Die angegebene Zeit liegt vor der Zeit, die an das letzte Update übergeben wurde.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI \_ E \_ TIMER \_ CLIENT \_ ALREADY \_ CONNECTED**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Dieser Client ist bereits mit einem Timer verbunden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista und Plattformupdate nur für Windows \[ Vista-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Winerror.h</dt> </dl>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Referenz zu Animationen](windows-animation-reference.md)
</dt> </dl>

 

