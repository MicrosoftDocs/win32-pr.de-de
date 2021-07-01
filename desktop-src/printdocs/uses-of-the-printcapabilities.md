---
description: Erfahren Sie mehr über die Verwendungsmöglichkeiten von PrintCapabilities. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Verwendungsmöglichkeiten der PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119425"
---
# <a name="uses-of-the-printcapabilities"></a>Verwendungsmöglichkeiten der PrintCapabilities

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Die PrintCapabilities sollen konfigurierbare Geräteattribute entweder als Feature-/Optionskonstrukte oder als Parameterkonstrukte darstellen. Diese Informationen definieren den Konfigurationsraum des Geräts und können von einem Benutzeroberflächenclient verwendet werden, um eine Benutzeroberfläche zu erstellen. Die Druckschemaschlüsselwörter definieren eine Reihe von Standardfunktionsinstanzen, Optionsinstanzen für die Standardfunktionsinstanzen und ParameterDef-Instanzen.

Die Feature-/Options- oder Parameterkonstrukte in printCapabilities sind für Property- oder ScoredProperty-Instanzen vorgesehen, die ein Gerät beschreiben und vom Spoolersubsystem unterstützt werden. Diese Property- und ScoredProperty-Instanzen sind für Clients des Geräts von allgemeinem Interesse und enthalten die Informationen, die von den Win32 DevCaps-Funktionen bereitgestellt werden. Die Druckschemaschlüsselwörter definieren einen Satz von Standardeigenschaften- und ScoredProperty-Instanzen.

Es sollte hervorgehoben werden, dass das PrintCapabilities-Dokument nur einwertige Daten darstellen soll: Daten, die nicht von einer bestimmten Konfiguration des Geräts abhängen. Das PrintCapabilities-Dokument stellt nur eine Momentaufnahme konfigurationsabhängiger Daten bereit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



