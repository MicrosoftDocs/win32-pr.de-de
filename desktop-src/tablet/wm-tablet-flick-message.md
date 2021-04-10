---
description: Wird gesendet, wenn ein Benutzer einen Stift Flick ausführt. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: WM_TABLET_FLICK Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214552"
---
# <a name="wm_tablet_flick-message"></a>WM- \_ Tablet \_ Flick-Nachricht

Wird gesendet, wenn ein Benutzer einen Stift Flick ausführt. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine [**Flick \_ Datenstruktur**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) , die Informationen über den aufgetretenen Stift Flick enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Die [**flimapointstruktur \_**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) , die angibt, wo der Stift flicke aufgetreten ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei einem Stift-Flick handelt es sich um eine unidirektionale Stift Bewegung, bei der der Benutzer sich bei einer schnellen, geraden Bewegung an den Digitalisierer wenden muss. Ein Flick ist durch hohe Geschwindigkeit und einen hohen Grad an Genauigkeit gekennzeichnet. Ein Flick wird durch seine Richtung identifiziert. Flicks können in acht Richtungen erstellt werden, die den Haupt-und sekundären Kompass Richtungen entsprechen.

Wenn ein Stift-Flick auftritt, benachrichtigt Windows zunächst eine Anwendung, indem er eine **WM- \_ Tablet- \_** Pass-Nachricht sendet, die ein Fenster über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion empfängt. Gibt die in [Flicks-Konstanten](flicks-constants.md)beschriebene **Maske-Maske- \_ \_ \_ Maske** zurück, die angibt, dass die Anwendung auf die **WM- \_ Tablet \_** -Nachricht geantwortet hat. Wenn die Anwendung keine " **Flick- \_ WM \_ behandelte \_ Maske**" zurückgibt, führt Windows die in der schnelle Stift Bewegungen-Systemsteuerung angegebene Standardaktion aus, indem eine nach Verfolgungs Benachrichtigung gesendet wird, wie z. b. [**WM \_ appcommand**](../inputdev/wm-appcommand.md), [**WM \_ VScroll**](../controls/wm-vscroll.md)oder [**WM \_ KeyDown**](../inputdev/wm-keydown.md), je nachdem, welche Aktion dem Stift Flick zugeordnet ist.

Gehen Sie bei der Behandlung der **WM- \_ Tablet \_ Flick** -Nachricht vorsichtig vor. **WM \_ Tablet \_ Flick** wird über die [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion übergeben. Wenn Sie Methoden für eine COM-Schnittstelle aufzurufen, muss sich dieses Objekt innerhalb desselben Prozesses befinden. Andernfalls löst com eine Ausnahme aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Flick \_ Datenstruktur**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**WM- \_ Tablet \_ Flick-Nachricht**](wm-tablet-flick-message.md)
</dt> <dt>

[Gesten schnelle Stift Bewegungen](flicks-gestures.md)
</dt> <dt>

[reagieren auf Pen-schnelle Stift Bewegungen](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
