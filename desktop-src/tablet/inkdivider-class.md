---
description: Stellt die Fähigkeit dar, das Layout einer Auflistung von Strichen zu analysieren und Sie in Text und Grafiken aufzuteilen.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: InkDivider-Klasse (Msinkaut15. h)
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
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352494"
---
# <a name="inkdivider-class"></a>InkDivider-Klasse

Stellt die Fähigkeit dar, das Layout einer Auflistung von Strichen zu analysieren und Sie in Text und Grafiken aufzuteilen.

**InkDivider** verfügt über folgende Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkDivider** -Klasse definiert.



| Schnittstelle       | BESCHREIBUNG                                                          |
|:----------------|:---------------------------------------------------------------------|
| **Iinkdivider** | Dieses Objekt implementiert die **iinkdivider** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **InkDivider** -Klasse verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Glie**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Gibt ein [**iinkdivisionresult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt zurück, das Strukturinformationen zu den Strichen im **InkDivider** -Objekt enthält.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **InkDivider** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lesen/Schreiben<br/> | Ruft die erwartete Handschrift Höhe in HIMETRIC-Einheiten ab oder legt diese fest.<br/>                                                      |
| [**Erkennungs Kontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lesen/Schreiben<br/> | Ruft das für die Handschrifterkennung verwendete [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt ab oder legt es fest.<br/> |
| [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lesen/Schreiben<br/> | Ruft die im **InkDivider** -Objekt enthaltene [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab oder legt Sie fest. <br/>     |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Das **InkDivider** -Objekt verwendet das Layout der Striche, die Reihenfolge, in der die Striche hinzugefügt werden, die Richtung, in der die Striche gezeichnet werden, und andere Faktoren zum Durchführen der Analyse der frei Hand Eingaben. Die vom **InkDivider** -Objekt analysierten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ist in der [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) -Eigenschaft des **InkDivider** -Objekts enthalten. Das **InkDivider** -Objekt analysiert die inkstrokes-Auflistung dynamisch, wenn Sie Sie der Auflistung hinzufügen oder daraus löschen, aber es führt keine Änderung der Striche aus.

Die Analyseergebnisse werden in einem [**iinkdivisionresult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt zurückgegeben.

Das **InkDivider** -Objekt verwendet ein [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt, um die Striche genauer aufzuteilen und den Ergebnissen eine Erkennungs Zeichenfolge zuzuweisen.

> [!Note]  
> Das **InkDivider** -Objekt verwendet die Standard Eigenschafts Einstellungen des [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekts.

 

Wenn Sie dem **InkDivider** -Objekt keinen Erkennungs Kontext zuweisen, analysiert das **InkDivider** -Objekt weiterhin die frei Hand Eingaben, dividiert die Striche jedoch weniger genau und ordnet der Divisions Ergebnisse keinen Text zu.

> [!Note]  
> Die [**erkenzercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) -Eigenschaft sollte festgelegt werden, bevor der [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) -Eigenschaft Striche hinzugefügt werden. Nach dem Hinzufügen von Strichen zum **InkDivider** -Objekt kann die Eigenschaft " **erkennzercontext** " nicht geändert werden.

 

Der **InkDivider** unterstützt derzeit keine vertikalen Sprachen. Damit das **InkDivider** -Objekt diese Sprachen ordnungsgemäß erkennt, muss das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt für die Sprache die kostenlose Eingabe Funktion unterstützen, und die Zeichen müssen von links nach rechts geschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                               |
| Header<br/>                   | <dl> <dt>Msinkaut15. h (erfordert auch Msinkaut15 \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkdivisionresult-Schnittstelle**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**Inkrecognizercontext-Klasse**](inkrecognizercontext-class.md)
</dt> <dt>

[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

