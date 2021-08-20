---
title: Vordefinierte Textattribute (TsAttrid.h)
description: Die folgenden Werte identifizieren Textattribute, die mit der ITfContext GetAppProperty-Methode erhalten wurden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind enthalten.
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- Vordefinierte Textattribute Textdienstframework
topic_type:
- apiref
api_name:
- Predefined Text Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4518e754b5ddca5a8fe19ed35434d9150a76061edc08966447dbe2de9b5a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951838"
---
# <a name="predefined-text-attributes"></a>Vordefinierte Textattribute

Die folgenden Werte identifizieren Textattribute, die mit der [**ITfContext::GetAppProperty-Methode erhalten**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) wurden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind enthalten.

## <a name="properties"></a>Eigenschaften



| Eigenschaft                                     | Beschreibung                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| TSATTRID-Text \_                               | Wird nicht verwendet.                                                                                                                                                |
| \_TSATTRID-Textausrichtung \_                    | Wird nicht verwendet.                                                                                                                                                |
| TSATTRID \_ Text \_ Alignment \_ Center            | Enthält einen Wert ungleich 0 (null), wenn der Text zentriert ist, andernfalls 0 (null).                                                                                      |
| TSATTRID \_ Text \_ Alignment \_ Justify           | Enthält einen Wert ungleich 0 (null), wenn der Text gerechtfertigt ist, andernfalls 0 (null).                                                                                     |
| TSATTRID– \_ \_ Textausrichtung \_ links              | Enthält einen Wert ungleich 0 (null), wenn der Text linksbündig ausgerichtet ist, andernfalls 0 (null).                                                                                  |
| TSATTRID– \_ \_ Textausrichtung \_ rechts             | Enthält einen Wert ungleich 0 (null), wenn der Text rechtsbündig ausgerichtet ist, andernfalls 0 (null).                                                                                 |
| TSATTRID \_ Text \_ EmbeddedObject               | Enthält einen Wert ungleich 0 (null), wenn der Text ein eingebettetes Objekt oder andernfalls 0 (null) ist.                                                                            |
| \_ \_ TSATTRID-Text-Bindestriche                  | Enthält einen Wert ungleich 0 (null), wenn der Text bindestrichiert ist, andernfalls 0 (null).                                                                                    |
| \_TSATTRID-Textsprache \_                     | Enthält den **LANGID-Sprachbezeichner** des Texts.                                                                                                 |
| \_TSATTRID-Textlink \_                         | Enthält einen Zeiger auf ein Linkobjekt. Der Aufrufer muss die QueryInterface-Methode verwenden, um die gewünschte Schnittstelle wie **IUniformResourceLocator zu erhalten.** |
| \_TSATTRID-Textausrichtung \_                  | Gibt den Winkel zwischen der Textbasislinie und der x-Achse des Geräts in Zehntel grad an.                                                          |
| TSATTRID \_ Text \_ Para                         | Wird nicht verwendet.                                                                                                                                                |
| TSATTRID \_ Text \_ Para \_ FirstLineIndent        | Enthält die Anzahl der Punkte, um die die erste Zeile eines Absatzes eingerückt ist.                                                                            |
| TSATTRID \_ Text \_ Para \_ LeftIndent             | Enthält die Anzahl der Punkte, um die der Absatz von links eingerückt wird.                                                                              |
| TSATTRID \_ Text \_ Para \_ LineSpacing            | Wird nicht verwendet.                                                                                                                                                |
| TSATTRID \_ Text \_ Para \_ LineSpacing \_ AtLeast   | Enthält die Mindestanzahl von Zeilen für den Zeilenabstand des Absatzes.                                                                              |
| TSATTRID \_ Text \_ Para \_ LineSpacing \_ Double    | Enthält einen Wert ungleich 0 (null), wenn der Absatz doppelt oder andernfalls 0 (null) ist.                                                                            |
| TSATTRID \_ Text \_ Para \_ LineSpacing \_ Exactly   | Enthält die genaue Anzahl von Zeilen für den Zeilenabstand des Absatzes.                                                                                |
| TSATTRID \_ Text \_ Para \_ LineSpacing \_ Multiple  | Enthält die Anzahl der Zeilen für den Abstand zwischen mehreren Zeilen des Absatzes.                                                                             |
| TSATTRID \_ Text \_ Para \_ LineSpacing \_ OnePtFive | Enthält einen Wert ungleich 0 (null), wenn der Absatz eine und eine halbe Zeile leerzeichend oder andernfalls 0 (null) ist.                                                             |
| TSATTRID \_ Text \_ Para \_ LineSpacing \_ Single    | Enthält einen Wert ungleich 0 (null), wenn der Absatz ein einzelnes Leerzeichen oder andernfalls 0 (null) ist.                                                                            |
| TSATTRID \_ Text \_ Para \_ RightIndent            | Enthält die Anzahl der Punkte, um die der Absatz von rechts eingerückt wird.                                                                             |
| TSATTRID \_ Text \_ Para \_ SpaceAfter             | Enthält die Anzahl der Abstandspunkte nach dem Absatz.                                                                                            |
| TSATTRID \_ Text \_ Para \_ SpaceBefore            | Enthält die Anzahl der Abstandspunkte vor dem Absatz.                                                                                           |
| TSATTRID \_ Text \_ ReadOnly                     | Enthält 0 (null), wenn der Text schreibgeschützt ist oder andernfalls ungleich 0 (null) ist.                                                                                             |
| TSATTRID \_ Text \_ RightToLeft                  | Enthält 0 (null), wenn der Text von rechts nach links gelesen wird oder andernfalls ungleich 0 (null) ist.                                                                                 |
| TSATTRID \_ Text \_ VerticalWriting              | Gibt an, ob der Text vertikal oder horizontal ist. Enthält 0 (null), wenn der Text horizontal oder ungleich 0 (null) ist, wenn der Text vertikal ist.                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>TsAttrid.h</dt> </dl> |



 

