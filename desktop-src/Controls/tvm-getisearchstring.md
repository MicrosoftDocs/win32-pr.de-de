---
title: TVM_GETISEARCHSTRING-Nachricht (Commctrl.h)
description: Ruft die inkrementelle Suchzeichenfolge für ein Strukturansichtssteuerelement ab.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 79838b2b0d2f109216caf970d33d51b4a3c1369da7b1fc47f5a53e45c3ee82fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060240"
---
# <a name="tvm_getisearchstring-message"></a>TVM \_ GETISEARCHSTRING-Nachricht

Ruft die inkrementelle Suchzeichenfolge für ein Strukturansichtssteuerelement ab. Das Strukturansichtssteuerelement verwendet die inkrementelle Suchzeichenfolge, um ein Element basierend auf vom Benutzer eingegebenen Zeichen auszuwählen. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-Makros GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den Puffer, der die inkrementelle Suchzeichenfolge empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen in der inkrementellen Suchzeichenfolge zurück.

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit Ihres Programms beeinträchtigen. Sie müssen einen ausreichend großen Puffer für die Zeichenfolge zuordnen. Rufen Sie zunächst die Nachricht auf, die **NULL** in *lParam* übergibt. Dadurch wird die Anzahl der erforderlichen Zeichen zurückgegeben, mit Ausnahme von **NULL.** Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen. Lesen Sie [Sicherheitsüberlegungen: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.

Wenn sich das Strukturansichtssteuerelement nicht im inkrementellen Suchmodus befindet, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) und **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





