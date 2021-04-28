---
description: Neue Low-Level Binärdateien
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Neue Low-Level Binärdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088068"
---
# <a name="new-low-level-binaries"></a>Neue Low-Level Binärdateien

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Das Feature

**Schweregrad –** Mittel  
**Häufigkeit** : Hoch  











## <a name="description"></a>BESCHREIBUNG

Um die Interne Engineering-Effizienz zu verbessern und die Grundlagen für zukünftige Arbeit zu verbessern, haben wir einige Funktionen in neue Binärdateien auf niedriger Ebene verschoben. Durch dieses Refactoring können zukünftige Installationen von Windows Teilmengen der Funktionalität bereitstellen, um die Oberfläche zu reduzieren (Datenträger- und Arbeitsspeicheranforderungen, Wartung und Angriffsfläche).

## <a name="manifestation-of-impact"></a>Wirkungserz weiter

Als Beispiel für die Funktionalität, die wir in Binärdateien auf niedriger Ebene verschoben haben, ruft kernelbase.dll Funktionen aus kernel32.dll und advapi32.dll ab. Dies bedeutet, dass die vorhandene Binärdatei jetzt Aufrufe an die neue Binärdatei weiterleitet, anstatt sie direkt zu verarbeiten. Die Weiterleitung kann statisch sein (die Exporttabelle zeigt die Umleitung) oder runtime (die DLL verfügt über eine Stubroutine, die die neue Binärdatei aufruft). Dies wirkt sich auf Low-Level-Anwendungen wie Sicherheits- und Sicherungsanwendungen aus, die von internen APIs und Offsets abhängig sind.

## <a name="solution"></a>Lösung

Die einzige Auswirkung ist der Code, der Annahmen trifft, wenn versucht wird, die kernel32.dll oder die advapi32.dll Exporttabelle im Arbeitsspeicher zu betrachten, z. B. eine Antivirenanwendung. Verwenden Sie veröffentlichte APIs und nicht die Details ihrer Implementierung. Dies ist nur ein Beispiel für die Implementierung eines Implementierungsdetails für eine API.

 

 



