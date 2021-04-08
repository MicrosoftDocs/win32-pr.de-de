---
title: TB_SETMAXTEXTROWS Meldung (kommstrg. h)
description: Legt die maximale Anzahl der auf einer Symbolleisten Schaltfläche angezeigten Textzeilen fest.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Windows-Steuerelemente für TB_SETMAXTEXTROWS Meldung
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949596"
---
# <a name="tb_setmaxtextrows-message"></a>TB \_ setmaxtextrows-Nachricht

Legt die maximale Anzahl der auf einer Symbolleisten Schaltfläche angezeigten Textzeilen fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Maximale Anzahl von Textzeilen, die angezeigt werden können.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Um das Umbruch von Text zu bewirken, müssen Sie die maximale Schaltflächen breite festlegen, indem Sie eine [**TB- \_ setbuttonwidth**](tb-setbuttonwidth.md) -Nachricht senden. Der Text wird bei einem Wort Umbruch umschlossen. Zeilenumbrüche (" \\ n") im Text werden ignoriert. Der Text in den tbstyle- \_ Listen Symbolleisten wird immer in einer einzelnen Zeile angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





