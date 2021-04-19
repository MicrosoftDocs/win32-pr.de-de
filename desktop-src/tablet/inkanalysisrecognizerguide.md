---
description: Gibt das Handbuch oder den Bereich an, in dem frei Hand Eingaben gezeichnet und erkannt werden.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Inkanalysiserkenzerguide-Struktur (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356742"
---
# <a name="inkanalysisrecognizerguide-structure"></a>Inkanalysiserkenzerguide-Struktur

Gibt das Handbuch oder den Bereich an, in dem frei Hand Eingaben gezeichnet und erkannt werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a>Member

<dl> <dt>

**rectbeschreitingbox**
</dt> <dd>

Der unsichtbare Schreibbereich des Erkennungs Handbuchs, in dem geschrieben werden kann.

</dd> <dt>

**rectdrawnbox**
</dt> <dd>

Das Rechteck, das auf dem Tablet-Bildschirm gezeichnet wird und in dem geschrieben wird.

</dd> <dt>

**Crows**
</dt> <dd>

Die Anzahl der Zeilen im Feld Erkennungs Handbuch.

</dd> <dt>

**cColumns**
</dt> <dd>

Die Anzahl der Spalten im Feld Erkennungs Handbuch.

</dd> <dt>

**vervollständigen**
</dt> <dd>

Die Höhe des Feld Erkennungs Handbuchs in der Mitte. Die mittlere Höhe ist der Abstand zwischen der Baseline und der Mitte des gezeichneten Felds.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein **inkanalysiserkenzerguide** definiert einen erwarteten Bereich von Eingaben, z. b. eine Linie oder Felder für Zeichen. Eine **inkanalysiserkenzerguide** -Struktur kann nur auf einem Kontext Knoten des Analyse Hinweises festgelegt werden (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)). Der [**iinkanalyzer**](iinkanalyzer.md) verwendet den Speicherort des Knoten "Analyse Hinweis" und die Speicherorte der frei Hand Striche, um dem Knoten "Analyse Hinweis" einen Strich zuzuordnen. Bei allen Strichen mit einer Zuordnung zum Knoten des Analyse Hinweises wird das angegebene **inkanalysiserkenzerguide** verwendet, wenn es von einem **iinkanalyzer** erkannt wird, vorausgesetzt, der **iinkanalyzer** unterstützt das **inkanalysiserkenzerguide**. Die Werte, die in der **inkanalysiserkenzerguide** -Klasse ausgedrückt werden, sind immer relativ zum Speicherort des Analysis Hint-Knotens und werden in Freihand Raumkoordinaten angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften des Analyse Hinweises](analysis-hint-properties.md)
</dt> <dt>

[**Iinkanalyzer:: feateanalysishint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




