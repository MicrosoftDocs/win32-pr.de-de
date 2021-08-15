---
title: EM_SETSCROLLPOS Nachricht (Richedit.h)
description: Führt einen Bildlauf des Inhalts eines Rich-Edit-Steuerelements bis zum angegebenen Punkt durch.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d86609c1b3f4b04ade24e5ea2f3343c367bbad0a52b8e07be7c18b2282536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412335"
---
# <a name="em_setscrollpos-message"></a>EM \_ SETSCROLLPOS-Nachricht

Führt einen Bildlauf des Inhalts eines Rich-Edit-Steuerelements bis zum angegebenen Punkt durch.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**POINT-Struktur,**](/previous-versions//dd162805(v=vs.85)) die einen Punkt im virtuellen Textbereich des Dokuments in Pixel angibt. Das Dokument wird gescrollt, bis sich dieser Punkt in der oberen linken Ecke des Bearbeitungssteuerelementfensters befindet. Wenn Sie die Ansicht so ändern möchten, dass die obere linke Ecke der Ansicht zwei Zeilen nach unten und ein Zeichen vom linken Rand entfernt ist. Sie würden einen Punkt von (7, 22) übergeben.

Das Rich-Edit-Steuerelement überprüft die x- und y-Koordinaten und passt sie bei Bedarf an, sodass oben eine vollständige Linie angezeigt wird. Außerdem wird sichergestellt, dass der Text nie vollständig aus dem Ansichtsrechteck gescrollt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 

