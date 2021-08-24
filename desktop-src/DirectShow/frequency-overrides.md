---
description: Häufigkeitsüberschreibungen
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Häufigkeitsüberschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a2c7663e70aa0e975cee52dc630453bea1ad4121a8c91d03564fe7d7a2cb4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997839"
---
# <a name="frequency-overrides"></a>Häufigkeitsüberschreibungen

Es wurde ein erheblicher Aufwand aufgewendet, um sicherzustellen, dass die Übertragungshäufigkeiten und Farbstandardzuweisungen für jedes Land/jede Region korrekt sind. Dennoch gibt es Situationen, in denen die Häufigkeitstabellen nicht ausreichen, Fehler enthalten oder veraltet sind. Um dieses Problem zu beheben, können die in den Häufigkeitstabellen des TV Tuner-Filters aufgeführten Häufigkeiten selektiv überschrieben werden, indem der folgende Registrierungsschlüssel verwendet wird:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> Ab Windows 7 wird der folgende umgeleitete Registrierungsschlüssel für x86-Anwendungen verwendet, die auf x64-Versionen von Windows ausgeführt werden:

 

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

Häufigkeitsüberschreibungen werden in anwendungsdefinierte "Optimierungsräume" gruppiert, die anhand der Zahl identifiziert werden. Das folgende Beispiel zeigt eine Beispielüberschreibung:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

In diesem Fall gibt "TS0-1" den Optimierungsbereich 0 für Kabelfrequenzen an. Die erste Zahl identifiziert den Optimierungsbereich. Die zweite Zahl ist entweder 0 für Übertragungsfrequenzen oder 1 für Kabelfrequenzen.

Der Unterschlüssel mit dem Namen "12" überschreibt den Frequency-Wert für die Häufigkeit bei Index 12 in der aktuellen Frequency-Tabelle. Der Wert des Unterschlüssels ist ein **DWORD,** das die Häufigkeit in Hertz (Hz) angibt. In diesem Beispiel wird die Frequenz auf 67,25 MHz festgelegt. Außerkraftsetzungen können für alle Kanalnummern im Bereich von 1 bis einschließlich 999 definiert werden. Wenn die Optimierungshardware eine bestimmte Häufigkeit nicht unterstützt, schlägt die Optimierungsanforderung fehl.

Dieser Mechanismus kann auch verwendet werden, um neue Kanalnummern außerhalb des vorhandenen Bereichs in der Häufigkeitstabelle zu erstellen. Die [**IAMTuner::ChannelMinMax-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) gibt den erweiterten Kanalbereich zurück. Wenn der ursprüngliche Kanalbereich beispielsweise 1 bis 158 betrug und der Registrierung eine Kanalüberschreibung von "200" hinzugefügt wird, gibt die **ChannelMinMax-Methode** 200 als maximalen Kanal zurück. In diesem Fall werden Kanalnummern im Bereich von 159 bis 199 keine Frequenzen zugewiesen, sodass alle Optimierungsanforderungen in diesem Bereich automatisch fehlschlagen.

Mit der [**IAMTuner::p ut \_ TuningSpace-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) kann die Anwendung auswählen, welche Außerkraftsetzungen und Optimierungsinformationen verwendet werden sollen. Optimierungsraumnummern sind willkürlich. Es liegt in der Verantwortung der Anwendung, die Beziehung zwischen dem Optimierungsbereich und der Häufigkeitstabelle beizubehalten. Der einfachste Ansatz besteht darin, den Länder-/Regionscode als Optimierungsraumnummer zu verwenden. Wenn die Anwendung dann zu einem neuen Länder-/Regionscode wechselt, wechselt sie auch zum gleichen Optimierungsbereich (in dieser Reihenfolge).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Analog TV-Optimierung](international-analog-tv-tuning.md)
</dt> </dl>

 

 



