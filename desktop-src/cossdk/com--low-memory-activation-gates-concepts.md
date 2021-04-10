---
description: Com+ versucht, Situationen zu vermeiden, in denen diese Fehler Pfade auf einem Server ausgeführt werden müssen.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Konzepte der com+-Low-Memory Activation Gates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d844a0492301ef067f5b3cd0e0749ec3a21779
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103961055"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Konzepte der com+-Low-Memory Activation Gates

Im Allgemeinen ist die Synchronisierung nicht erforderlich, wenn Sie über ein Single Thread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt. Die Synchronisierung wird wichtig, wenn Sie über ein Multithread-Apartment (MTA) und ein Freethread-Objekt verfügen. In der Vergangenheit mussten frei Thread Objekte Sperren behandeln. Sie können die Verwendung von Sperren ausschließen, indem Sie das Synchronisierungs Attribut für eine Komponente festlegen.

Zuverlässigkeitsprobleme treten häufig auf, wenn die Ressourcen eines Servers nicht effizient auf Spitzenlasten reagieren können. Wenn ein Server nicht über genügend physische Ressourcen verfügt, um den Spitzenbedarf zu erfüllen, kann der virtuelle Arbeitsspeicher erschöpft werden. Dies wird zu einem Problem, wenn der Benutzercode oder der Systemcode Fehler bei der Speicher Belegung nicht ordnungsgemäß behandelt. Der Server beginnt mit der Verlangsamung, und die Speicher Belegung schlägt fehl, wenn der Arbeitsspeicher erschöpft ist. Der Server führt Fehler Pfade zum Behandeln der Zuordnungs Fehler aus. Wenn ein Fehler Pfad einen Fehler im System-oder Benutzercode enthält, der auf dem Server ausgeführt wird, ist es äußerst schwierig, sicher abzufangen und zu verarbeiten.

Com+ versucht, Situationen zu vermeiden, in denen diese Fehler Pfade auf einem Server ausgeführt werden müssen. Über das Feature für Aktivierungs Gates mit geringem Arbeitsspeicher überwacht com+ proaktiv die Arbeitsspeicher Auslastung im System und stellt sicher, dass vor dem Ausführen des Benutzercodes eine angemessene Menge an Arbeitsspeicher verfügbar ist. Wenn der Prozentsatz des für die Anwendung verfügbaren virtuellen Speichers unter einen festgelegten Schwellenwert fällt, schlägt die Aktivierung fehl, bevor eine COM+-Serveranwendung oder ein COM+-Objekt erstellt wird (wie in der Abbildung unten dargestellt). Durch das Fehlschlagen dieser Aktivierungen, die normalerweise ausgeführt werden, minimiert die Funktion für die Aktivierung des niedrigen Arbeitsspeichers die Probleme, die im Zusammenhang mit Speicher Belegungen im Benutzercode auftreten, wodurch die Systemzuverlässigkeit deutlich

![Diagramm, das die Beziehung zwischen einer COM+-Anwendung und einem Aktivierungs Gate mit geringem Arbeitsspeicher anzeigt.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

Das Feature für Aktivierungs Gates mit geringem Arbeitsspeicher gilt nur für konfigurierte COM-Komponenten, die in einer COM+-Anwendung installiert sind.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Funktionsweise der Funktion "Low-Memory Activation Gates"

Die Funktion für die Aktivierung der Funktion für niedrige Arbeitsspeicher verwendet je nach Art der Aktivierung einen anderen festgelegten Schwellenwert. Beim Erstellen einer COM+-Serveranwendung ermöglicht com+ die Aktivierung, wenn mehr als 10 Prozent des virtuellen Arbeitsspeichers verfügbar sind. Wenn weniger als 10 Prozent verfügbar sind, erstellt com+ eine Test Zuordnung, um herauszufinden, ob die Auslagerungs Datei erweitert werden kann, um die neue Arbeitsspeicher Auslastung zu ermöglichen. Wenn die Auslagerungs Datei erweitert wird, wird die Serveranwendung erstellt. Wenn die Auslagerungs Datei nicht erweitert werden kann, schlägt die Aktivierung fehl, und der Arbeitsspeicher wird nicht zugeordnet.

Der Prozess ist ähnlich, wenn ein Objekt erstellt wird. In diesem Fall ermöglicht com+ die Aktivierung, wenn mehr als 5 Prozent des virtuellen Arbeitsspeichers verfügbar sind. Wenn weniger als 5 Prozent verfügbar sind, fährt com+ mit einer Test Zuordnung fort. Wenn die Test Zuordnung die Auslagerungs Datei erweitert, wird das-Objekt erstellt. Andernfalls tritt ein Fehler bei der Aktivierung auf.

Die festgelegten Schwellenwerte für Aktivierungs Gates mit geringem Arbeitsspeicher können derzeit nicht konfiguriert werden. Aus diesem Grund sind dieser Funktion keine Aufgaben zugeordnet.

 

 



