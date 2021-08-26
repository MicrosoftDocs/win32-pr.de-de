---
title: TB_GETMAXSIZE (Commctrl.h)
description: Ruft die Gesamtgröße aller sichtbaren Schaltflächen und Trennzeichen in der Symbolleiste ab.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- TB_GETMAXSIZE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511d5726f117bbda183f55af5570fb75c2df3c78f5f6132dcefb406ee8fa7b70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918680"
---
# <a name="tb_getmaxsize-message"></a>TB \_ GETMAXSIZE-Nachricht

Ruft die Gesamtgröße aller sichtbaren Schaltflächen und Trennzeichen in der Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SIZE-Struktur,**](/previous-versions//dd145106(v=vs.85)) die die Größe der Elemente empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

