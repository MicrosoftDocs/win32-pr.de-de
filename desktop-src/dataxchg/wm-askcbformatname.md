---
title: WM_ASKCBFORMATNAME (Winuser.h)
description: Wird von einem Zwischenablage-Viewerfenster an den Besitzer der Zwischenablage gesendet, um den Namen eines CF \_ OWNERDISPLAY-Zwischenablageformats an fordern.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME der Exchange
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe96a2ddf4e6767c083ec2e3f4e3fc61bdde902ff93ce9a162ec7e93eb5bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991240"
---
# <a name="wm_askcbformatname-message"></a>WM \_ ASKCBFORMATNAME-Nachricht

Wird von einem Zwischenablage-Viewerfenster an den Besitzer der Zwischenablage gesendet, um den Namen eines [**CF \_ OWNERDISPLAY-Zwischenablageformats**](standard-clipboard-formats.md) an fordern.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Größe des Puffers in Zeichen, auf den der *lParam-Parameter zeigt.*

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der den Formatnamen der Zwischenablage empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Als Reaktion auf diese Meldung sollte der Besitzer der Zwischenablage den Namen des Besitzeranzeigeformats in den angegebenen Puffer kopieren und die vom *wParam-Parameter* angegebene Puffergröße nicht überschreiten.

Ein Zwischenablageanzeigefenster sendet diese Meldung an den Besitzer der Zwischenablage, um den Namen des [**CF \_ OWNERDISPLAY-Formats**](standard-clipboard-formats.md) zu bestimmen, z. B. um ein Menü mit verfügbaren Formaten zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über die Zwischenablage](clipboard.md)
</dt> </dl>

 

