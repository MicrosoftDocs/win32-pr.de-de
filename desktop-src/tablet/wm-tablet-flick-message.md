---
description: Wird gesendet, wenn ein Benutzer einen Stiftflick ausführt. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: WM_TABLET_FLICK (Tpcshrd.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb01fce646d2e7c6cb4e1b25c2f49f0c4dde5258ba2167e117a23eff22a5d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842775"
---
# <a name="wm_tablet_flick-message"></a>WM \_ TABLET \_ FLICK-Nachricht

Wird gesendet, wenn ein Benutzer einen Stiftflick ausführt. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine [**\_ FLICK-DATENstruktur,**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) die Informationen über den aufgetretenen Stiftflick enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Die [**FLICK \_ POINT-Struktur,**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) die angibt, wo der Stiftflick aufgetreten ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Stiftflick ist eine unidirektionale Stiftbewegung, bei der der Benutzer den Digitizer in einer schnellen, geraden Bewegung kontaktieren muss. Ein Flick ist durch hohe Geschwindigkeit und einen hohen Grad an Geraden gekennzeichnet. Ein Flick wird anhand seiner Richtung identifiziert. Flicks können in acht Richtungen vorgenommen werden, die den Kardinal- und sekundären Kompassrichtungen entspricht.

Wenn ein Stiftflick auftritt, benachrichtigt Windows zunächst eine Anwendung durch Senden einer **WM \_ TABLET \_ FLICK-Nachricht,** die ein Fenster über seine [*WindowProc-Funktion*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) empfängt. Gibt die **FLICK \_ WM \_ HANDLED \_ MASK-Konstante** zurück, die unter [Flicks-Konstanten](flicks-constants.md)beschrieben ist, um anzugeben, dass die Anwendung auf die **WM TABLET \_ \_ FLICK-Nachricht geantwortet** hat. Wenn die Anwendung **FLICK \_ WM \_ HANDLED \_ MASK** nicht zurücksendet, führt Windows die in der Flicks-Systemsteuerung angegebene Standardaktion aus, indem eine Folgebenachrichtigung wie [**WM \_ APPCOMMAND,**](../inputdev/wm-appcommand.md) [**WM \_ VSCROLL**](../controls/wm-vscroll.md)oder [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md)sendet, je nachdem, welche Aktion dem Stiftflick zugeordnet ist.

Seien Sie vorsichtig, wenn Sie die **WM \_ TABLET \_ FLICK-Nachricht** behandeln. **WM \_ TABLET \_ FLICK** wird über die [**SendMessageTimeout-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) übergeben. Wenn Sie Methoden für eine COM-Schnittstelle aufrufen, muss sich dieses Objekt innerhalb desselben Prozesses finden. Wenn dies nicht der Dert ist, löst COM eine Ausnahme aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Tpcshrd.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Datenstruktur mit \_ "Flick"**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**wm \_ tablet \_ flick message**](wm-tablet-flick-message.md)
</dt> <dt>

[Gesten für Blättern](flicks-gestures.md)
</dt> <dt>

[Reagieren auf Stiftflicks](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
