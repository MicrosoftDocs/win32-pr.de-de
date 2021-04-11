---
title: TB_SETROWS Meldung (kommstrg. h)
description: Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- Windows-Steuerelemente für TB_SETROWS Meldung
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041012"
---
# <a name="tb_setrows-message"></a>TB- \_ Nachricht (loggt)

Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -Wert gibt die Anzahl der angeforderten Zeilen an. Die Mindestanzahl von Zeilen ist 1, und die maximale Anzahl von Zeilen entspricht der Anzahl der Schaltflächen auf der Symbolleiste.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob mehr Zeilen als angefordert erstellt werden sollen, wenn das System nicht die Anzahl der Zeilen erstellen kann, die von *wParam* angegeben werden. **True** gibt an, dass das System weitere Zeilen erstellt. Wenn der Wert **false** ist, erstellt das System weniger Zeilen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck der Symbolleiste empfängt, nachdem die Zeilen festgelegt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Da das System beim Festlegen der Zeilen Anzahl keine Schaltflächen Gruppen aufbricht, kann sich die resultierende Anzahl von Zeilen von der angeforderten Anzahl unterscheiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

