---
description: Stellt den Bereich dar, der von der -Erkennen verwendet wird, in dem Ink gezeichnet werden kann. Der Bereich wird als Erkennungsleitfaden bezeichnet.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: InkRecognizerGuide-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 758c2ac58803b0086a4a4083545a66d250799b414bd44e3814c90de37ca9d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675665"
---
# <a name="inkrecognizerguide-class"></a>InkRecognizerGuide-Klasse

Stellt den Bereich dar, der von der -Erkennen verwendet wird, in dem Ink gezeichnet werden kann. Der Bereich wird als Erkennungsleitfaden bezeichnet.

**InkRecognizerGuide** verfügt über die folgenden Membertypen:

-   [Schnittstellen](#interfaces)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Die **InkRecognizerGuide-Klasse** definiert diese Schnittstellen.



| Schnittstelle               | BESCHREIBUNG                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Dieses Objekt implementiert die **COM-Schnittstelle IInkRecognizerGuide.**<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **InkRecognizerGuide-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Spalten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lesen/Schreiben<br/> | Ruft die Anzahl der Spalten im Führungsfeld ab oder legt diese fest.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lesen/Schreiben<br/> | Ruft das Feld ab, das physisch auf dem Bildschirm des Tablets gezeichnet wird und in dem geschrieben wird, oder legt dieses fest.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lesen/Schreiben<br/> | Ruft Leitfadendaten für C++-Entwickler ab oder legt diese fest.<br/>                                                                         |
| [**Mittellinie**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lesen/Schreiben<br/> | Ruft die Mittlerenhöhe ab oder legt sie fest. Die Mittlerenhöhe ist der Abstand zwischen der Baseline und der Mittellinie des gezeichneten Felds.<br/> |
| [**Zeilen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lesen/Schreiben<br/> | Ruft die Anzahl der Zeilen im Führungsfeld ab oder legt diese fest.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lesen/Schreiben<br/> | Ruft den unsichtbaren Schreibbereich des Führungsfelds ab, in dem tatsächlich geschrieben werden kann, oder legt diese fest.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode instanziiert**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) werden.

Standardmäßig gibt es keine Anleitung zur Wiedererkennung. In einer Standardanleitung sind alle Eigenschaftswerte auf 0 festgelegt. Sie müssen die Eigenschaften dieses Objekts verwenden, um die Anleitung festlegen zu können.

Wenn die Anwendung Richtlinien auf dem Bildschirm gezeichnet hat, auf dem der Benutzer schreiben soll, sollte die Anwendung die Werte der Eigenschaften der Recognizer-Anleitung festlegen, um die Erkennen zu informieren. Diese Eigenschaften sind nur für die Verwendung durch die Recognizer-Eigenschaft. Wenn Sie sie festlegen, werden keine visuellen Hinweise auf die Anzeige geerbt. Die Anwendung oder das Steuerelement zeichnet die visuellen Hinweise.

Die Erkennungsanleitung kann aus Zeilen und Spalten bestehen, und diese geben der Erkennung einen besseren Kontext, in dem sie eine Erkennung durchführen kann. Buchstaben wie "t" und "I" sind leichter zu erkennen, wenn ein Leitfaden verwendet wird, um der Ink-Datei Kontext zu geben. Beispielsweise können Sie horizontale Linien auf einem Bildschirm zeichnen, die zeigen, wo geschrieben werden soll (diese Art von Leitfaden würde nur aus Zeilen bestehen und keine Spalten). Durch das Schreiben in die Zeilen verbessert sich die Erkennungsgenauigkeit anstelle von beliebigem Platz.

Die Anleitung gibt die Grenzen der Freiraumkoordinaten in Freiraum an.

Die [**DrawnBox-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) kann ein Feld definieren, das die gleiche Größe wie oder kleiner als das feld hat, das von der [**WritingBox-Eigenschaft definiert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) wird.

Die folgende Abbildung zeigt die Elemente einer Recognizer-Anleitung mit zwei Zeilen und ohne Spalten.

![Abbildung, die Elemente des Leitfadens zur Wiedererkennung zeigt](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Zusätzlich zum Zeichnen von Linien auf dem Bildschirm, die Benutzern zeigen, wo geschrieben werden soll, können Sie Zellen auf dem Bildschirm zeichnen, auf denen Zeichen oder Wörter geschrieben werden. Dies wird als Geschachtelte Eingabe bezeichnet und ist für einige sprachen in Asien nützlich. Rufen Sie die [**Capabilities-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) des [**IInkRecognizer-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) auf, um zu ermitteln, ob die Ermittlung geschachtelte Eingaben ermöglichen kann.

Die folgende Abbildung zeigt eine Anleitung zur Erkennen von vier Spalten.

![Abbildung: Leitfaden zur Wiedererkennung mit vier Spalten](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkRecognizer-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md)
</dt> </dl>

 

