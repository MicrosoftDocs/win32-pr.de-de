---
description: Aktivieren der Windows 7-Unterstützung für Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Aktivieren der Windows 7-Unterstützung für Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1509bac62634c85aa733b2c1de0c152169ac6cda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088458"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Aktivieren der Windows 7-Unterstützung für Intel AVX

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** – Windows 7 SP1  
**Server** – Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>BESCHREIBUNG

Intel<sup>?</sup> Advanced Vector Extensions (AVX)<sup>?</sup> ist eine 256-Bit-SIMD-Gleitkommavektorerweiterung der Intel-Architektur. Sie enthält Erweiterungen für Anweisungs- und Registersätze.

Microsoft hat einige API-Erweiterungen entwickelt, z. B. XState-Funktionen, mit denen Anwendungen auf erweiterte Prozessorfeatureinformationen und -zustände zugreifen und diese bearbeiten können, einschließlich AVX.

## <a name="usage-scenarios"></a>Verwendungsszenarien

Es gibt drei allgemeine Ebenen potenzieller Auswirkungen.

**Ebene 1:** Anwendungen, die Intel AVX nicht direkt verwenden, haben keine Auswirkungen auf ihre Funktionalität, selbst wenn sie Bibliotheken aufrufen oder Compiler verwenden, die intel AVX-Erweiterungen indirekt verwenden oder generieren. Dies stellt den weitaus größten Teil der Anwendungen dar.

**Ebene 2:** Erweiterte Anwendungen, die explizit den Intel AVX-Anweisungssatz verwenden, können auf AVX-Registerinhalte zugreifen und diese ändern, wenn eine Hardwareausnahme ausgelöst wird. Eine sehr kleine Anzahl von Anwendungen würde in diese Kategorie fallen, da sie ein fundiertes Wissen über den Anweisungsstream impliziert, der zum Zeitpunkt der Ausnahme ausgeführt wird, z. B. Anwendungen mit Abschnitten, die in der Assemblysprache geschrieben sind, oder solche, die Computercode zur Laufzeit generieren (z. B. Laufzeiten von verwaltetem Code mit Just-in-Time-Kompilierung).

**Ebene 3:** Debuggeranwendungen können auf den AVX-Status in der zu debuggenden Anwendung zugreifen und diesen bearbeiten.

## <a name="how-to-leverage-feature-capabilities"></a>Nutzen von Featurefunktionen

**Ebene 1:** Es ist keine Aktion erforderlich, damit Anwendungen Intel AVX verwenden können.

**Ebene 2:** Anwendungen in dieser Kategorie haben die Möglichkeit, in ihren Ausnahmefiltern auf den AVX-Zustand zum Zeitpunkt der Ausnahme zu zugreifen und ihn zu bearbeiten. Nach dem Abrufen des Basisprozessorkontexts über GetExceptionInformation sollten Filter:

 **1. Überprüfen** Sie den Wert des **CONTEXT \_ XSTATE-Flags.** Dieses Flag gibt an, dass mindestens ein XState-Feature im Kontext vorlag.  
**2.** Wenn dies der Fall ist, rufen Sie **GetXStateFeaturesMask** auf, und testen Sie den Wert des **XSTATE \_ AVX-Flags** in der zurückgegebenen Maske. Dies gibt das Vorhandensein des AVX-Zustands im Kontext an.  
**3. Rufen Sie** **LocateXStateFeature auf,** um den tatsächlichen Speicherort des AVX-Zustands abzurufen.  

**Ebene 3:** Es ist nicht erforderlich, vorhandene Debuggeranwendungen zu aktualisieren, es sei denn, sie möchten auf die Intel AVX-Register zugreifen:

**1.** Um zu bestimmen, ob AVX aktiviert ist, sollte der Debugger Verwenden:

-   GetEnabledXStateFeatures zum Erhalten einer Maske aktivierter XState-Features auf x86- oder x64-Prozessoren, um zu bestimmen, welche Features auf dem System vorhanden und aktiviert sind, bevor ein XState-Prozessorfeature verwendet oder versucht wird, XState-Kontexte zu bearbeiten

  
**2.** Wenn AVX vorhanden ist und Sie den AVX-Zustand aus der zu debuggenden Anwendung abrufen und bearbeiten möchten (z. B. GetThreadContext und SetThreadContext), sollte der Debugger Folgendes verwenden:

-   InitializeContext-Funktion zum Initialisieren einer Kontextstruktur innerhalb eines Puffers mit der erforderlichen Größe und Ausrichtung
-   CopyContext-Funktion zum Kopieren einer Quellkontextstruktur (einschließlich eines beliebigen XState) in eine initialisierte Zielkontextstruktur

  
**3.** Zum Testen, Festlegen und Suchen des AVX-Zustands in einem Prozessorkontext sollte der Debugger Verwenden:

-   LocateXStateFeature zum Abrufen eines Zeigers auf den Prozessorzustand für ein einzelnes XState-Feature innerhalb einer Kontextstruktur
-   GetXStateFeaturesMask zum Zurückgeben der Maske von XState-Features, die innerhalb einer Kontextstruktur festgelegt sind
-   SetXStateFeaturesMask zum Festlegen der Maske von XState-Features, die innerhalb einer Kontextstruktur festgelegt sind

  


## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   Informationen zu den XState-Funktionen im Windows SDK finden Sie unter [Debuggen von Funktionen.](../debug/debugging-functions.md)
-   Eine Übersicht über die Anweisungen und Funktionen von Intel AVX finden Sie unter [Intel AVX: New Grenzlinien in Leistungsverbesserungen und Energieeffizienz.](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/)

 

 
