---
title: Vordefinierte Text Attribute ("tsatyd. h")
description: Die folgenden Werte identifizieren Text Attribute, die mit der ITF Context getappproperty-Methode abgerufen werden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- Vordefinierte Text Attribute Text Dienste-Framework
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
ms.openlocfilehash: 6cb214f6c555b589c52e9916325e38b46b0bfb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105381"
---
# <a name="predefined-text-attributes"></a>Vordefinierte Text Attribute

Die folgenden Werte identifizieren Text Attribute, die mit der [**ITF context:: getappproperty**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) -Methode abgerufen werden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.

## <a name="properties"></a>Eigenschaften



| Eigenschaft                                     | BESCHREIBUNG                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| - \_ Text                               | Nicht verwendet.                                                                                                                                                |
| Text Ausrichtung für den Tsat- \_ Text \_                    | Nicht verwendet.                                                                                                                                                |
| \_Text \_ Ausrichtungs \_ Zentrier Text            | Enthält einen Wert ungleich 0 (null), wenn der Text zentriert ist oder andernfalls NULL.                                                                                      |
| \_Text Ausrichtung für die Text \_ Ausrichtung \_           | Enthält einen Wert ungleich 0 (null), wenn der Text gerechtfertigt ist, andernfalls NULL.                                                                                     |
| Die Text Ausrichtung für den Tsat- \_ Text \_ \_ Links              | Enthält einen Wert ungleich 0 (null), wenn der Text linksbündig ausgerichtet oder andernfalls NULL ist.                                                                                  |
| \_Text \_ Ausrichtung nach \_ Rechts             | Enthält einen Wert ungleich 0 (null), wenn der Text rechtsbündig ausgerichtet ist, andernfalls NULL.                                                                                 |
| "- \_ TextBlock \_ "               | Enthält einen Wert ungleich 0 (null), wenn der Text ein eingebettetes Objekt ist, andernfalls NULL.                                                                            |
| \_TextText- \_ Bindestrich                  | Enthält einen Wert ungleich 0 (null), wenn der Text mittels Bindestrich ist, andernfalls NULL.                                                                                    |
| Sprache für den \_ Sprache-Text \_                     | Enthält den **LangID** -sprach Bezeichner des Texts.                                                                                                 |
| \_Text Verknüpfung "tsatder d" \_                         | Enthält einen Zeiger auf ein Link Objekt. Der Aufrufer muss die QueryInterface-Methode verwenden, um die gewünschte Schnittstelle zu erhalten, z. b. **iuniforresourcelocator**. |
| Text Ausrichtung für den Tsat- \_ Text \_                  | Gibt den Winkel in Zehntel Grad zwischen der Text Basislinie und der x-Achse des Geräts an.                                                          |
| Der Wert für die Spalte "Tsat" \_ \_                         | Nicht verwendet.                                                                                                                                                |
| Der Tsat- \_ Text-Text \_ para \_ firstlineingedent        | Enthält die Anzahl der Punkte, an denen die erste Zeile eines Absatzes eingezogen ist.                                                                            |
| \_Virus Text Text \_ para Richtung \_             | Enthält die Anzahl der Punkte, an denen der Absatz von Links eingerückt wird.                                                                              |
| -Text- \_ para-Text \_ \_            | Nicht verwendet.                                                                                                                                                |
| Der Wert von "- \_ Text" \_ \_ \_   | Enthält die Mindestanzahl von Zeilen für den Zeilenabstand des Absatzes.                                                                              |
| Wert für " \_ \_ \_ tsatzweid" für " \_ Double"    | Enthält einen Wert ungleich 0 (null), wenn der Absatz einen doppelten Abstand hat, andernfalls NULL.                                                                            |
| Der Wert für die Text-ID "". \_ \_ \_ \_   | Enthält die genaue Anzahl von Zeilen für den Zeilenabstand des Absatzes.                                                                                |
| Der Wert von "-Text" für "". \_ \_ \_ \_  | Enthält die Anzahl der Zeilen für den Abstand mehrerer Zeilen des Absatzes.                                                                             |
| Der- \_ Text-Text-Text \_ para \_ linespacingoneptfive \_ | Enthält einen Wert ungleich 0 (null), wenn der Absatz ein und eine halbe Zeilen Grenze ist, andernfalls NULL.                                                             |
| "Tsatzd" \_ Text \_ para \_ linespacingsingle \_    | Enthält einen Wert ungleich 0 (null), wenn der Absatz einzelner Abstand ist, andernfalls NULL.                                                                            |
| "Tsatzd"- \_ Text \_ para \_ RightIndent            | Enthält die Anzahl der Punkte, an denen der Absatz von rechts eingerückt wird.                                                                             |
| Der '- \_ Text '-Text ' \_ para \_ SpaceAfter '             | Enthält die Anzahl der Abstands Punkte nach dem Absatz.                                                                                            |
| Der Tsat- \_ Text-Text \_ para \_ SpaceBefore            | Enthält die Anzahl der Abstands Punkte vor dem Absatz.                                                                                           |
| Der '- \_ Text '-Text ' \_                     | Enthält 0 (null), wenn der Text schreibgeschützt ist oder andernfalls ungleich 0 (null).                                                                                             |
| Der Tsat- \_ Text " \_ RightToLeft"                  | Enthält 0 (null), wenn der Text von rechts nach links gelesen oder andernfalls ungleich 0 (null) ist.                                                                                 |
| \_Text verticalwriting in der-Textdatei \_              | Gibt an, ob der Text vertikal oder horizontal ist. Enthält 0 (null), wenn der Text horizontal oder nicht NULL ist, wenn der Text vertikal ist.                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>"Tsatphd. h"</dt> </dl> |



 

