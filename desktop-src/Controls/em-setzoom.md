---
title: EM_SETZOOM Meldung (RichEdit. h)
description: Legt das Zoomverhältnis fest. Das Verhältnis muss ein Wert zwischen 1/64 und 64 sein. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Windows-Steuerelemente für EM_SETZOOM Meldung
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859009"
---
# <a name="em_setzoom-message"></a>EM- \_ setzoom-Meldung

Legt das Zoomverhältnis eines mehrzeiligen Bearbeitungs Steuer Elements oder eines Rich-Edit-Steuer Elements fest. Das Verhältnis muss ein Wert zwischen 1/64 und 64 sein. Das Bearbeitungs Steuerelement muss über den erweiterten Stil des **es \_ Ex \_** -Formats verfügen, damit diese Nachricht wirksam wird. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zähler des Zoom Verhältnisses.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Nenner des Zoom Verhältnisses. Diese Parameter können die folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Beide 0**</dt> </dl>                                                                                                   | Deaktiviert das Zoomen mithilfe der EM-Datei (" **\_ setzoom** ") (das Zoomen kann weiterhin mithilfe von " [**txgetextent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)" erfolgen).<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/LPARAM) < 64**</dt> </dl> | Zoom Anzeige nach Zoomverhältnis Zähler/Nenner<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die neue Zoomeinstellung akzeptiert wird, ist der Rückgabewert " **true**".

Wenn die neue Zoomeinstellung nicht akzeptiert wird, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

**Bearbeiten:** Wird in Windows 10 1809 und höher unterstützt. Das Bearbeitungs Steuerelement muss über den erweiterten Stil des **es \_ Ex \_** -Formats verfügen, damit diese Nachricht wirksam wird. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md). Weitere Informationen zum Bearbeitungs Steuerelement finden Sie unter [Edit Controls](about-edit-controls.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h/kommctrl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getzoom**](em-getzoom.md)
</dt> </dl>

 

 





