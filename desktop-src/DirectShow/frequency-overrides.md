---
description: Überschreibungs Überschreitungen
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Überschreibungs Überschreitungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520659"
---
# <a name="frequency-overrides"></a>Überschreibungs Überschreitungen

Es wurde ein erheblicher Aufwand aufgewendet, um sicherzustellen, dass die Übertragungs Häufigkeits-und Farbstandard Zuweisungen für jedes Land/jede Region korrekt sind. Es gibt auch Situationen, in denen die Häufigkeits Tabellen nicht ausreichen, Fehler enthalten oder veraltet sind. Um dieses Problem zu beheben, werden die Häufigkeits Tabellen der TV-Tuner-Filter möglicherweise selektiv überschrieben, indem der folgende Registrierungsschlüssel verwendet wird:

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **TV System Services** \\ **tvautotune** \\ **TS0-1**

> [!Note]  
> Ab Windows 7 wird der folgende umgeleitete Registrierungsschlüssel für x86-Anwendungen verwendet, die in x64-Versionen von Windows ausgeführt werden:

 

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **tvautotune** \\ **TS0-1**

Häufigkeits Überschreibungen werden in Anwendungs definierte "optimierungsbereiche" gruppiert, die nach Zahl identifiziert werden. Das folgende Beispiel zeigt eine Beispiel Überschreibung:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

In diesem Fall weist "TS0-1" auf den Optimierungs Bereich 0 für Kabel häufigerungen hin. Die erste Zahl identifiziert den Optimierungs Bereich. Die zweite Zahl ist entweder 0 für Broadcast Häufigkeiten oder 1 für Kabel Häufigkeiten.

Der Unterschlüssel mit dem Namen "12" überschreibt den Frequency-Wert für die Häufigkeit bei Index 12 in der aktuellen Häufigkeits Tabelle. Der Wert des unter Schlüssels ist ein **DWORD** -Wert, der die Häufigkeit in Hertz (Hz) angibt. In diesem Beispiel wird die Häufigkeit auf 67,25 MHz festgelegt. Außer Kraft setzungen können für alle Kanalnummern im Bereich zwischen 1 und 999 (einschließlich) definiert werden. Wenn die Optimierungs Hardware eine bestimmte Häufigkeit nicht unterstützt, tritt bei der Tune-Anforderung ein Fehler auf.

Dieser Mechanismus kann auch verwendet werden, um neue Kanalnummern außerhalb des vorhandenen Bereichs in der Häufigkeits Tabelle zu erstellen. Die [**iamtuner:: channelminmax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) -Methode gibt den erweiterten Kanalbereich zurück. Wenn der ursprüngliche Kanalbereich z. b. 1 bis 158 lautet und eine Kanal Überschreibung von "200" zur Registrierung hinzugefügt wird, gibt die **channelminmax** -Methode 200 als maximalen Kanal zurück. In diesem Fall werden den Kanalnummern im Bereich von 159 bis 199 keine Frequenzen zugewiesen, sodass alle Optimierungs Anforderungen in diesem Bereich automatisch fehlschlagen.

Die [**iamtuner::p UT \_ tuningspace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) -Methode ermöglicht der Anwendung die Auswahl der zu verwendenden außer Kraft setzungen und der fein Optimierungs Informationen. Der Optimierungs Bereich ist beliebig. Es liegt in der Verantwortung der Anwendung, die Beziehung zwischen dem Optimierungs Bereich und der Häufigkeits Tabelle aufrechtzuerhalten. Der einfachste Ansatz besteht darin, den Länder-/Regionscode als Optimierungs Raum Nummer zu verwenden. Jedes Mal, wenn die Anwendung zu einem neuen Land-/Regionscode wechselt, wechselt Sie auch in denselben Optimierungs Bereich (in dieser Reihenfolge).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Analog-TV-Optimierung](international-analog-tv-tuning.md)
</dt> </dl>

 

 



