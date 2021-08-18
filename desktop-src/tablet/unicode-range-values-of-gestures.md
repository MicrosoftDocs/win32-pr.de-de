---
description: 'Wenn Sie Ihre eigene Microsoft-Gestenerkennung implementieren, müssen Sie den Namen und den Unicode-Bereichswert für jede Geste definieren, die ihre Recognizer erkennen soll. Wenn Sie die Gesten implementieren möchten, die bereits unterstützt oder als Teil der Gestenerkennung von Microsoft definiert sind, verwenden Sie die definierten Namen und Unicode-Bereichswerte für diese Gesten. Die gesamte Auflistung von Namen und Unicode-Bereichswerten für implementierte und nicht implementierte Gesten in der Gestenerkennung von Microsoft wird in der Headerdatei Recdefs.h bereitgestellt (standardmäßig installiert in C: Programme \\ Microsoft Tablet PC Platform SDK \\ \\ Include). Die Gestennamen und Unicode-Bereichswerte sind auch in den folgenden Tabellen aufgeführt. Hinweis Die GESTE NULL-Geste wird verwendet, um anzugeben, dass eine \_ Erkennende Eingaben nicht als Geste erkennt.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Unicode-Bereichswerte von Gesten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f96c1f59ea9e53d63999c01db73c45080f205bccf043e26463563b0f1f6af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449223"
---
# <a name="unicode-range-values-of-gestures"></a>Unicode-Bereichswerte von Gesten

Wenn Sie Ihre eigene Microsoft-Gestenerkennung implementieren, müssen Sie den Namen und den Unicode-Bereichswert für jede Geste definieren, die ihre Recognizer erkennen soll.

Wenn Sie die Gesten implementieren möchten, die bereits unterstützt oder als Teil der Gestenerkennung von Microsoft definiert sind, verwenden Sie die definierten Namen und Unicode-Bereichswerte für diese Gesten. Die gesamte Auflistung von Namen und Unicode-Bereichswerten für implementierte und nicht implementierte Gesten in der Gestenerkennung von Microsoft wird in der Headerdatei Recdefs.h bereitgestellt (standardmäßig installiert in C: Programme \\ Microsoft Tablet PC Platform SDK \\ \\ Include). Die Gestennamen und Unicode-Bereichswerte sind auch in den folgenden Tabellen aufgeführt.

> [!Note]  
> Die \_ GESTE NULL wird verwendet, um anzugeben, dass eine Erkennende Eingaben nicht als Geste erkennt.

 

## <a name="implemented-gestures"></a>Implementierte Gesten



| Gestenname                          | Unicode-Bereichswert |
|---------------------------------------|---------------------|
| GESTURE \_ NULL<br/>              | 0xf000<br/>   |
| \_GESTEN-SCRATCHOUT<br/>        | 0xf001<br/>   |
| \_GESTENDREIECK<br/>          | 0xf002<br/>   |
| \_GESTENPLATZ<br/>            | 0xf003<br/>   |
| \_GESTEN-STERN<br/>              | 0xf004<br/>   |
| \_GESTENÜBERPRÜFUNG<br/>             | 0xf005<br/>   |
| \_GESTEN-CURLICUE<br/>          | 0xf010<br/>   |
| GESTURE \_ DOUBLE \_ CURLICUE<br/>  | 0xf011<br/>   |
| \_GESTENKREIS<br/>            | 0xf020<br/>   |
| GESTE \_ – \_ DOPPELTER KREIS<br/>    | 0xf021<br/>   |
| GESTE \_ \_ HALBKREISFÖRMIGES LINKS<br/>  | 0xf028<br/>   |
| GESTE \_ HALBKREIS \_ RECHTS<br/> | 0xf029<br/>   |
| \_GESTEN-CHEVRON \_ NACH OBEN<br/>       | 0xf030<br/>   |
| \_GESTEN-CHEVRON \_ NACH UNTEN<br/>     | 0xf031<br/>   |
| GESTE \_ CHEVRON \_ LINKS<br/>     | 0xf032<br/>   |
| GESTE \_ CHEVRON \_ RECHTS<br/>    | 0xf033<br/>   |
| \_GESTENPFEIL \_ NACH OBEN<br/>         | 0xf038<br/>   |
| \_GESTENPFEIL \_ NACH UNTEN<br/>       | 0xf039<br/>   |
| \_GESTENPFEIL \_ NACH LINKS<br/>       | 0xf03a<br/>   |
| \_GESTENPFEIL \_ NACH RECHTS<br/>      | 0xf03b<br/>   |
| GESTEN \_ NACH OBEN<br/>                | 0xf058<br/>   |
| GESTE \_ NACH UNTEN<br/>              | 0xf059<br/>   |
| GESTE \_ NACH LINKS<br/>              | 0xf05a<br/>   |
| GESTE \_ NACH RECHTS<br/>             | 0xf05b<br/>   |
| GESTE \_ NACH OBEN \_<br/>          | 0xf060<br/>   |
| \_ \_ NACH-OBEN-GESTE<br/>          | 0xf061<br/>   |
| GESTE \_ LINKS \_ RECHTS<br/>       | 0xf062<br/>   |
| GESTE \_ RECHTS \_ LINKS<br/>       | 0xf063<br/>   |
| GESTE \_ NACH \_ OBEN LINKS \_ LONG<br/>    | 0xf064<br/>   |
| GESTE \_ \_ NACH OBEN RECHTS \_ LONG<br/>   | 0xf065<br/>   |
| GESTE \_ NACH \_ UNTEN LINKS \_ LANG<br/>  | 0xf066<br/>   |
| GESTE \_ \_ NACH UNTEN RECHTS \_ LONG<br/> | 0xf067<br/>   |
| GESTE \_ NACH \_ OBEN LINKS<br/>          | 0xf068<br/>   |
| GESTE \_ NACH \_ OBEN RECHTS<br/>         | 0xf069<br/>   |
| GESTE \_ NACH \_ LINKS<br/>        | 0xf06a<br/>   |
| GESTE \_ NACH UNTEN \_ RECHTS<br/>       | 0xf06b<br/>   |
| GESTE \_ NACH \_ OBEN<br/>          | 0xf06c<br/>   |
| GESTE \_ NACH \_ LINKS<br/>        | 0xf06d<br/>   |
| GESTE \_ NACH \_ OBEN<br/>         | 0xf06e<br/>   |
| GESTE \_ NACH UNTEN \_<br/>       | 0xf06f<br/>   |
| \_GESTEN-AUSRUFEZEICHEN<br/>       | 0xf0a4<br/>   |
| GESTEN \_ TIPPEN<br/>               | 0xf0f0<br/>   |
| \_GESTENDOPPEL \_ TIPPEN<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Nichtimplementierte Gesten



| Gestenname                             | Unicode-Bereichswert |
|------------------------------------------|---------------------|
| GESTURE \_ INFINITY<br/>             | 0xf006<br/>   |
| \_GESTENKREUZ<br/>                | 0xf007<br/>   |
| GESTEN \_ ABSATZ<br/>            | 0xf008<br/>   |
| \_GESTENABSCHNITT<br/>              | 0xf009<br/>   |
| \_GESTEN-AUFZÄHLUNGSZEICHEN<br/>               | 0xf00a<br/>   |
| \_GESTEN-AUFZÄHLUNGSKREUZ \_<br/>        | 0xf00b<br/>   |
| \_GESTENSQUIGGLE<br/>             | 0xf00c<br/>   |
| \_GESTENAUSTAUSCH<br/>                 | 0xf00d<br/>   |
| \_GESTEN-OPENUP<br/>               | 0xf00e<br/>   |
| GESTURE \_ CLOSEUP<br/>              | 0xf00f<br/>   |
| \_GESTENRECHTECK<br/>            | 0xf012<br/>   |
| \_ \_ GESTENKREIS TIPPEN<br/>          | 0xf022<br/>   |
| \_ \_ GESTENKREISKREIS<br/>       | 0xf023<br/>   |
| \_ \_ GESTENKREISKREUZ<br/>        | 0xf025<br/>   |
| \_GESTENKREISLINIE \_ \_ VERT<br/>   | 0xf026<br/>   |
| \_ \_ \_ GESTENKREISLINIEN-HORZ<br/>   | 0xf027<br/>   |
| GESTE \_ \_ DOPPELPFEIL \_ NACH OBEN<br/>    | 0xf03c<br/>   |
| GESTE \_ MIT \_ DOPPELPFEIL \_ NACH UNTEN<br/>  | 0xf03d<br/>   |
| GESTE \_ \_ DOPPELPFEIL \_ NACH LINKS<br/>  | 0xf03e<br/>   |
| GESTE \_ \_ DOPPELPFEIL \_ NACH RECHTS<br/> | 0xf03f<br/>   |
| GESTE \_ NACH OBEN \_ NACH \_ LINKS<br/>      | 0xf040<br/>   |
| \_ \_ \_ NACH-RECHTS-GESTE<br/>     | 0xf041<br/>   |
| GESTE \_ NACH UNTEN \_ NACH \_ LINKS<br/>    | 0xf042<br/>   |
| GESTE \_ NACH UNTEN \_ NACH \_ RECHTS<br/>   | 0xf043<br/>   |
| GESTE \_ NACH LINKS \_ NACH \_ OBEN<br/>      | 0xf044<br/>   |
| GESTE \_ \_ \_ NACH-LINKS-TASTE NACH UNTEN<br/>    | 0xf045<br/>   |
| GESTE \_ NACH RECHTS \_ NACH \_ OBEN<br/>     | 0xf046<br/>   |
| GESTE \_ \_ \_ NACH-RECHTS-TASTE NACH UNTEN<br/>   | 0xf047<br/>   |
| GESTE \_ \_ DIAGONALE NACH-LINKS-AKTION<br/>     | 0xf05c<br/>   |
| GESTE \_ \_ DIAGONALE NACH RECHTS<br/>    | 0xf05d<br/>   |
| GESTE \_ DIAGONAL \_ LEFTDOWN<br/>   | 0xf05e<br/>   |
| \_GESTENDIAGONALE \_ NACH-RECHTS-ABDRÜCKUNG<br/>  | 0xf05f<br/>   |
| \_GESTENBUCHSTABE \_ A<br/>            | 0xf080<br/>   |
| \_GESTENBUCHSTABE \_ B<br/>            | 0xf081<br/>   |
| \_GESTENBUCHSTABE \_ C<br/>            | 0xf082<br/>   |
| \_GESTENBUCHSTABE \_ D<br/>            | 0xf083<br/>   |
| \_GESTENBUCHSTABE \_ E<br/>            | 0xf084<br/>   |
| \_GESTENBUCHSTABE \_ F<br/>            | 0xf085<br/>   |
| \_GESTENBUCHSTABE \_ G<br/>            | 0xf086<br/>   |
| \_GESTENBUCHSTABE \_ H<br/>            | 0xf087<br/>   |
| \_GESTENBUCHSTABE \_ I<br/>            | 0xf088<br/>   |
| \_GESTENBUCHSTABE \_ J<br/>            | 0xf089<br/>   |
| \_GESTENBUCHSTABE \_ K<br/>            | 0xf08a<br/>   |
| \_GESTENBUCHSTABE \_ L<br/>            | 0xf08b<br/>   |
| \_GESTENBUCHSTABE \_ M<br/>            | 0xf08c<br/>   |
| \_GESTENBUCHSTABE \_ N<br/>            | 0xf08d<br/>   |
| \_GESTENBUCHSTABE \_ O<br/>            | 0xf08e<br/>   |
| \_GESTENBUCHSTABE \_ P<br/>            | 0xf08f<br/>   |
| \_GESTENBUCHSTABE \_ Q<br/>            | 0xf090<br/>   |
| \_GESTENBUCHSTABEN \_ R<br/>            | 0xf091<br/>   |
| \_GESTENBUCHSTABEN \_ S<br/>            | 0xf092<br/>   |
| \_GESTENBUCHSTABEN \_ T<br/>            | 0xf093<br/>   |
| \_GESTENBUCHSTABEN \_ U<br/>            | 0xf094<br/>   |
| \_GESTENBUCHSTABEN \_ V<br/>            | 0xf095<br/>   |
| \_GESTENBUCHSTABEN \_ W<br/>            | 0xf096<br/>   |
| \_GESTENBUCHSTABEN \_ X<br/>            | 0xf097<br/>   |
| \_GESTENBUCHSTABEN \_ Y<br/>            | 0xf098<br/>   |
| \_GESTENBUCHSTABEN \_ Z<br/>            | 0xf099<br/>   |
| \_GESTENZIFFER \_ 0<br/>             | 0xf09a<br/>   |
| \_GESTENZIFFER \_ 1<br/>             | 0xf09b<br/>   |
| \_GESTENZIFFER \_ 2<br/>             | 0xf09c<br/>   |
| \_GESTENZIFFER \_ 3<br/>             | 0xf09d<br/>   |
| \_GESTENZIFFER \_ 4<br/>             | 0xf09e<br/>   |
| \_GESTENZIFFER \_ 5<br/>             | 0xf09f<br/>   |
| \_GESTENZIFFER \_ 6<br/>             | 0xf0a0<br/>   |
| \_GESTENZIFFER \_ 7<br/>             | 0xf0a1<br/>   |
| \_GESTENZIFFER \_ 8<br/>             | 0xf0a2<br/>   |
| \_GESTENZIFFER \_ 9<br/>             | 0xf0a3<br/>   |
| \_GESTENFRAGE<br/>             | 0xf0a5<br/>   |
| \_GESTEN-SHARP<br/>                | 0xf0a6<br/>   |
| \_GESTEN-DOLLAR<br/>               | 0xf0a7<br/>   |
| \_GESTEN-STERNCHEN<br/>             | 0xf0a8<br/>   |
| GESTE \_ PLUS<br/>                 | 0xf0a9<br/>   |
| GESTE \_ DOPPELT \_ NACH OBEN<br/>           | 0xf0b8<br/>   |
| GESTE \_ DOPPELT \_ NACH UNTEN<br/>         | 0xf0b9<br/>   |
| GESTE \_ DOUBLE \_ LEFT<br/>         | 0xf0ba<br/>   |
| GESTE \_ DOPPELT \_ RECHTS<br/>        | 0xf0bb<br/>   |
| GESTE \_ DREIFACH \_ NACH OBEN<br/>           | 0xf0bc<br/>   |
| GESTE \_ TRIPLE \_ DOWN<br/>         | 0xf0bd<br/>   |
| GESTE \_ TRIPLE \_ LEFT<br/>         | 0xf0be<br/>   |
| GESTE \_ TRIPLE \_ RIGHT<br/>        | 0xf0bf<br/>   |
| \_GESTENKLAMMER \_ ÜBER<br/>        | 0xf0e4<br/>   |
| \_GESTENKLAMMER \_ UNTER<br/>       | 0xf0e5<br/>   |
| \_GESTENKLAMMER \_ LINKS<br/>        | 0xf0e6<br/>   |
| \_GESTENKLAMMER \_ RECHTS<br/>       | 0xf0e7<br/>   |
| \_GESTENKLAMMER \_ ÜBER<br/>          | 0xf0e8<br/>   |
| \_GESTENKLAMMER \_ UNTER<br/>         | 0xf0e9<br/>   |
| \_GESTENKLAMMER \_ NACH LINKS<br/>          | 0xf0ea<br/>   |
| \_GESTENKLAMMER \_ RECHTS<br/>         | 0xf0eb<br/>   |
| GESTE \_ – \_ DREIFACHES TIPPEN<br/>          | 0xf0f2<br/>   |
| \_ \_ GESTEN-QUAD-TIPPEN<br/>            | 0xf0f3<br/>   |



 

 

 




