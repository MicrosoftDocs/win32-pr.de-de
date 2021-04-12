---
description: Stellt den Bereich dar, den die Erkennung verwendet, in dem frei Hand Eingaben gezeichnet werden können. Der Bereich wird als Erkennungs Handbuch bezeichnet.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: InkRecognizerGuide-Klasse (msink AUT. h)
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
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218578"
---
# <a name="inkrecognizerguide-class"></a>InkRecognizerGuide-Klasse

Stellt den Bereich dar, den die Erkennung verwendet, in dem frei Hand Eingaben gezeichnet werden können. Der Bereich wird als Erkennungs Handbuch bezeichnet.

**InkRecognizerGuide** verfügt über diese Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkRecognizerGuide** -Klasse definiert.



| Schnittstelle               | BESCHREIBUNG                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **Iinkrecognizerguide** | Dieses Objekt implementiert die **iinkrecognizerguide** -com-Schnittstelle.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **InkRecognizerGuide** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Spalten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lesen/Schreiben<br/> | Ruft die Anzahl der Spalten im Führungs Feld ab oder legt diese fest.<br/>                                                                |
| [**Drawnbox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lesen/Schreiben<br/> | Ruft das Feld ab, das physisch auf dem Bildschirm des Tablets gezeichnet wird und in dem geschrieben wird, oder legt dieses fest.<br/>              |
| [**Guidedata**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lesen/Schreiben<br/> | Ruft Führungs Daten für C++-Entwickler ab oder legt Sie fest.<br/>                                                                         |
| [**Vervollständigen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lesen/Schreiben<br/> | Ruft die Höhe des Mittelpunkts ab oder legt diese fest. Die Höhe des Mittelpunkts liegt zwischen der Baseline und der Mitte der gezeichneten Box.<br/> |
| [**Streitigkeiten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lesen/Schreiben<br/> | Ruft die Anzahl der Zeilen im Führungs Feld ab oder legt diese fest.<br/>                                                                   |
| [**Beschreibbox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lesen/Schreiben<br/> | Ruft den nicht sichtbaren Schreibbereich des Handbuchs ab, in dem geschrieben werden kann, oder legt diesen fest.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode instanziiert werden.

Standardmäßig gibt es keine Erkennungs Anleitung. In einem standardhandbuch sind alle Eigenschaftswerte auf 0 festgelegt. Sie müssen die Eigenschaften dieses-Objekts verwenden, um das Handbuch festzulegen.

Wenn die Anwendung Richtlinien auf dem Bildschirm gezeichnet hat, auf dem der Benutzer zu schreiben erwartet, sollte die Anwendung die Werte der Eigenschaften des Erkennungs Leitfadens festlegen, um die Erkennung zu informieren. Diese Eigenschaften sind nur für die Verwendung durch die Erkennung vorgesehen. Wenn Sie Sie festlegen, zeichnen Sie visuelle Hinweise auf der Anzeige. Die Anwendung oder das Steuerelement zeichnet die visuellen Hinweise.

Das Erkennungs Handbuch kann aus Zeilen und Spalten bestehen, und diese geben der Erkennung einen besseren Kontext zum Durchführen der Erkennung. Buchstaben wie "t" und "I" lassen sich leichter erkennen, wenn ein Leitfaden verwendet wird, um dem frei Hand Kontext Kontext zuzuweisen. Beispielsweise können Sie horizontale Linien auf einem Bildschirm zeichnen, die anzeigen, wo das Schreiben erfolgen soll (dieser Richtlinientyp würde nur aus Zeilen und ohne Spalten bestehen). Durch das Schreiben in den Zeilen wird die Erkennungsgenauigkeit verbessert, anstatt etwas beliebiges Leerzeichen.

Das Handbuch gibt die Grenzen des frei Hand Zeichens in frei Hand Raumkoordinaten an.

Die [**drawnbox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) -Eigenschaft kann ein Feld definieren, das der Größe entspricht, die kleiner ist als das von der Eigenschaft " [**Write Box**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) " definierte Feld.

Die folgende Abbildung zeigt die Elemente eines Erkennungs Leitfadens mit zwei Zeilen und ohne Spalten.

![Abbildung der Elemente des Erkennungs Leitfadens](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Zusätzlich zum Zeichnen von Linien auf dem Bildschirm, die Benutzer anzeigen, für die Sie schreiben möchten, können Sie Zellen auf dem Bildschirm zeichnen, in denen Zeichen oder Wörter geschrieben sind. Dies wird als eingegebene Eingabe bezeichnet und ist für einige asiatische Sprachen nützlich. Um zu ermitteln, ob die Erkennung in der Lage ist, eine eingegebene Eingabe aufzurufen, müssen Sie die Eigenschaft [**Funktionen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) des [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekts aufzurufen.

Die folgende Abbildung zeigt eine Erkennungs Anleitung mit vier Spalten.

![Darstellung des Erkennungs Leitfadens mit vier Spalten](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkrecognizer-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Inkrecognizercontext-Klasse**](inkrecognizercontext-class.md)
</dt> </dl>

 

