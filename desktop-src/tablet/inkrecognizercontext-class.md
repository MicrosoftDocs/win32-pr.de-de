---
description: Ermöglicht das Ausführen von frei Hand Eingaben, das Abrufen des Erkennungs Ergebnisses und das Abrufen von Alternativen. Der inkrecognizercontext ermöglicht der verschiedenen Erkennungs Modul, die auf einem System installiert sind, die Verwendung der frei Handerkennung, um die Eingabe entsprechend zu verarbeiten.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Inkrecognizercontext-Klasse (msink AUT. h)
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
ms.openlocfilehash: afe5469cabf6764ed9b02fdcffcc8c1bedaca1d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216411"
---
# <a name="inkrecognizercontext-class"></a>Inkrecognizercontext-Klasse

Ermöglicht das Ausführen von frei Hand Eingaben, das Abrufen des Erkennungs Ergebnisses und das Abrufen von Alternativen. Der **inkrecognizercontext** ermöglicht der verschiedenen Erkennungs Modul, die auf einem System installiert sind, die Verwendung der frei Handerkennung, um die Eingabe entsprechend zu verarbeiten.

**Inkrecognizercontext** enthält diese Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **inkrecognizercontext** -Klasse enthält diese Ereignisse.



| Ereignis                                                                               | BESCHREIBUNG                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erkennung**](inkrecognizercontext-recognition.md)                             | Tritt auf, wenn der inkrecognizercontext Ergebnisse aus der backgrounderkennmethode generiert hat.<br/>                                                                                             |
| [**Erkentionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) | Tritt auf, wenn der **inkrecognizercontext** Ergebnisse generiert hat, nachdem die [**backgrounderkennzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode aufgerufen wurde.<br/> |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **inkrecognizercontext** -Klasse definiert.



| Schnittstelle                 | BESCHREIBUNG                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **Iinkrecognizercontext** | Dieses Objekt implementiert die **iinkrecognizercontext** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **inkrecognizercontext** -Klasse verfügt über diese Methoden.



| Methode                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Background erkannt**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Gibt an, dass die Erkennung die zugeordneten Striche erkennen und ein [**Erkennungs**](inkrecognizercontext-recognition.md) Ereignis auslösen soll, wenn die Erkennung beendet ist.<br/>                                                                |
| [**Backgrounderkenzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Gibt an, dass die Erkennung die zugeordneten Striche erkennen und ein [**erkentionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) -Ereignis auslösen soll, wenn die Erkennung beendet ist.<br/>                                    |
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Erstellt ein doppeltes **inkrecognizercontext**.<br/>                                                                                                                                                                                               |
| [**Umdinkinput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Beendet die frei Hand Eingabe an den **inkrecognizercontext**.<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Gibt an, ob das System Wörterbuch, das Benutzerwörterbuch oder die [**Wortliste**](inkwordlist-class.md) eine angegebene Zeichenfolge enthält<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Führt eine Erkennung für eine [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung durch und gibt Erkennungsergebnisse zurück.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Beendet die Hintergrund Erkennung, die mit einem Rückruf von [**backgroundrecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) oder [**backgrounderkenzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)gestartet wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **inkrecognizercontext** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Charakteristische automatische Vervollständigung**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Lesen/Schreiben<br/> | Ruft den Auto Vervollständigen-Modus des Zeichens ab, der bestimmt, wann Zeichen oder Wörter erkannt werden, oder legt ihn fest.<br/>                                         |
| [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Lesen/Schreiben<br/> | Ruft den Zeichen folgen Namen des Faktoid ab, das vom **inkrecognizercontext** -Objekt verwendet wird, oder legt diesen fest.<br/>                                                        |
| [**Handbuch**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Lesen/Schreiben<br/> | Ruft den für die frei Hand Eingabe zu verwendenden [**InkRecognizerGuide**](inkrecognizerguide-class.md) ab oder legt diesen fest.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Lesen/Schreiben<br/> | Ruft die Zeichen ab, die vor der [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung im **inkrecognizercontext** -Objekt enthalten sind, oder legt diese fest.<br/> |
| [**Erkentionflags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Lesen/Schreiben<br/> | Ruft die Flags ab oder legt diese fest, die angeben, wie die Erkennung die Handschrift interpretiert und die Ergebnis Zeichenfolge bestimmt.<br/>                                     |
| [**Erkennung**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Lesen/Schreiben<br/> | Ruft das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt ab, das vom **inkrecognizercontext** -Objekt verwendet wird, oder legt dieses fest.<br/>                                   |
| [**Striche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Lesen/Schreiben<br/> | Ruft die dem **inkrecognizercontext** -Objekt zugeordnete [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab oder legt Sie fest.<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Lesen/Schreiben<br/> | Ruft die Zeichen ab, die nach der [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung im **inkrecognizercontext** -Objekt enthalten sind, oder legt diese fest.<br/>  |
| [**"WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Lesen/Schreiben<br/> | Ruft das [**inkwordlist**](inkwordlist-class.md) -Objekt ab, das zum Verbessern der Erkennungsergebnisse verwendet wird, oder legt dieses fest.<br/>                               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Es gibt zwei Arten der Erkennung: Background (Asynchronous) oder Vordergrund (synchron). Die Hintergrund Erkennung wird durch einen Rückruf der Methoden [**Background**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) Recognition oder [**backgrounderkenzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) gestartet, tritt in einem Hintergrund Thread auf und meldet Ergebnisse an die Anwendung über einen Ereignis Mechanismus. Die Vordergrund Erkennung gibt erst dann zurück, wenn die gesamte Erkennung abgeschlossen ist, sodass die Erkennungsergebnisse für den aufrufenden Thread verfügbar sind, ohne das Erkennungs Ereignis zu überwachen.

Frei Hand Eingaben werden fortlaufend im Hintergrund verarbeitet. Wenn der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, auf die der **inkrecognizercontext** verweist, ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) hinzugefügt wird, wird das **IInkStrokeDisp** sofort erkannt. Weitere Informationen finden Sie [**in den Hinweisen im Thema zur Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) "Methode".

Die gesamte Erkennung erfolgt über einen Erkennungs Kontext. Der Kontext definiert die Einstellungen für eine einzelne Erkennungs Sitzung. Er empfängt die frei Hand Eingabe, die erkannt werden muss, und definiert die Einschränkungen für die frei Hand Eingabe und die Erkennungs Ausgabe. Die Einschränkungen, die für den Kontext festgelegt werden können, sind u. a. die Sprache, das Wörterbuch und die verwendete Grammatik.

> [!Note]  
> Das Festlegen von Eigenschaften, die nicht die [**Striche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) - [**Eigenschaft oder die Eigenschaft "Eigenschaften für**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) Eigenschaften von Eigenschaften" aufweisen **, ist nur** erfolgreich, [Wenn die](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Sie müssen die anderen Eigenschaften festlegen, bevor Sie die inkstrokes-Auflistung an den **inkrecognizercontext** anfügen, oder Sie müssen die inkstrokes-Auflistung auf **null** festlegen und dann die anderen Eigenschaften festlegen. Wenn Sie für die inkstrokes-Auflistung **null** festlegen und dann die anderen Eigenschaften festlegen, müssen Sie möglicherweise die inkstrokes-Auflistung erneut anfügen. Dies liegt daran, dass die Erkennung unmittelbar nach dem Zuweisen der inkstrokes zum **inkrecognizercontext** beginnt. Wenn ein-Befehl zum [**erkennen der Methode " \[ inkrecognizecontext \] Class**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) " oder " [**backgrounderkannte**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)" aufgerufen wird, sind möglicherweise bereits die Rückruf Ergebnisse verfügbar.

 

Um die Leistung Ihrer Anwendung zu verbessern, löschen Sie Ihr **inkrecognizercontext** -Objekt, wenn es nicht mehr benötigt wird.

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

[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

