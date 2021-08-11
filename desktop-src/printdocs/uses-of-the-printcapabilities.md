---
description: Erfahren Sie mehr über die Verwendungsmöglichkeiten von PrintCapabilities. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Verwendungsmöglichkeiten von PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aec2d21a2751305ae1f2e191a37adb584a0209542a78a0bf53253ea66faa20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233528"
---
# <a name="uses-of-the-printcapabilities"></a>Verwendungsmöglichkeiten von PrintCapabilities

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintCapabilities soll konfigurierbare Geräteattribute entweder als Feature-/Optionskonstrukte oder als Parameterkonstrukte darstellen. Diese Informationen definieren den Konfigurationsraum des Geräts und können von einem Benutzeroberflächenclient verwendet werden, um eine Benutzeroberfläche zu erstellen. Die Druckschemaschlüsselwörter definieren eine Reihe von Standardfunktionsinstanzen, Optionsinstanzen für die Standardfunktionsinstanzen und ParameterDef-Instanzen.

Die Feature-/Options- oder Parameterkonstrukte in PrintCapabilities sind für Property- oder ScoredProperty-Instanzen vorgesehen, die ein Gerät beschreiben und vom Spooler-Subsystem unterstützt werden. Diese Property- und ScoredProperty-Instanzen sind für Clients des Geräts von allgemeinem Interesse und enthalten die Informationen, die von den Win32 DevCaps-Funktionen bereitgestellt werden. Die Print Schema Keywords definieren einen Satz von Standard-Property- und ScoredProperty-Instanzen.

Es sollte hervorgehoben werden, dass das PrintCapabilities-Dokument nur einwertige Daten darstellen soll: Daten, die nicht von einer bestimmten Konfiguration des Geräts abhängen. Das PrintCapabilities-Dokument enthält nur eine Momentaufnahme konfigurationsabhängiger Daten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



