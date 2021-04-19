---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Windows 7-Unterstützung für Intel AVX aktivieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362722"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Windows 7-Unterstützung für Intel AVX aktivieren

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** : Windows 7 SP1  
**Server** -Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Intel<sup>?</sup> Erweiterte Vektor Erweiterungen (AVX)<sup>?</sup> ist eine 256-Bit-SIMD-Gleit Komma-Vektor Erweiterung der Intel-Architektur. Sie enthält Erweiterungen für Anweisungs-und Register Sätze.

Microsoft hat einige API-Erweiterungen entwickelt, wie z. b. xstate-Funktionen, mit denen Anwendungen auf Informationen und den Status erweiterter Prozessor Features zugreifen und diese bearbeiten können (einschließlich AVX).

## <a name="usage-scenarios"></a>Verwendungsszenarien

Es gibt drei allgemeine Ebenen der möglichen Auswirkung.

**Ebene 1:** Anwendungen, die Intel AVX nicht direkt verwenden, sehen keinerlei Auswirkung auf ihre Funktionalität, auch wenn Sie Bibliotheken aufzurufen oder Compiler verwenden, die indirekt Intel AVX-Erweiterungen verwenden oder generieren. Dies stellt die Mehrzahl der Anwendungen dar.

**Ebene 2:** Erweiterte Anwendungen, die den Intel AVX-Anweisungs Satz explizit verwenden, sind in der Lage, auf AVX-Register Inhalte zuzugreifen und diese zu ändern, wenn eine Hardware Ausnahme ausgelöst wird. Eine sehr geringe Anzahl von Anwendungen würde in diese Kategorie fallen, da Sie eine intime Kenntnis des Anweisungs Datenstroms impliziert, der zum Zeitpunkt der Ausnahme ausgeführt wird, z. b. Anwendungen mit Abschnitten, die in der Assemblysprache geschrieben wurden, oder solche, die zur Laufzeit Computercode generieren (z. b. Laufzeiten für verwalteten Code mit Just-in-Time-Kompilierung

**Ebene 3:** Debugger-Anwendungen können in der Anwendung, die gedebuggt wird, auf den AVX-Zustand zugreifen und ihn bearbeiten.

## <a name="how-to-leverage-feature-capabilities"></a>Funktionsweise von Featurefunktionen

**Ebene 1:** Es ist keine Aktion erforderlich, damit Anwendungen Intel AVX verwenden können.

**Ebene 2:** Anwendungen in dieser Kategorie haben die Möglichkeit, zum Zeitpunkt der Ausnahme innerhalb ihrer Ausnahme Filter auf den AVX-Zustand zuzugreifen und ihn zu bearbeiten. Nachdem Sie den Basis Prozessor Kontext über GetExceptionInformation erhalten haben, sollten Filter folgende Aktionen ausführen:

 **1.** überprüfen Sie den Wert des **context- \_ xstate** -Flags. Dieses Flag gibt an, dass mindestens eine xstate-Funktion im Kontext vorhanden ist.  
**2.** wenn dies der Fall ist, können Sie **getxstatefeaturesmask** aufrufen und den Wert des **xstate- \_ AVX** -Flags in der zurückgegebenen Maske testen. Dies gibt an, dass der AVX-Zustand im Kontext vorhanden ist.  
**3.** rufen Sie **Lo-exstatefeature** auf, um den tatsächlichen Speicherort abzurufen, an dem der AVX-Status gespeichert wird.  

**Ebene 3:** Es ist nicht erforderlich, vorhandene Debugger-Anwendungen zu aktualisieren, es sei denn, Sie möchten auf die Intel AVX-Register zugreifen:

**1.** um zu ermitteln, ob AVX aktiviert ist, sollte der Debugger Folgendes verwenden:

-   Getenabledxstatefeatures, um eine Maske von aktivierten xstate-Features auf x86-oder x64-Prozessoren zu erhalten, um zu bestimmen, welche Features auf dem System vorhanden und aktiviert sind, bevor Sie eine xstate-Prozessor Funktion verwenden oder xstate-Kontexte bearbeiten.

  
**2.** wenn AVX vorhanden ist und Sie den AVX-Zustand von der zu debuggenden Anwendung abrufen und bearbeiten möchten (z. b. GetThreadContext und SetThreadContext), sollte der Debugger Folgendes verwenden:

-   Initializecontext-Funktion zum Initialisieren einer Kontext Struktur in einem Puffer mit der erforderlichen Größe und Ausrichtung
-   Copycontext-Funktion zum Kopieren einer Quell Kontext Struktur (einschließlich eines beliebigen xstate) in eine initialisierte Ziel Kontext Struktur

  
**3.** zum Testen, festlegen und suchen des AVX-Zustands innerhalb eines Prozessor Kontexts sollte der Debugger Folgendes verwenden:

-   Locatcher exstatefeature zum Abrufen eines Zeigers auf den Prozessor Zustand für eine einzelne xstate-Funktion innerhalb einer Kontext Struktur
-   Getxstatefeaturesmask zum Zurückgeben der Maske von xstate-Funktionen, die innerhalb einer Kontext Struktur festgelegt sind.
-   Setxstatefeaturesmask zum Festlegen der Maske von xstate-Funktionen, die innerhalb einer Kontext Struktur festgelegt sind.

  


## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   Informationen zu den xstate-Funktionen in der Windows SDK finden Sie unter [Debuggingfunktionen](../debug/debugging-functions.md).
-   Eine Übersicht über die Anweisungen und Funktionen von Intel AVX finden Sie unter [Intel AVX: New Frontiers in Performance Verbesserungen und Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
