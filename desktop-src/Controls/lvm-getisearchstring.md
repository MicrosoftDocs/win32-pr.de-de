---
title: LVM_GETISEARCHSTRING (Commctrl.h)
description: Ruft die inkrementelle Suchzeichenfolge eines Listenansicht-Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetISearchString-Makros senden.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d612a6c1ba303bc08b6d5067ccb4dd3802354456159e3aea4120bd122348e74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540820"
---
# <a name="lvm_getisearchstring-message"></a>LVM \_ GETISEARCHSTRING-Nachricht

Ruft die inkrementelle Suchzeichenfolge eines Listenansicht-Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetISearchString-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der die inkrementelle Suchzeichenfolge empfängt. Um einfach die Länge der Zeichenfolge abzurufen, legen *Sie lParam auf* **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen in der inkrementellen Suchzeichenfolge zurück, ohne das beendende NULL-Zeichen, oder 0 (null), wenn sich das Listenansicht-Steuerelement nicht im inkrementellen Suchmodus befindet.

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit Ihres Programms gefährden. Diese Meldung bietet Ihnen keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Meldung verwenden, rufen Sie zuerst die Meldung auf, die **NULL** im *lParam* übergibt. Dadurch wird die Anzahl der zeichen zurückgegeben, mit Ausnahme von **NULL,** die erforderlich sind. Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen. Lesen Sie die [Sicherheitsüberlegungen: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.

Die *inkrementelle Suchzeichenfolge* ist die Zeichenfolge, die der Benutzer eingibt, während die Listenansicht den Eingabefokus besitzt. Jedes Mal, wenn der Benutzer ein Zeichen eingibt, fügt das System das Zeichen an die Suchzeichenfolge an und sucht dann nach einem übereinstimmenden Element. Wenn das System eine Übereinstimmung findet, wählt es das Element aus und führt bei Bedarf einen Bildlauf in die Ansicht durch.

Jedem Vom Benutzer typisierungsbasierten Zeichen wird ein Time out-Zeitraum zugeordnet. Wenn das Time out verstreicht, bevor der Benutzer ein anderes Zeichen eingibt, wird die inkrementelle Suchzeichenfolge zurückgesetzt.

Stellen Sie sicher, dass der Puffer groß genug ist, um die Zeichenfolge und das beendende NULL-Zeichen zu enthalten. Wenn er zu klein ist, führt dies zu einem unmittelbar ungültigen Seitenfehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) und **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





