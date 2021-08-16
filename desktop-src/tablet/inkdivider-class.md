---
description: Stellt die Möglichkeit dar, das Layout einer Auflistung von Strichen zu analysieren und in Text und Grafiken zu unterteilen.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: InkDivider-Klasse (Msinkaut15.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: d7dd98aaef627bac6a26340464c14c4e46c07d6a23f32c2664651503b5d79014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220831"
---
# <a name="inkdivider-class"></a>InkDivider-Klasse

Stellt die Möglichkeit dar, das Layout einer Auflistung von Strichen zu analysieren und in Text und Grafiken zu unterteilen.

**InkDivider verfügt** über die folgenden Membertypen:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Die **InkDivider-Klasse** definiert diese Schnittstellen.



| Schnittstelle       | Beschreibung                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Dieses Objekt implementiert die **IInkDivider-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkDivider-Klasse** verfügt über diese Methoden.



| Methode                              | Beschreibung                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividieren**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Gibt ein [**IInkDivisionResult-Objekt**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) zurück, das strukturelle Informationen zu den Strichen im **InkDivider-Objekt** enthält.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **InkDivider-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp           | Beschreibung                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lesen/Schreiben<br/> | Ruft die erwartete Schrifthöhe in HIMETRIC-Einheiten ab oder legt diese fest.<br/>                                                      |
| [**Recognizercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lesen/Schreiben<br/> | Ruft das für die [**Handschrifterkennung verwendete InkRecognizerContext-Objekt**](inkrecognizercontext-class.md) ab oder legt dieses fest.<br/> |
| [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lesen/Schreiben<br/> | Ruft die im **InkDivider-Objekt** enthaltene [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab oder legt sie fest. <br/>     |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Das **InkDivider-Objekt** verwendet das Layout der Striche, die Reihenfolge, in der die Striche hinzugefügt werden, die Richtung, in der die Striche gezeichnet werden, und andere Faktoren, um die Analyse der Ink durchzuführen. Die Vom **InkDivider-Objekt** analysierte [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ist in der [**Strokes-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) des **InkDivider-Objekts** enthalten. Das **InkDivider-Objekt** analysiert die InkStrokes-Auflistung dynamisch, während Sie der Auflistung hinzufügen oder daraus löschen, führt jedoch keine Änderung der Striche durch.

Die Analyseergebnisse werden in einem [**IInkDivisionResult-Objekt**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) zurückgegeben.

Das **InkDivider-Objekt** verwendet ein [**InkRecognizerContext-Objekt,**](inkrecognizercontext-class.md) um die Striche genauer zu unterteilen und den Ergebnissen eine Erkennungszeichenfolge zu zuweisen.

> [!Note]  
> Das **InkDivider-Objekt** verwendet die Standardeigenschaftseinstellungen des [**InkRecognizerContext-Objekts.**](inkrecognizercontext-class.md)

 

Wenn Sie dem **InkDivider-Objekt** keinen Recognizer-Kontext zuweisen, analysiert das **InkDivider-Objekt die InkDivider-Objekte** weiterhin, teilt die Striche jedoch weniger genau auf und ordnet den Divisionsergebnissen keinen Text zu.

> [!Note]  
> Die [**RecognizerContext-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) sollte festgelegt werden, bevor der [**Strokes-Eigenschaft Striche hinzugefügt**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) werden. Nachdem dem **InkDivider-Objekt** Striche hinzugefügt wurden, kann die **RecognizerContext-Eigenschaft** nicht mehr geändert werden.

 

Der **InkDivider unterstützt** derzeit keine vertikalen Sprachen. Damit das **InkDivider-Objekt** diese Sprachen ordnungsgemäß erkennt, muss das [**IInkRecognizer-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) für die Sprache die funktion für die kostenlose Eingabe unterstützen, und die Zeichen müssen von links nach rechts geschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                               |
| Header<br/>                   | <dl> <dt>Msinkaut15.h (erfordert auch Msinkaut15 \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkDivisionResult-Schnittstelle**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md)
</dt> <dt>

[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

