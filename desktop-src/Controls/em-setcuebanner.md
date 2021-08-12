---
title: EM_SETCUEBANNER Nachricht (Commctrl.h)
description: Legt den Texthinweis oder Tipp fest, der vom Bearbeitungssteuerelement angezeigt wird, um den Benutzer zur Eingabe von Informationen aufzufordern.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08694d7368a994c639f236f18537e13d81f57083521599c23671941c74889bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673103"
---
# <a name="em_setcuebanner-message"></a>EM \_ SETCUEBANNER-Nachricht

Legt den Texthinweis oder Tipp fest, der vom Bearbeitungssteuerelement angezeigt wird, um den Benutzer zur Eingabe von Informationen aufzufordern.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

**TRUE,** wenn das Hinweisbanner auch dann angezeigt werden soll, wenn das Bearbeitungssteuerelement den Fokus besitzt. Andernfalls **FALSE**. **FALSE** ist das Standardverhalten, bei dem das Hinweisbanner ausgeblendet wird, wenn der Benutzer auf das Steuerelement klickt.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Text enthält, der als Texthinweise angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **TRUE** zurückgegeben. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Ein Bearbeitungssteuerelement, das zum Starten einer Suche verwendet wird, zeigt möglicherweise "Suche hier eingeben" in grauer Textform als Texthinweise an. Wenn der Benutzer auf den Text klickt, wird der Text entfernt, und der Benutzer kann eingeben.

Sie können kein Cue-Banner für ein mehrzeiliges Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement festlegen.

> [!Note]  
> Um diese API verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bearbeiten \_ von SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





