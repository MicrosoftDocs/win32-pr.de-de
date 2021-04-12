---
description: In dieser Übersicht werden mehrere XAudio2-Methoden eingeführt, die Sie als Teil eines Vorgangs Satzes aufzurufen können.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: XAudio2-Vorgangs Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218553"
---
# <a name="xaudio2-operation-sets"></a>XAudio2-Vorgangs Sätze

In dieser Übersicht werden mehrere XAudio2-Methoden eingeführt, die Sie als Teil eines Vorgangs Satzes aufzurufen können.

Mehrere XAudio2-Methoden verwenden das *operationset* -Argument, das es Ihnen ermöglicht, als Teil einer verzögerten Gruppe aufgerufen zu werden. Zu einem bestimmten Zeitpunkt können Sie einen vollständigen Satz von Änderungen gleichzeitig anwenden, indem Sie die Funktion [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem *operationset* -Bezeichner für diese Gruppe aufrufen. Der Bezeichner ist eine beliebige Zahl. Dadurch können separate Teile des Client Codes getrennte atomarische Änderungen auf das Diagramm anwenden, ohne dass Konflikte auftreten. Die empfohlene Vorgehensweise besteht darin, dass der Client immer dann einen globalen Wert erhöht, wenn er einen eindeutigen, neuen *operationsetbezeichner* generieren muss. Ein Satz von Änderungen am Diagramm, das atomarisch angewendet wird, ist garantiert ein Beispiel. Beispielsweise werden die Stimmen synchron gestartet.

Wenn Sie *operationset* auf XAUDIO2 \_ Commit now festgelegt \_ haben, wird die Änderung sofort angewendet. Sie tritt in Kraft, wenn der erste Audioverarbeitungs Durchlauf nach dem Methoden aufzurufen. Wenn Sie [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit XAUDIO2 \_ Commit all aufzurufen \_ , werden Änderungen an allen ausstehenden Vorgängen durchgeführt, unabhängig von Ihrer *operationsetkennung* .

Bestimmte Methoden treten sofort in Kraft, wenn Sie von einem XAudio2-Rückruf mit einem *operationset* von XAudio2 \_ Commit now aufgerufen werden \_ . Alle anderen Methoden, die ein *operationset* -Argument annehmen, werden erst nach dem Aufrufen der-Methode (bei Aufruf mit XAUDIO2 \_ Commit \_ ) oder nach dem Aufrufen von [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem gleichen *operationset* wirksam. Aus diesem Grund werden bestimmte Methodenaufrufe möglicherweise nicht immer in derselben Reihenfolge ausgeführt, in der Sie aufgerufen wurden.

Alle ausstehenden Vorgänge werden atomisch ausgeführt, wenn [**IXAudio2:: stopengine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) aufgerufen wird. Alle Methoden, die aufgerufen werden, während die Engine angehalten wird, treten unabhängig vom bereitgestellten *operationsetwert* sofort in Kraft. Wenn Sie die Engine neu starten, kehrt XAudio2 in den asynchronen Modus zurück.

Einfache Szenarien, in denen Vorgangs Sätze nützlich sind, sind die folgenden Beispiele.

-   Gleichzeitiges Starten mehrerer Stimmen.
-   Gleichzeitiges Senden eines Puffers an eine Stimme, Festlegen der sprach Parameter und Starten der Stimme.
-   Eine umfangreiche Änderung des Diagramms, z. b. das Verbinden aller Quell stimmen mit einer neuen Teil Mischungs Sprache.

Weitere Informationen finden Sie unter Gewusst [wie: Gruppieren von Audiomethoden als Vorgangs Satz](how-to--group-audio-methods-as-an-operation-set.md) für ein Beispiel für die Verwendung eines Vorgangs Satzes.

## <a name="operation-set-methods"></a>Vorgangs Satz Methoden

Sie können die folgenden Methoden als Teil eines Vorgangs Satzes aufzurufen.

-   [**IXAudio2SourceVoice:: exitloop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice:: setfrequendcyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D isableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice:: enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice:: setchannelvolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice:: Einstellungsparameter**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice:: Beendigung**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Wie bereits beschrieben, muss der Client Code letztendlich die Funktion [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) zum Ausführen der verzögerten Änderungen aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgangs Sätze](operation-sets.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
