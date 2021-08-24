---
title: CB_GETCUEBANNER Meldung (Winuser.h)
description: Ruft den Im Bearbeitungssteuerelement eines Kombinationsfelds angezeigten Text des Cue-Banners ab. Senden Sie diese Nachricht explizit oder mithilfe des ComboBox \_ GetCueBannerText-Makros.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81ddcd8123f28317726f412255f440d47f53310aa035ab34d25190658550163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089270"
---
# <a name="cb_getcuebanner-message"></a>CB \_ GETCUEBANNER-Nachricht

Ruft den Im Bearbeitungssteuerelement eines Kombinationsfelds angezeigten Text des Cue-Banners ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ComboBox \_ GetCueBannerText-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Unicode-Zeichenfolgenpuffer, der den Text des Hinweisbanners empfängt. Die aufrufende Anwendung ist für die Zuweisung des Arbeitsspeichers für den Puffer verantwortlich. Die Puffergröße muss der Länge der Cue-Bannerzeichenfolge in **WCHARs** und 1 für den abschließenden **NULL-WCHAR-Wert** entsprechen. 

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Die Größe des Puffers, auf den *lpcwText* in **WCHARs** zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 1 zurück, andernfalls einen Fehlerwert.

Wenn kein Hinweisbannertext abzurufen ist, ist der Rückgabewert 0. Wenn die aufrufende Anwendung keinen Puffer zuordnet oder *lParam* vor dem Senden dieser Nachricht festgelegt hat, kann das nicht definierte Verhalten auftreten, und der Rückgabewert ist möglicherweise nicht zuverlässig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kombinationsfeldfeatures](combo-box-features.md)
</dt> </dl>

 

 





