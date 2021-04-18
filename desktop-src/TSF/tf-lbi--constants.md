---
title: TF_LBI_ Konstanten (ctfutb. h)
description: Die TF \_ LBI \_ \-Konstanten werden mit der itflangbaritemsink OnUpdate-Methode verwendet, um anzugeben, welche sprach leisten Elemente geändert wurden.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337726"
---
# <a name="tf_lbi_-constants"></a>TF- \_ LBI- \_ \* Konstanten

Die **tf \_ LBI \_ \** _-Konstanten werden mit der [itflangbaritemsink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) -Methode verwendet, um anzugeben, welche sprach leisten Elemente geändert wurden.



| Konstante/Wert                                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_ LBI- \_ Symbol * *</dt> <dt>0x00000001</dt> </dl>                                                        | Das Symbol des Elements wurde geändert. Die sprach Leiste ruft [itflangbaritembutton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) als Reaktion auf diese Benachrichtigung auf.<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**Tf \_ LBI- \_ Text**</dt> <dt>0x00000002</dt> </dl>                                                        | Der Text einer Schaltfläche oder eines Bitmap-Schaltflächen Elements wurde geändert. Die sprach Leiste ruft [itflangbaritembutton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) oder [itflangbaritembitmapbutton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext)auf, je nachdem, was für diese Benachrichtigung geeignet ist.<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**Tf \_ LBI \_**</dt> -QuickInfo <dt>0x00000004</dt> </dl>                                               | Der QuickInfo-Text des Elements wurde geändert. Die sprach Leiste ruft [itflangbaritem:: gettooltipstring](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) als Reaktion auf diese Benachrichtigung auf.<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**Tf \_ LBI- \_ Bitmap**</dt> <dt>0x00000008</dt> </dl>                                                  | Die Bitmap eines Bitmap-oder Bitmap-Schaltflächen Elements wurde geändert. Die sprach Leiste ruft [itflangbaritembitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) oder [itflangbaritembitmapbutton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap)auf, je nachdem, was für diese Benachrichtigung geeignet ist.<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**Tf \_ LBI \_**</dt> -Sprechblase <dt>0x00000010</dt> </dl>                                               | Die Informationen für ein Sprechblasen Element wurden geändert. Die sprach Leiste ruft [itflangbaritemballoon:: getballooninfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) als Reaktion auf diese Benachrichtigung auf.<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**Tf \_ LBI- \_ Status**</dt> <dt>0x00010000 bis</dt> </dl>                                                  | Der Element Status wurde geändert. Die sprach Leiste ruft [itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) als Reaktion auf diese Benachrichtigung auf.<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**Tf \_ LBI \_ bmpall**</dt> <dt>tf \_ LBI \_ Bitmap \| tf \_ LBI \_ TOOLTIP</dt> </dl>                          | Kombiniert TF \_ LBI \_ Bitmap und TF \_ LBI \_ TOOLTIP.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**Tf \_ LBI \_ bmpbtnall**</dt> <dt>tf \_ LBI \_ Bitmap \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt> </dl> | Kombiniert TF \_ LBI \_ Bitmap, TF \_ LBI \_ Text und TF \_ LBI \_ TOOLTIP.<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**Tf \_ LBI \_ btnall**</dt> <dt>tf \_ LBI \_ Icon \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt> </dl>            | Kombiniert TF \_ LBI \_ Icon, TF \_ LBI \_ Text und TF \_ LBI \_ TOOLTIP.<br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITF langbaritemsink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





