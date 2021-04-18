---
description: Gibt die Attribute eines iinkanalysiserkenzer an.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Erkenzerfunktionalitäten-Enumeration (iacom. h)
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
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357821"
---
# <a name="recognizercapabilities-enumeration"></a>Erkennungsfunktionen-Enumeration

Gibt die Attribute eines [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)an.

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

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ keine**
</dt> <dd>

Es wurden keine Funktionen angegeben.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC- \_ donotcare**
</dt> <dd>

Ignoriert alle anderen Flags, die festgelegt sind.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC- \_ Objekt**
</dt> <dd>

Unterstützt Objekterkennung; Andernfalls wird nur Text von erkannt.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ freeinput**
</dt> <dd>

Unterstützt kostenlose Eingaben, bei denen frei Hand Eingaben ohne Erkennungs Handbuch eingegeben werden, z. b. eine Linie oder ein Feld.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC- \_ LinedInput**
</dt> <dd>

Unterstützt eine Inline Eingabe, die dem Schreiben auf einem Whitepaper ähnelt.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC- \_ boxedinput**
</dt> <dd>

Unterstützt eingegebene Eingaben, wobei jedes Zeichen oder Wort in einem Feld eingegeben wird.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC- \_ Merkmal autocompletioninput**
</dt> <dd>

Unterstützt das automatische Vervollständigen von Zeichen. Erkennungs Modul, die Zeichen Auto Vervollständigen unterstützen, erfordern eine eingegebene Eingabe.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC- \_ rightanddown**
</dt> <dd>

Unterstützt die Handschrift Eingabe in der richtigen Reihenfolge und in der richtigen Reihenfolge, wie z. b. in westlichen Sprachen und in

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ leftanddown**
</dt> <dd>

Unterstützt Handschrift Eingaben in der linken und in der Reihenfolge, z. b. in hebräischen und arabischen Sprachen.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC- \_ downandleft**
</dt> <dd>

Unterstützt Handschrift Eingaben in der Reihenfolge nach unten und Links, z. b. in einigen ostasiatischen Sprachen.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC- \_ downandright**
</dt> <dd>

Unterstützt die Handschrift Eingabe in der richtigen Reihenfolge, z. b. in einigen ostasiatischen Sprachen.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC- \_ arbiaryangle**
</dt> <dd>

Unterstützt Text, der in beliebigen Winkeln geschrieben wurde.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC- \_ Gitter**
</dt> <dd>

Unterstützt das Zurückgeben eines Gitters als Alternative Zeichenfolge für Handschrift Erkennungsergebnisse.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC- \_ adviseinkchange**
</dt> <dd>

Unterstützt das Unterbrechen der Hintergrund Erkennung, z. b. wenn die frei Hand Eingabe geändert wurde

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ strokereorder**
</dt> <dd>

Unterstützt, dass die hubreihenfolge, räumlich und Temporale, als Teil des Erkennungs Vorgangs behandelt werden. Der [**iinkanalyzer**](iinkanalyzer.md) ändert keine Striche neu, bevor er frei Hand Eingaben an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)sendet.

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ personalisierbar**
</dt> <dd>

Unterstützt personalisierte Handschrift, bei der die Erkennung die Erkennung verbessert, wenn Sie im Laufe der Zeit für dieselbe Handschrift verfügbar ist.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ prefersarbitraryangle**
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) muss die Handschrift nicht in eine horizontale Ausrichtung drehen, bevor die frei Hand Eingaben an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)gesendet werden.

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ prefersparagraphbreak**
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) sollte ganze Absätze von frei Hand Eingaben an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)senden, sodass **iinkanalysiserkenzer** den Zeilenumbruch und das Wort (oder das Zeichen) unterbricht.

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ preferssegmentationrecognition**
</dt> <dd>

Erkennt nur ein Wort oder Zeichen pro Erkennungs Vorgang. [**Iinkanalyzer**](iinkanalyzer.md) führt Segmentierung auf der Handschrift durch und sendet jeweils nur ein Segment an [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration ermöglicht eine bitweise Kombination der Element Werte. Verwenden Sie diese Enumeration, um eine installierte Handschrifterkennung zu suchen, die die benötigten Attribute unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalysiserkenzer:: getfunktionen**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




