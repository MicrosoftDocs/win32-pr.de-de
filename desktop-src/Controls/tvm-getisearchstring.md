---
title: TVM_GETISEARCHSTRING Meldung (kommstrg. h)
description: Ruft die inkrementelle Such Zeichenfolge für ein Strukturansicht-Steuerelement ab.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Windows-Steuerelemente für TVM_GETISEARCHSTRING Meldung
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105957"
---
# <a name="tvm_getisearchstring-message"></a>TVM- \_ getisearchstring-Meldung

Ruft die inkrementelle Such Zeichenfolge für ein Strukturansicht-Steuerelement ab. Das Strukturansicht-Steuerelement verwendet die inkrementelle Such Zeichenfolge, um auf der Grundlage der vom Benutzer eingegebenen Zeichen ein Element auszuwählen. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ getisearchstring**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den Puffer, der die inkrementelle Such Zeichenfolge empfängt

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen in der inkrementellen Such Zeichenfolge zurück

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen. Sie müssen einen ausreichend großen Puffer zuordnen, um die Zeichenfolge zu speichern. Nennen Sie zuerst die Nachricht, die **null** in *LPARAM* übergibt. Dadurch wird die Anzahl von Zeichen zurückgegeben, die erforderlich sind, ausgenommen **null**. Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

Wenn sich das Strukturansicht-Steuerelement nicht im inkrementellen Suchmodus befindet, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ Getisearchstringw** (Unicode) und **TVM \_ getisearchstrauinga** (ANSI)<br/> |



 

 





