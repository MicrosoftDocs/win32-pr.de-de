---
title: LVM_SETINFOTIP (Commctrl.h)
description: Legt QuickInfo-Text in verzögerter Antwort auf die \_ LVN-GETINFOTIP-Benachrichtigung fest.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef739535e399550911adfbe86d7376d3efeb77cd797ba807b24ee682d1f3fe3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919900"
---
# <a name="lvm_setinfotip-message"></a>LVM \_ SETINFOTIP-Nachricht

Legt QuickInfo-Text in verzögerter Antwort auf die [ \_ LVN-GETINFOTIP-Benachrichtigung](lvn-getinfotip.md) fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP-Struktur,</a> die die festgelegten Informationen enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der QuickInfo-Text erfolgreich festgelegt wurde, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Mit **der LVM \_ SETINFOTIP-Nachricht** kann eine Anwendung Infotips im Hintergrund berechnen, indem die folgenden Schritte ausgeführt werden:

1.  Legen Sie als Reaktion auf [die LVN \_ GETINFOTIP-Benachrichtigung](lvn-getinfotip.md) das **pszText-Element** der [**NMLVGETINFOTIP-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) auf eine leere Zeichenfolge fest, und geben Sie 0 zurück.
2.  Berechnen Sie im Hintergrund den Infotip.
3.  Senden Sie nach dem Berechnen des Infotips die **LVM \_ SETINFOTIP-Nachricht,** indem Sie das **pszText-Element** der [**LVSETINFOTIP-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) auf den Infotip und die **iItem-** und **iSubItem-Elemente** auf das Element und Unterelement festlegen, für das der Infotip gilt.

Der an die **LVM \_ SETINFOTIP-Nachricht** übergebene Text wird nur angezeigt, wenn sich das von der [**LVSETINFOTIP-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) beschriebene Element und Unterelement noch in einem Zustand befinden, der einen Infotip erfordert.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





