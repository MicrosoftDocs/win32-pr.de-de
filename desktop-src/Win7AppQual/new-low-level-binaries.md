---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Neue Low-Level-Binärdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217412"
---
# <a name="new-low-level-binaries"></a>Neue Low-Level-Binärdateien

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Häufigkeit** -hoch  











## <a name="description"></a>BESCHREIBUNG

Um die interne Entwicklungseffizienz zu verbessern und die Grundlagen für zukünftige arbeiten zu verbessern, haben wir einige Funktionen in neue Low-Level-Binärdateien verlagert. Dieses Refactoring ermöglicht die zukünftige Installation von Windows, um Teilmengen von Funktionen zur Reduzierung der Oberfläche (Datenträger-und Arbeitsspeicher Anforderungen, Wartung und Angriffsfläche) bereitzustellen.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Als Beispiel für Funktionen, die in Binärdateien auf niedriger Ebene verschoben wurden, kernelbase.dll die Funktionalität von kernel32.dll und advapi32.dll abrufen. Dies bedeutet, dass die vorhandene Binärdatei jetzt Aufrufe an die neue Binärdatei weiterleitet, anstatt Sie direkt zu verarbeiten. die Weiterleitung kann statisch sein (die Export Tabelle zeigt die Umleitung), oder die Laufzeit (die dll verfügt über eine Stub-Routine, die die neue Binärdatei aufruft). Dies wirkt sich auf Low-Level-Anwendungen wie z. b. Sicherheits-und Sicherungs Anwendungen aus, die von internen APIs und Offsets abhängig sind.

## <a name="solution"></a>Lösung

Der einzige Untergrund ist der Code, der Annahmen trifft, wenn versucht wird, die kernel32.dll oder die advapi32.dll Export Tabelle im Speicher zu untersuchen, z. b. eine Antivirussoftware. Verwenden Sie veröffentlichte APIs und nicht die Details Ihrer Implementierung. Dies ist nur ein Beispiel für die Implementierung von Implementierungsdetails für eine API.

 

 



