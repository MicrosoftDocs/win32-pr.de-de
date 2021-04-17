---
title: EM_SETSCROLLPOS Meldung (RichEdit. h)
description: Führt einen Bildlauf für den Inhalt eines Rich-Edit-Steuer Elements zum angegebenen Punkt durch.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Windows-Steuerelemente für EM_SETSCROLLPOS Meldung
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
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478558"
---
# <a name="em_setscrollpos-message"></a>EM \_ setscrollpos-Meldung

Führt einen Bildlauf für den Inhalt eines Rich-Edit-Steuer Elements zum angegebenen Punkt durch.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die einen Punkt im virtuellen Textbereich des Dokuments in Pixel angibt. Das Dokument wird gescrollt, bis sich dieser Punkt in der oberen linken Ecke des Bearbeitungs Steuer Elements befindet. Wenn Sie die Ansicht so ändern möchten, dass die obere linke Ecke der Ansicht zwei Zeilen nach unten und ein Zeichen vom linken Rand aus angezeigt wird. Sie würden einen Punkt (7, 22) übergeben.

Das Rich Edit-Steuerelement überprüft die x-und y-Koordinaten und passt Sie ggf. an, sodass oben eine komplette Zeile angezeigt wird. Außerdem wird sichergestellt, dass der Text niemals vollständig vom Ansichts Rechteck entfernt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getscrollpos**](em-getscrollpos.md)
</dt> </dl>

 

