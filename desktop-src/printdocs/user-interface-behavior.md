---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Verhalten der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d475472330c8e3ba2ceb06d0cbde9f3a7fb0be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357166"
---
# <a name="user-interface-behavior"></a>Verhalten der Benutzeroberfläche

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Angenommen, Sie erstellen einen Printworks-Client, der in einem Printworks-Dokument liest und eine oder mehrere Optionen aus jedem Feature auswählt und diese zum Erstellen eines PrintTicket verwendet, das die Konfiguration angibt, die zum Verarbeiten des Auftrags verwendet werden soll. Für jedes Feature, das von Interesse ist, muss der Client die einzelnen Optionen untersuchen und entscheiden, ob diese Option für die jeweilige Aufgabe geeignet ist. Für eine Option, die nicht parametrisiert ist, kann Sie durch Zugriff auf den Wert der einzelnen ScoredProperty ausgewertet werden. Im Fall einer nicht parametrisierten Mediengrößen Option bestimmt der Client, ob die Abmessungen für Breite und Höhe des in jeder Option gemeldeten Mediums den erforderlichen Dimensionen entsprechen.

Im Fall der parametrisierten Option muss der Client auf die ParameterDef-Instanz zugreifen, die in der ParameterRef-Instanz angegeben ist, die in einer der ScoredProperty-Instanzen enthalten ist. ParameterDef definiert normalerweise den Wertebereich, der für den Parameter zulässig ist, sowie die Einheiten (Zoll, mm usw.), die durch den-Wert dargestellt werden. Wenn die erforderlichen Dimensionen in den Wertebereich fallen, der für die einzelnen Parameter zulässig ist, verfügt der Client über die zusätzliche Aufgabe, die Parameter (über eine parameterinit-Instanz) in PrintTicket zu initialisieren. Dies ist eine besonders wichtige Aufgabe. Beispielsweise sollte ein Print Ticket keine benutzerdefinierte Mediengröße angeben, ohne die Abmessungen des Mediums anzugeben, da das resultierende PrintTicket mehrdeutig und falsch definiert ist.

Ein ähnlicher Satz von Umständen muss behandelt werden, wenn der Client eine Benutzeroberfläche ist. Die Benutzeroberfläche zeigt in der Regel die Werte der ScoredProperty-Instanzen an, die für die einzelnen Optionen definiert wurden. Aus Gründen der Übersichtlichkeit ist es von entscheidender Bedeutung, den zulässigen Bereich und die zulässigen Einheiten für die Parameter in einer parametrisierten Option anzuzeigen. Wenn der Benutzer außerdem die parametrisierte Option auswählt, muss die Benutzeroberfläche (User Interface, UI) den Benutzer auffordern, den Wert einzugeben, der zum Initialisieren der einzelnen Parameter verwendet werden soll. Zum Schluss muss die Benutzeroberfläche ein Print Ticket verfassen, das alle Auswahlmöglichkeiten des Benutzers widerspiegelt.

Details zur Druck Ticketerstellung und zur Angabe der Parameter Initialisierung finden Sie unter [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Weitere Informationen zum dereferenzieren von ParameterRef-Instanzen und zum Interpretieren von ParameterDef-Instanzen finden [Sie unter Verwenden von Parametern](using-parameters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



