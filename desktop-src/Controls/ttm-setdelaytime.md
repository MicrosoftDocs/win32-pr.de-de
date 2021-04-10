---
title: TTM_SETDELAYTIME Meldung (kommstrg. h)
description: Legt die Anfangs-, Popup-und neueinblenden Dauer für ein QuickInfo-Steuerelement fest.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Windows-Steuerelemente für TTM_SETDELAYTIME Meldung
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956483"
---
# <a name="ttm_setdelaytime-message"></a>TTM- \_ setdelta-Zeit Nachricht

Legt die Anfangs-, Popup-und neueinblenden Dauer für ein QuickInfo-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das den festzulegenden Uhrzeitwert angibt. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**ttdt- \_ autopop**</dt> </dl>       | Legen Sie den Zeitraum fest, in dem ein QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär ist. Um die autopop-Verzögerungszeit auf den Standardwert zurückzusetzen, legen Sie *LPARAM* auf-1 fest.<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**ttdt- \_ Initial**</dt> </dl>       | Legen Sie den Zeitraum fest, in dem ein Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird. Legen Sie *LPARAM* auf-1 fest, um die anfängliche Verzögerungszeit auf den Standardwert zurückzusetzen.<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**ttdt \_ erneut anzeigen**</dt> </dl>          | Legen Sie die Zeitspanne fest, die benötigt wird, bis nachfolgende QuickInfo-Fenster angezeigt werden, wenn der Zeiger von einem Tool zu einem anderen wechselt. Legen Sie *LPARAM* auf-1 fest, um die Zeit zum erneuten Anzeigen der Verzögerung auf den Standardwert zurückzusetzen.<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**ttdt \_ automatisch**</dt> </dl> | Legen Sie alle drei Verzögerungszeiten auf Standard Proportionen fest. Die autopop-Zeit ist zehnmal so oft wie die Anfangszeit, und die reshow-Zeit ist ein fünftes Mal. Wenn dieses Flag festgelegt ist, verwenden Sie einen positiven Wert von *LPARAM* , um die anfängliche Zeit in Millisekunden anzugeben. Legen Sie *LPARAM* auf einen negativen Wert fest, um alle drei Verzögerungszeiten auf ihre Standardwerte zurückzusetzen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Verzögerungszeit in Millisekunden an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Die Standard Verzögerungszeiten basieren auf der Doppelklick Zeit. Bei der standardmäßigen Doppelklick Zeit von 500 ms beträgt die anfängliche, autopop-und reshow-Verzögerungszeit 500 ms, 5000 ms bzw. 100 ms. Im folgenden Code Fragment wird die [**getdoubleclicktime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) -Funktion verwendet, um die drei Verzögerungszeiten für ein beliebiges System festzulegen.


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM \_ getdelta-Zeit**](ttm-getdelaytime.md)
</dt> </dl>

 

