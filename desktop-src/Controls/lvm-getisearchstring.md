---
title: LVM_GETISEARCHSTRING Meldung (kommstrg. h)
description: Ruft die inkrementelle Such Zeichenfolge eines Listenansicht-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getisearchstring-Makros senden.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Windows-Steuerelemente für LVM_GETISEARCHSTRING Meldung
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
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478525"
---
# <a name="lvm_getisearchstring-message"></a>LVM- \_ getisearchstring-Nachricht

Ruft die inkrementelle Such Zeichenfolge eines Listenansicht-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getisearchstring**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der die inkrementelle Such Zeichenfolge empfängt Legen Sie *LPARAM* auf **null** fest, um die Länge der Zeichenfolge abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen in der inkrementellen Such Zeichenfolge zurück, ohne das abschließende Null-Zeichen, oder 0 (null), wenn sich das Listenansicht-Steuerelement nicht im inkrementellen

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Meldung verwenden, müssen Sie zuerst die Nachricht mit der Übergabe von **null** im *LPARAM*-Element aufzurufen. Dadurch wird die Anzahl der Zeichen zurückgegeben, ausgenommen **null** . Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

Die *inkrementelle Such Zeichenfolge* ist die Zeichenfolge, die der Benutzer eingibt, während die Listenansicht den Eingabefokus besitzt. Jedes Mal, wenn der Benutzer ein Zeichen eingibt, fügt das System das Zeichen an die Such Zeichenfolge an und sucht dann nach einem entsprechenden Element. Wenn das System eine Entsprechung findet, wählt es das Element aus und führt ggf. einen Bildlauf in die Ansicht aus.

Jedem Zeichen, das der Benutzer eingibt, wird ein Timeout Zeitraum zugeordnet. Wenn die Timeout Spanne abläuft, bevor der Benutzer ein anderes Zeichen eingibt, wird die Zeichenfolge für die inkrementelle Suche zurückgesetzt.

Stellen Sie sicher, dass der Puffer groß genug ist, um die Zeichenfolge und das abschließende Null-Zeichen zu speichern. Wenn es zu klein ist, wird ein sofortiger ungültiger Seiten Fehler zurückzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Getisearchstringw** (Unicode) und **LVM \_ getisearchstrauinga** (ANSI)<br/> |



 

 





