---
title: ICM_DRAW_REALIZE Meldung (VFW. h)
description: Mit der ICM \_ Draw- \_ Meldung wird ein renderingerber benachrichtigt, seine Zeichnungs Palette beim Zeichnen zu erkennen. Sie können diese Nachricht explizit oder mithilfe des icdraw-/-Makros senden.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391826"
---
# <a name="icm_draw_realize-message"></a>ICM \_ Draw- \_ Nachricht erkennen

Mit der **ICM \_ Draw \_** -Meldung wird ein renderingerber benachrichtigt, seine Zeichnungs Palette beim Zeichnen zu erkennen. Sie können diese Nachricht explizit oder mithilfe des [**icdraw-**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) /-Makros senden.


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*HDC*
</dt> <dd>

Handle für den DC, der zum realisieren der Palette verwendet wird.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*f-Hintergrund*
</dt> <dd>

Hintergrundflag. Geben Sie **true** an, um die Palette als Hintergrundaufgabe zu erkennen, oder **false** , um die Palette im Vordergrund zu erkennen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn die Zeichnungs Palette realisiert wird, oder ICERR wird \_ nicht unterstützt, wenn die Palette, die den entkomprimierten Daten zugeordnet ist, erkannt wird.

## <a name="remarks"></a>Bemerkungen

Treiber müssen auf diese Nachricht nur reagieren, wenn sich die Zeichnungs Palette von der dekomprimierten Palette unterscheidet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





