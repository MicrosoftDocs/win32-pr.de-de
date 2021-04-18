---
description: 'Beim Implementieren ihrer eigenen Microsoft-Gestenerkennung müssen Sie den Wert für Name und Unicode-Bereich für jede Geste definieren, die ihre Erkennung erkennen soll. Wenn Sie sich entschließen, die Gesten zu implementieren, die bereits als Teil der Microsoft Gestenerkennung unterstützt oder definiert wurden, verwenden Sie die definierten Namen und Unicode-Bereichs Werte für diese Gesten. Die gesamte Auflistung von Namen und Unicode-Bereichs Werten sowohl für implementierte als auch nicht implementierte Gesten in der Microsoft Gestenerkennung wird in der Header Datei "recdefs. h" bereitgestellt (standardmäßig installiert in C: \\ Programme \\ Microsoft Tablet PC Platform SDK \\ include). Die Gesten Namen und Unicode-Bereichs Werte werden auch in den folgenden Tabellen aufgeführt. Beachten Sie, dass die Gesten- \_ null-Geste verwendet wird, um anzugeben, dass eine Erkennung die Eingabe nicht als Geste erkennt.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Unicode-Bereichs Werte von Gesten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b66b9b4ee511e9eeadd79e0dff2675391ceee6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358546"
---
# <a name="unicode-range-values-of-gestures"></a>Unicode-Bereichs Werte von Gesten

Beim Implementieren ihrer eigenen Microsoft-Gestenerkennung müssen Sie den Wert für Name und Unicode-Bereich für jede Geste definieren, die ihre Erkennung erkennen soll.

Wenn Sie sich entschließen, die Gesten zu implementieren, die bereits als Teil der Microsoft Gestenerkennung unterstützt oder definiert wurden, verwenden Sie die definierten Namen und Unicode-Bereichs Werte für diese Gesten. Die gesamte Auflistung von Namen und Unicode-Bereichs Werten sowohl für implementierte als auch nicht implementierte Gesten in der Microsoft Gestenerkennung wird in der Header Datei "recdefs. h" bereitgestellt (standardmäßig installiert in C: \\ Programme \\ Microsoft Tablet PC Platform SDK \\ include). Die Gesten Namen und Unicode-Bereichs Werte werden auch in den folgenden Tabellen aufgeführt.

> [!Note]  
> Die Gesten- \_ null-Geste wird verwendet, um anzugeben, dass eine Erkennung die Eingabe nicht als Geste erkennt.

 

## <a name="implemented-gestures"></a>Implementierte Gesten



| Gesten Name                          | Unicode-Bereichs Wert |
|---------------------------------------|---------------------|
| Geste \_ null<br/>              | 0xF<br/>   |
| Gesten \_ ScratchOut<br/>        | 0xF 001<br/>   |
| Gesten \_ Dreieck<br/>          | 0xF 002<br/>   |
| Gesten \_ Quadrat<br/>            | 0xF 003<br/>   |
| Gesten \_ Stern<br/>              | 0xF 004<br/>   |
| Gesten \_ Überprüfung<br/>             | 0xmode 005<br/>   |
| Gesten \_ Cursor<br/>          | 0xF 010<br/>   |
| Bewegung \_ doppelter \_ Cursor<br/>  | 0xF 011<br/>   |
| Gesten \_ Kreis<br/>            | 0xF 020<br/>   |
| Bewegung \_ Double- \_ Kreis<br/>    | 0xF 021<br/>   |
| Bewegung \_ Semicircle \_ Links<br/>  | 0xdie<br/>   |
| Bewegung \_ Semicircle \_ Rechts<br/> | 0xF.<br/>   |
| Gesten- \_ Chevron \_<br/>       | 0xF 030<br/>   |
| Bewegung \_ Chevron \_ nach unten<br/>     | 0xF.<br/>   |
| Bewegung \_ Chevron \_ Links<br/>     | 0xF 032<br/>   |
| Bewegung \_ Chevron \_ right<br/>    | 0xF 033<br/>   |
| Gesten \_ Pfeil nach \_ oben<br/>         | 0xF.<br/>   |
| Gesten \_ Pfeil \_ nach unten<br/>       | 0xF 039<br/>   |
| Gesten \_ Pfeil \_ Links<br/>       | 0xF 03a<br/>   |
| Gesten \_ Pfeil nach \_ Rechts<br/>      | 0xF 03b<br/>   |
| Bewegung nach \_ oben<br/>                | 0xF<br/>   |
| Bewegung \_ nach unten<br/>              | 0xF 059<br/>   |
| Bewegung nach \_ Links<br/>              | 0xF 05A<br/>   |
| Gesten nach \_ Rechts<br/>             | 0xF 05b<br/>   |
| Bewegung \_ \_ nach oben<br/>          | 0xF.<br/>   |
| Bewegung \_ nach \_ oben<br/>          | 0xF 061<br/>   |
| Gesten \_ Links nach \_ Rechts<br/>       | 0xma062<br/>   |
| Bewegung \_ rechts \_ Links<br/>       | 0xF 063<br/>   |
| Bewegung \_ nach \_ Links \_<br/>    | 0xF.<br/>   |
| Bewegung \_ auf der \_ rechten Seite \_<br/>   | 0xF 065<br/>   |
| Bewegung \_ nach unten \_ Links \_<br/>  | 0xF 066<br/>   |
| Bewegung \_ nach unten \_ rechts \_<br/> | 0xF 067<br/>   |
| Bewegung \_ nach \_ Links<br/>          | 0xF 068<br/>   |
| Bewegung \_ nach \_ Rechts<br/>         | 0xF.<br/>   |
| Bewegung \_ nach unten \_ Links<br/>        | 0xF 06A<br/>   |
| Bewegung \_ nach \_ Rechts<br/>       | 0xF 06b<br/>   |
| Bewegung \_ nach \_ oben<br/>          | 0xF 06c<br/>   |
| Bewegung \_ \_ nach unten<br/>        | 0xF 06D<br/>   |
| Bewegung \_ nach \_ oben<br/>         | 0xF 06E<br/>   |
| Bewegung \_ \_ nach unten<br/>       | 0xF 06f<br/>   |
| Gesten \_ Ausrufezeichen<br/>       | 0xF 0a4<br/>   |
| Bewegung \_ tippen<br/>               | 0xF 0F<br/>   |
| Geste \_ Doppel \_ tippen<br/>       | 0xF 0F<br/>   |



 

## <a name="unimplemented-gestures"></a>Nicht implementierte Gesten



| Gesten Name                             | Unicode-Bereichs Wert |
|------------------------------------------|---------------------|
| Bewegung \_ unendlich<br/>             | 0xF 006<br/>   |
| Bewegung \_ Kreuz<br/>                | 0xF 007<br/>   |
| Gesten \_ Absatz<br/>            | 0xF 008<br/>   |
| Gesten \_ Abschnitt<br/>              | 0xF 009<br/>   |
| Gesten \_ Kugel<br/>               | 0xF 00A<br/>   |
| Gesten- \_ Kugel \_ Kreuz<br/>        | 0xs00b<br/>   |
| Gesten \_ Wellenlinie<br/>             | 0x-00c<br/>   |
| Gesten \_ Austausch<br/>                 | 0xF-ID<br/>   |
| \_geöffdie Geste<br/>               | 0x-00E<br/>   |
| Gesten \_ closeup<br/>              | 0xF 00F<br/>   |
| Gesten \_ Rechteck<br/>            | 0xF<br/>   |
| Bewegung \_ Kreis \_ tippen<br/>          | 0xF 022<br/>   |
| Kreis \_ Kreis \_ Kreis<br/>       | 0xF 023<br/>   |
| Gesten \_ Kreis \_ Kreuz<br/>        | 0xF 025<br/>   |
| Bewegung \_ Kreis \_ Linie \_ Vert<br/>   | 0xF.<br/>   |
| Bewegung \_ Kreis \_ Linie \_ Horz<br/>   | 0xF 027<br/>   |
| \_Pfeil nach \_ \_ oben<br/>    | 0xF 03c<br/>   |
| \_Doppel \_ Pfeil \_ nach unten<br/>  | 0xF 03D<br/>   |
| \_Doppel \_ Pfeil nach \_ Links<br/>  | 0xF 03e<br/>   |
| \_Pfeil nach \_ \_ Rechts<br/> | 0xF 03f<br/>   |
| Gesten nach \_ oben \_ Pfeil \_ Links<br/>      | 0xF 040<br/>   |
| Bewegung nach \_ oben nach \_ \_ Rechts<br/>     | 0xF 041<br/>   |
| Bewegung \_ nach unten \_ Pfeil \_ Links<br/>    | 0xF 042<br/>   |
| Bewegung \_ nach-unten- \_ Pfeil \_ Rechts<br/>   | 0xF 043<br/>   |
| Bewegung nach \_ Links \_ Pfeil nach \_ oben<br/>      | 0xF 044<br/>   |
| Bewegung \_ \_ nach links \_ nach unten<br/>    | 0xF 045<br/>   |
| Bewegung nach \_ rechts nach \_ \_ oben<br/>     | 0xF 046<br/>   |
| Bewegung \_ \_ nach Rechtspfeil \_ nach unten<br/>   | 0xF 047<br/>   |
| Bewegung \_ diagonal \_ linkstup<br/>     | 0xF 05C<br/>   |
| Bewegung \_ diagonal \_<br/>    | 0xF 05D<br/>   |
| Bewegung \_ diagonal \_ leftdown<br/>   | 0xF 05e<br/>   |
| Bewegung \_ diagonal \_ rechts unten<br/>  | 0xF 05f<br/>   |
| Gesten \_ Buchstabe \_ A<br/>            | 0xF 080<br/>   |
| Gesten \_ Buchstabe \_ B<br/>            | 0xF 081<br/>   |
| Gesten \_ Buchstabe \_ C<br/>            | 0xF 082<br/>   |
| Gesten \_ Buchstabe \_ D<br/>            | 0xF 083<br/>   |
| Gesten \_ Buchstabe \_ E<br/>            | 0xF 084<br/>   |
| Gesten \_ Buchstabe \_ F<br/>            | 0xF 085<br/>   |
| Gesten \_ Buchstabe \_ G<br/>            | 0xF 086<br/>   |
| Gesten \_ Buchstabe \_ H<br/>            | 0xF 087<br/>   |
| Gesten \_ Buchstabe \_ I<br/>            | 0xF 088<br/>   |
| Gesten \_ Buchstabe \_ J<br/>            | 0xF 089<br/>   |
| Gesten \_ Buchstabe \_ K<br/>            | 0xF 08a<br/>   |
| Gesten \_ Buchstabe \_ L<br/>            | 0xF 08b<br/>   |
| Gesten \_ Buchstabe \_ M<br/>            | 0xF 08c<br/>   |
| Gesten \_ Buchstabe \_ N<br/>            | 0xF 08d<br/>   |
| Gesten \_ Buchstabe \_ O<br/>            | 0xF 08e<br/>   |
| Gesten \_ Buchstabe \_ P<br/>            | 0xF 08F<br/>   |
| Gesten \_ Buchstabe \_ Q<br/>            | 0xF 090<br/>   |
| Gesten \_ Buchstabe \_ R<br/>            | 0xF 091<br/>   |
| Gesten \_ Buchstabe \_ S<br/>            | 0xF.<br/>   |
| Gesten \_ Buchstabe \_ T<br/>            | 0xF 093<br/>   |
| Gesten \_ Buchstabe \_ U<br/>            | 0xF 094<br/>   |
| Gesten \_ Buchstabe \_ V<br/>            | 0xF 095<br/>   |
| Gesten \_ Buchstabe \_ W<br/>            | 0xF 096<br/>   |
| Gesten \_ Buchstabe \_ X<br/>            | 0xF 097<br/>   |
| Gesten \_ Buchstabe \_ Y<br/>            | 0xma098<br/>   |
| Gesten \_ Buchstabe \_ Z<br/>            | 0xF 099<br/>   |
| Gesten \_ Ziffer \_ 0<br/>             | 0xF 09A<br/>   |
| Gesten \_ Ziffer \_ 1<br/>             | 0xF 09b<br/>   |
| Gesten \_ Ziffer \_ 2<br/>             | 0xF 09c<br/>   |
| Gesten \_ Ziffer \_ 3<br/>             | 0xF 09d<br/>   |
| Gesten \_ Ziffer \_ 4<br/>             | 0xF 09e<br/>   |
| Gesten \_ Ziffer \_ 5<br/>             | 0xF 09F<br/>   |
| Gesten \_ Ziffer \_ 6<br/>             | 0xF 0A0<br/>   |
| Gesten \_ Ziffer \_ 7<br/>             | 0xF 0a1<br/>   |
| Gesten \_ Ziffer \_ 8<br/>             | 0xF 0a2<br/>   |
| Gesten \_ Ziffer \_ 9<br/>             | 0xF 0a3<br/>   |
| Gesten \_ Frage<br/>             | 0xF 0a5<br/>   |
| Gesten \_ Spitze<br/>                | 0xF 0a6<br/>   |
| Gesten \_ Dollar<br/>               | 0xF 0a7<br/>   |
| Gesten \_ Sternchen<br/>             | 0xF 0a8<br/>   |
| Bewegung \_ Plus<br/>                 | 0xF 0a9<br/>   |
| Geste \_ Doppel \_<br/>           | 0xF 0b8<br/>   |
| Geste \_ Doppel \_ unten<br/>         | 0xF 0B9<br/>   |
| Bewegung \_ doppelt \_ Links<br/>         | 0xF 0BA<br/>   |
| Bewegung \_ doppelt \_ Rechts<br/>        | 0xF 0BB<br/>   |
| Gesten \_ dreifach nach \_ oben<br/>           | 0xF 0BC<br/>   |
| Bewegung \_ dreifach \_ nach unten<br/>         | 0x0bd<br/>   |
| Bewegung \_ dreifach \_ Links<br/>         | 0xF<br/>   |
| Bewegung \_ Triple \_ right<br/>        | 0xF-BF<br/>   |
| Gesten \_ Klammer \_ über<br/>        | 0xF 0e4<br/>   |
| Gesten \_ Klammer \_ unter<br/>       | 0xF 0e5<br/>   |
| Gesten \_ Klammer \_ Links<br/>        | 0xF 0E6<br/>   |
| Gesten \_ Klammer \_ Rechts<br/>       | 0xF 0e7<br/>   |
| Gesten-geschweifter \_ Klammer \_<br/>          | 0xF 0e8<br/>   |
| Gesten \_ Klammer \_ unter<br/>         | 0xF 0e9<br/>   |
| Gesten \_ Klammer \_ Links<br/>          | 0xF 0Ea<br/>   |
| Gesten \_ Klammer \_ Rechts<br/>         | 0xF-EB<br/>   |
| Bewegung \_ dreifacher \_ Tap<br/>          | 0xF 0F<br/>   |
| Gesten \_ Quad \_ tippen<br/>            | 0xF 0F<br/>   |



 

 

 




