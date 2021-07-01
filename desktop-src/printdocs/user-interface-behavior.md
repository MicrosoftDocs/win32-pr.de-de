---
description: Sehen Sie sich eine Diskussion über das Verhalten der Benutzeroberfläche in Bezug auf Features und Optionen für Dokumente und Drucken an.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Benutzeroberfläche Verhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d007c653ed3f019892e944d9fa4203dc6de11
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119435"
---
# <a name="user-interface-behavior"></a>Benutzeroberfläche Verhalten

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Angenommen, Sie erstellen einen PrintCapabilities-Client, der ein PrintCapabilities-Dokument liest und mindestens eine Option aus jedem Feature auswählt und diese verwendet, um ein PrintTicket zu erstellen, das die Konfiguration angibt, die zum Verarbeiten des Auftrags verwendet werden soll. Für jedes feature of interest muss der Client jede Option überprüfen und entscheiden, ob diese Option für den jeweiligen Task geeignet ist. Für eine Option, die nicht parametrisiert ist, kann sie ausgewertet werden, indem Sie auf den Wert jeder ScoredProperty zugreifen. Im Fall einer Option für nichtparameterisierte Mediengröße bestimmt der Client, ob die Breite und Höhe der Medien, die in jeder Option gemeldet werden, mit den erforderlichen Dimensionen übereinstimmen.

Im Fall der parametrisierten Option muss der Client auf die ParameterDef-Instanz zugreifen, die in der ParameterRef-Instanz angegeben ist, die in einer der ScoredProperty-Instanzen enthalten ist. Die ParameterDef definiert in der Regel den zulässigen Wertebereich für den Parameter sowie die Einheiten (Zoll, MM und so weiter), die durch den Wert dargestellt werden. Wenn die erforderlichen Dimensionen innerhalb des für jeden Parameter zulässigen Wertebereichs liegen, hat der Client die zusätzliche Aufgabe, die Parameter (mit einer ParameterInit-Instanz) im PrintTicket zu initialisieren. Dies ist eine besonders wichtige Aufgabe. Ein PrintTicket sollte z. B. keine benutzerdefinierte Mediengröße angeben, ohne die Abmessungen des Mediums anzugeben, da das resultierende PrintTicket mehrdeutig und nicht definiert ist.

Ein ähnlicher Satz von Umständen muss behandelt werden, wenn der Client eine Benutzeroberfläche ist. Die Benutzeroberfläche zeigt in der Regel die Werte der ScoredProperty-Instanzen an, die für jede Option definiert sind. Aus Gründen der Übersichtlichkeit ist es wichtig, den zulässigen Bereich und die zulässigen Einheiten für die Parameter in einer parametrisierten Option anzuzeigen. Wenn der Benutzer außerdem die parametrisierte Option auswählt, muss die Benutzeroberfläche den Benutzer auffordern, den Wert eingibt, der zum Initialisieren der einzelnen Parameter verwendet werden soll. Schließlich muss die Benutzeroberfläche ein PrintTicket erstellen, das die auswahl des Benutzers widerspiegelt.

Details zur PrintTicket-Konstruktion und zur Spezifikation der Parameterin initialisierung finden Sie unter [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Informationen zum Dereferenzieren von ParameterRef-Instanzen und zum Interpretieren von ParameterDef-Instanzen finden Sie unter [Verwenden von Parametern.](using-parameters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



