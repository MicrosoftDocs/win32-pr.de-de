---
description: Ermöglicht das Ausführen der Ink-Erkennung, das Abrufen des Erkennungsergebnisses und das Abrufen alternativer Funktionen. InkRecognizerContext ermöglicht der verschiedenen Erkennung, die auf einem System installiert sind, die Verwendung der Ink-Erkennung, um Eingaben entsprechend zu verarbeiten.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: InkRecognizerContext-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 781d1b440f1287b22d5c3ddf7ecf7132f7311fc5f48da5da20e4145717f65bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218401"
---
# <a name="inkrecognizercontext-class"></a>InkRecognizerContext-Klasse

Ermöglicht das Ausführen der Ink-Erkennung, das Abrufen des Erkennungsergebnisses und das Abrufen alternativer Funktionen. **InkRecognizerContext** ermöglicht der verschiedenen Erkennung, die auf einem System installiert sind, die Verwendung der Ink-Erkennung, um Eingaben entsprechend zu verarbeiten.

**InkRecognizerContext** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkRecognizerContext-Klasse** verfügt über diese Ereignisse.



| Ereignis                                                                               | Beschreibung                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erkennung**](inkrecognizercontext-recognition.md)                             | Tritt ein, wenn der InkRecognizerContext Ergebnisse aus der BackgroundRecognize-Methode generiert hat.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Tritt ein, wenn **der InkRecognizerContext** nach dem Aufruf der [**BackgroundRecognizeWithAlternates-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) Ergebnisse generiert hat.<br/> |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkRecognizerContext-Klasse** definiert.



| Schnittstelle                 | Beschreibung                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerContext** | Dieses Objekt implementiert die **IInkRecognizerContext-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkRecognizerContext-Klasse** verfügt über diese Methoden.



| Methode                                                                                              | Beschreibung                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Backgroundrecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Gibt an, dass die Erkennung die zugeordneten Striche erkennen und ein [**Erkennungsereignis**](inkrecognizercontext-recognition.md) ausgelöst werden soll, wenn die Erkennung abgeschlossen ist.<br/>                                                                |
| [**Backgroundrecognizewithalternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Gibt an, dass die Erkennung die zugeordneten Striche erkennen und ein [**RecognitionWithAlternates-Ereignis**](inkrecognizercontext-recognitionwithalternates.md) ausgelöst werden soll, wenn die Erkennung abgeschlossen ist.<br/>                                    |
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Erstellt ein doppeltes **InkRecognizerContext-Objekt.**<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Beendet die **InkRecognizerContext-Eingabe.**<br/>                                                                                                                                                                                             |
| [**Isstringsupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Gibt an, ob das Systemwörterbuch, das Benutzerwörterbuch oder die [**Wortliste**](inkwordlist-class.md) eine angegebene Zeichenfolge enthalten.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Führt die Erkennung für eine [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) aus und gibt Erkennungsergebnisse zurück.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Beendet die Hintergrunderkennung, die mit einem Aufruf von [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) oder [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)gestartet wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **InkRecognizerContext-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | Beschreibung                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Lesen/Schreiben<br/> | Ruft den AutoVervollständigen-Modus für Zeichen ab, der bestimmt, wann Zeichen oder Wörter erkannt werden, oder legt dieses fest.<br/>                                         |
| [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Lesen/Schreiben<br/> | Ruft den Zeichenfolgennamen des factoid ab, das vom **InkRecognizerContext-Objekt** verwendet wird, oder legt den Zeichenfolgennamen fest.<br/>                                                        |
| [**Handbuch**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Lesen/Schreiben<br/> | Ruft den [**InkRecognizerGuide**](inkrecognizerguide-class.md) ab, der für die Ink-Eingabe verwendet werden soll, oder legt diesen fest.<br/>                                                   |
| [**Prefixtext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Lesen/Schreiben<br/> | Ruft die Zeichen ab, die vor der [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) im **InkRecognizerContext-Objekt liegen,** oder legt sie fest.<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Lesen/Schreiben<br/> | Ruft die Flags ab, die angeben, wie die Erkennung die Ink interpretiert und die Ergebniszeichenfolge bestimmt, oder legt sie fest.<br/>                                     |
| [**Erkennungsmodul**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Lesen/Schreiben<br/> | Ruft das [**IInkRecognizer-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) ab, das vom **InkRecognizerContext-Objekt** verwendet wird, oder legt es fest.<br/>                                   |
| [**Striche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Lesen/Schreiben<br/> | Ruft die [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die dem **InkRecognizerContext-Objekt** zugeordnet ist, oder legt sie fest.<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Lesen/Schreiben<br/> | Ruft die Zeichen ab, die nach der [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) im **InkRecognizerContext-Objekt stammen,** oder legt sie fest.<br/>  |
| [**Wordlist**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Lesen/Schreiben<br/> | Ruft das [**InkWordList-Objekt**](inkwordlist-class.md) ab, das zum Verbessern der Erkennungsergebnisse verwendet wird, oder legt dieses fest.<br/>                               |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Es gibt zwei Arten der Erkennung: Hintergrund (asynchron) oder Vordergrund (synchron). Die Hintergrunderkennung wird durch einen Aufruf der [**BackgroundRecognize-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) oder [**BackgroundRecognizeWithAlternates-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) gestartet, tritt in einem Hintergrundthread auf und meldet ergebnisse über einen Ereignismechanismus an die Anwendung. Die Vordergrunderkennung wird erst zurückgegeben, wenn die gesamte Erkennung abgeschlossen ist, sodass dem aufrufenden Thread Erkennungsergebnisse zur Verfügung gestellt werden, ohne auf das Erkennungsereignis zu lauschen.

Ink wird kontinuierlich im Hintergrund verarbeitet. Wenn der [InkStrokes-Sammlung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) auf die der **InkRecognizerContext** verweist, ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) hinzugefügt wird, wird **IInkStrokeDisp** sofort erkannt. Weitere Informationen finden Sie in den Hinweisen im Thema [**EndInkInput-Methode.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)

Die gesamte Erkennung erfolgt über einen Erkennungskontext. Der Kontext definiert die Einstellungen für eine einzelne Erkennungssitzung. Sie empfängt die Zugabe, die erkannt werden muss, und definiert die Einschränkungen für die Ink-Eingabe und die Erkennungsausgabe. Zu den Einschränkungen, die für den Kontext festgelegt werden können, gehören die verwendete Sprache, das Wörterbuch und die Grammatik.

> [!Note]  
> Das Festlegen anderer Eigenschaften als [**der Strokes-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) oder [**CharacterAutoCompletion-Eigenschaft**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) ist nur erfolgreich, wenn die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) **NULL** ist. Sie müssen die anderen Eigenschaften festlegen, bevor Sie die InkStrokes-Sammlung an **den InkRecognizerContext** anfügen, oder Sie müssen die InkStrokes-Auflistung auf **NULL** festlegen und dann die anderen Eigenschaften festlegen. Wenn Sie die InkStrokes-Sammlung auf **NULL** und dann die anderen Eigenschaften festlegen, müssen Sie die InkStrokes-Sammlung möglicherweise erneut anfügen. Dies liegt daran, dass die Erkennung direkt nach dem Zuweisen der InkStrokes zum **InkRecognizerContext** beginnt. Wenn die [**Recognize-Methode \[ InkRecognizeContext-Klasse \]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) oder [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)aufgerufen wird, sind die Aufrufergebnisse möglicherweise bereits verfügbar.

 

Um die Leistung Ihrer Anwendung zu verbessern, verwerfen Sie Ihr **InkRecognizerContext-Objekt,** wenn es nicht mehr benötigt wird.

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

[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

