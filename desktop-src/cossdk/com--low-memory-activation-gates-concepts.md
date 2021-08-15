---
description: COM+ versucht, Situationen zu verhindern, in denen diese Fehlerpfade auf einem Server ausgeführt werden müssen.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: COM+ Low-Memory Activation Gates Concepts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b4c34e10dcb18a88566d1bc45bb6751e500767c34a2e17cf8cdf12f0f1930c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129177"
---
# <a name="com-low-memory-activation-gates-concepts"></a>COM+ Low-Memory Activation Gates Concepts

Im Allgemeinen ist keine Synchronisierung erforderlich, wenn Sie über ein Singlethread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt. Die Synchronisierung wird wichtig, wenn Sie über ein Multithread-Apartment (MTA) und ein Freethread-Objekt verfügen. In der Vergangenheit mussten Freethread-Objekte sperren. Sie können das Sperren vermeiden, indem Sie das Synchronisierungsattribut für eine Komponente festlegen.

Zuverlässigkeitsprobleme treten häufig auf, wenn die Ressourcen eines Servers nicht effizient auf Spitzenlasten reagieren können. Wenn ein Server nicht über genügend physische Ressourcen verfügt, um den Spitzenbedarf zu erfüllen, kann er den virtuellen Arbeitsspeicher erschöpfen. Dies wird zu einem Problem, wenn der Benutzercode oder Systemcode Speicherbelegungsfehler nicht ordnungsgemäß verarbeitet. Der Server verlangsamt sich, und wenn der Arbeitsspeicher erschöpft ist, tritt bei der Speicherbelegung ein Fehler auf. Der Server führt Fehlerpfade aus, um die Zuordnungsfehler zu behandeln. Wenn ein Fehlerpfad einen Fehler im System- oder Benutzercode enthält, der auf dem Server ausgeführt wird, ist es äußerst schwierig, sicher abzufangen und zu behandeln.

COM+ versucht, Situationen zu verhindern, in denen diese Fehlerpfade auf einem Server ausgeführt werden müssen. Durch das Feature "Aktivierungsgates mit geringem Arbeitsspeicher" überwacht COM+ proaktiv die Speicherauslastung im System und stellt sicher, dass vor der Ausführung von Benutzercode eine angemessene Menge an Arbeitsspeicher verfügbar ist. Wenn der Prozentsatz des für die Anwendung verfügbaren virtuellen Arbeitsspeichers unter einen festen Schwellenwert fällt, schlägt die Aktivierung fehl, bevor eine COM+-Serveranwendung oder ein COM+-Serverobjekt erstellt wird (wie in der folgenden Abbildung dargestellt). Wenn diese Normalerweise ausgeführten Aktivierungen fehlschlagen, minimiert das Feature "Aktivierungsgates mit geringem Arbeitsspeicher" die Probleme im Zusammenhang mit Speicherbelegungen im Benutzercode, was die Systemzuverlässigkeit erheblich verbessert.

![Diagramm, das die Beziehung zwischen einer COM+-Anwendung und einem Aktivierungsgate mit geringem Arbeitsspeicher zeigt.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

Das Feature "Aktivierungsgates mit geringem Arbeitsspeicher" gilt nur für konfigurierte COM-Komponenten, die in einer COM+-Anwendung installiert sind.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Funktionsweise des Low-Memory Activation Gates-Features

Das Feature "Aktivierungsgates mit geringem Arbeitsspeicher" verwendet je nach Aktivierungstyp einen anderen festen Schwellenwert. Beim Erstellen einer COM+-Serveranwendung ermöglicht COM+ die Aktivierung, wenn mehr als 10 Prozent des virtuellen Arbeitsspeichers verfügbar sind. Wenn weniger als 10 Prozent verfügbar sind, stellt COM+ eine Testzuordnung bereit, um herauszufinden, ob die Auslagerungsdatei erweitert werden kann, um die neue Speicherauslastung zu bewältigen. Wenn die Auslagerungsdatei erweitert wird, wird die Serveranwendung erstellt. Wenn die Auslagerungsdatei nicht erweitert werden kann, schlägt die Aktivierung fehl, und der Arbeitsspeicher wird nicht zugeordnet.

Der Prozess ist beim Erstellen eines Objekts ähnlich. In diesem Fall ermöglicht COM+ die Aktivierung, wenn mehr als 5 Prozent des virtuellen Arbeitsspeichers verfügbar sind. Wenn weniger als 5 Prozent verfügbar sind, fährt COM+ mit einer Testzuordnung fort. Wenn die Testzuordnung die Auslagerungsdatei erweitert, wird das -Objekt erstellt. Wenn nicht, schlägt die Aktivierung fehl.

Die festen Schwellenwerte für Aktivierungsgates mit geringem Arbeitsspeicher sind derzeit nicht konfigurierbar. Aus diesem Grund sind dieser Funktion keine Aufgaben zugeordnet.

 

 



