---
description: Gibt die Attribute eines IInkAnalysisRecognizer an.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: RecognizerCapabilities-Enumeration (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 96e932b8e47f323198e1b0cc87da0df7839a593a76850c00c2c2e4d095854851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091450"
---
# <a name="recognizercapabilities-enumeration"></a>RecognizerCapabilities-Enumeration

Gibt die Attribute eines [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)an.

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ None**
</dt> <dd>

Es wurden keine Funktionen angegeben.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**
</dt> <dd>

Ignoriert alle anderen Flags, die festgelegt sind.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**\_RC-Objekt**
</dt> <dd>

Unterstützt die Objekterkennung. andernfalls wird nur Text erkannt.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**
</dt> <dd>

Unterstützt kostenlose Eingaben, bei denen Freihandeingaben ohne Verwendung eines Erkennungsleitfadens wie z. B. einer Zeile oder eines Felds eingegeben werden.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**
</dt> <dd>

Unterstützt gestrichstrichene Eingaben, die dem Schreiben auf zeileniertem Papier ähneln.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**
</dt> <dd>

Unterstützt geschachtelte Eingaben, bei denen jedes Zeichen oder Wort in ein Feld eingegeben wird.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**
</dt> <dd>

Unterstützt autovervollständigende Zeichen. Erkennungen, die autovervollständigende Zeichen unterstützen, erfordern geschachtelte Eingaben.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**
</dt> <dd>

Unterstützt Handschrifteingaben in der richtigen und unteren Reihenfolge, z. B. in westen Sprachen und einigen ostasiatischen Sprachen.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**
</dt> <dd>

Unterstützt Handschrifteingaben in linker und nach unten geschriebener Reihenfolge, z. B. in hebräischen und arabischen Sprachen.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**
</dt> <dd>

Unterstützt Handschrifteingaben in nach unten und links, z. B. in einigen ostasiatischen Sprachen.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**
</dt> <dd>

Unterstützt Handschrifteingaben in der nach unten und rechts geschriebenen Reihenfolge, z. B. in einigen ostasiatischen Sprachen.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**
</dt> <dd>

Unterstützt Text, der in beliebigen Winkeln geschrieben wird.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ Lattice**
</dt> <dd>

Unterstützt das Zurückgeben eines Lattice als Alternative zu einer Zeichenfolge für Handschrifterkennungsergebnisse.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**
</dt> <dd>

Unterstützt das Unterbrechen der Hintergrunderkennung, z. B. wenn sich die Ink geändert hat.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**
</dt> <dd>

Unterstützt, dass die räumliche und temporale Strichreihenfolge als Teil des Erkennungsvorgangs behandelt wird. [**IInkAnalyzer**](iinkanalyzer.md) ordnet Striche nicht neu an, bevor Freihand an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)gesendet wird.

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ Personalisierbar**
</dt> <dd>

Unterstützt personalisierte Handschrift, wobei die Erkennung die Erkennung verbessert, wenn sie im Laufe der Zeit für dieselbe Handschrift verfügbar gemacht wird.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**
</dt> <dd>

Der [**IInkAnalyzer**](iinkanalyzer.md) muss die Handschrift nicht in eine horizontale Ausrichtung drehen, bevor die Freihandschrift an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)gesendet wird.

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**
</dt> <dd>

Der [**IInkAnalyzer**](iinkanalyzer.md) sollte ganze Freihandabschnitte an den [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)senden, sodass **IInkAnalysisRecognizer** zeilen- und wort- oder zeichenteilige Brüche durchführen kann.

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**
</dt> <dd>

Erkennt nur ein Wort oder Zeichen pro Erkennungsvorgang. [**IInkAnalyzer**](iinkanalyzer.md) führt die Segmentierung der Handschrift aus und sendet jeweils nur ein Segment an [**den IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration ermöglicht eine bitweise Kombination ihrer Memberwerte. Verwenden Sie diese Enumeration, um eine installierte Ink-Erkennung zu suchen, die die benötigten Attribute unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




