---
title: EM_SETZOOM (Richedit.h)
description: Legt das Zoomverhältnis fest. Das Verhältnis muss ein Wert zwischen 1/64 und 64 sein. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM meldungssteuerelemente Windows
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
ms.openlocfilehash: ecf6541bc018df253a3ed45f8bced42e2f19938449d7fc35bf7f309909d53a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437180"
---
# <a name="em_setzoom-message"></a>EM \_ SETZOOM-Nachricht

Legt das Zoomverhältnis für ein mehrteiliges Bearbeitungssteuerobjekt oder ein Rich-Edit-Steuerelement fest. Das Verhältnis muss ein Wert zwischen 1/64 und 64 sein. Für das Bearbeitungssteuerobjekt muss der erweiterte Stil **ES \_ EX \_ ZOOMABLE** festgelegt sein. Informationen dazu, dass diese Meldung wirksam wird, finden Sie unter Bearbeiten erweiterter [Stile](edit-control-window-extended-styles.md)für Das Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zähler des Zoomverhältnis.

</dd> <dt>

*lParam* 
</dt> <dd>

Nenner des Zoomverhältnis. Diese Parameter können die folgenden Werte haben.



| Wert                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Beide 0**</dt> </dl>                                                                                                   | Deaktiviert das Zoomen mithilfe der **EM \_ SETZOOM-Meldung** (das Zoomen kann weiterhin mit [**TxGetExtent auftreten).**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Zoomen der Anzeige nach Zähler/Nenner des Zoomverhältnis<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die neue Zoomeinstellung akzeptiert wird, ist der Rückgabewert **TRUE.**

Wenn die neue Zoomeinstellung nicht akzeptiert wird, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

**Bearbeiten:** Wird in Windows 10 1809 und höher unterstützt. Für das Bearbeitungssteuerobjekt muss der erweiterte Stil **ES \_ EX \_ ZOOMABLE** festgelegt sein. Informationen dazu, dass diese Meldung wirksam wird, finden Sie unter Bearbeiten erweiterter [Stile](edit-control-window-extended-styles.md)für Das Steuerelement. Informationen zum Bearbeitungssteuerelementen finden Sie unter [Edit Controls](about-edit-controls.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h/Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**EM \_ GETZOOM**](em-getzoom.md)
</dt> </dl>

 

 





