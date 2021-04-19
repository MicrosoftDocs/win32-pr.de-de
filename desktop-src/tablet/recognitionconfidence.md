---
description: Gibt die Vertrauens Ebene an, die der iinkanalyzer in der Genauigkeit des Erkennungs Ergebnisses hat.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Erkentionconfidence-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351559"
---
# <a name="recognitionconfidence-enumeration"></a>Erkentionconfidence-Enumeration

Gibt die Vertrauens Ebene an, die der [**iinkanalyzer**](iinkanalyzer.md) in der Genauigkeit des Erkennungs Ergebnisses hat.

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**Erkentionconfidence \_ Strong**
</dt> <dd>

Sicheres Vertrauen im Ergebnis oder bei Alternativen.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**Erkennungs Konfidenz \_ zwischen**
</dt> <dd>

Zwischen Vertrauen im Ergebnis oder Alternativen.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**Erkennunkonfidenz \_ Mangel**
</dt> <dd>

Mangelhafte Zuverlässigkeit im Ergebnis oder Alternativen.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**\_Erkennunbekanntem Erkennungs Vertrauen**
</dt> <dd>

Das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element, das den erkannten Text generiert hat, unterstützt keine Vertrauens Ebenen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

[**Iinkanalyzer**](iinkanalyzer.md) verwendet mindestens ein [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekt, um Handschrift in Text zu konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisalternate:: getrecognitionconfidence-Methode**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Kontext Knoten Eigenschaften](context-node-properties.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




