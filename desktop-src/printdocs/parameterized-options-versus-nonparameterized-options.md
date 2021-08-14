---
description: Erfahren Sie, wie PrintTicket und PrintCapabilities parametrisierte und nicht parametrisierte Optionen behandeln.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Parametrisierte Optionen im Vergleich zu nicht parametrisierten Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb51d2d1df6ed49e389aff9aa614fabb2ace9d462cccbb3d56438f84b363fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731958"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Parametrisierte Optionen im Vergleich zu nicht parametrisierten Optionen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintCapabilities- und PrintTicket-Anbieter müssen parametrisierte Optionsinstanzen während des PrintTicket-Überprüfungsprozesses ordnungsgemäß verarbeiten. Wie unter [Optionsdefinitionen](option-definitions.md)erläutert, besteht ein Schritt bei der PrintTicket-Überprüfung darin, die Option im PrintCapabilities-Dokument des aktuellen Geräts (die Kandidatenoption) zu finden, die der im PrintTicket (Referenzoption) angegebenen Option am besten entspricht. Wenn eine oder beide Optionsinstanzen parametrisiert werden, gibt es drei mögliche Fälle, die vom vom Gerätetreiber definierten Bewertungsprozess behandelt werden müssen: der Fall, in dem beide Optionsinstanzen parametrisiert werden, und die beiden Fälle, in denen eine Option parametrisiert wird und die andere nicht. In den folgenden Fällen wird davon ausgegangen, dass es eine Entsprechung zwischen den parametrisierten ScoredProperty-Instanzen in der PrintTicket-Option und einer bestimmten ScoredProperty in der PrintCapabilities-Option gibt. Wenn keine Entsprechung vorliegt, kann der Bewertungsprozess diese ScoredProperty-Instanzen auf die gleiche Weise behandeln wie alle anderen nicht reagierenden ScoredProperty-Instanzen.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Fall 1: Parametrisierte PrintTicket- und PrintCapabilities-Dokumentoptionen

In diesem Fall werden sowohl die Verweisoption (im PrintTicket) als auch die Kandidatenoption (im PrintCapabilities-Dokument) parametrisiert. Greifen Sie auf die ParameterDef-Instanz zu, auf die von der Kandidatenoption verwiesen wird (beides im PrintCapabilities-Dokument), und bestimmen Sie, ob der im PrintTicket angegebene ParameterInit-Wert in den von der ParameterDef-Instanz zulässigen Bereich fällt. Wenn ja, betrachten Sie diese ScoredProperty als Übereinstimmung. Andernfalls ist diese ScoredProperty keine Übereinstimmung.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Fall 2: Parametrisierte PrintTicket-Option, nicht parametrisierte PrintCapabilities-Dokumentoption

In diesem Fall enthält printTicket ein Feature mit einer parametrisierten Option, während das entsprechende Feature im PrintCapabilities-Dokument mindestens eine Option enthält, die nicht parametrisiert ist. Auch wenn das PrintCapabilities-Dokument auch andere Option-Instanzen enthält, die parametrisiert sind, muss der Bewertungsprozess auf jede Option angewendet werden, da das Ziel darin besteht, die beste übereinstimmende Option zu identifizieren. Der Client muss nicht parametrisierte Optionskandidaten mit einer parametrisierten Verweisoption vergleichen können.

Da die parametrisierte Option im PrintTicket angezeigt wird, sollten auch die ParameterInit-Instanzen vorhanden sein, wie im vorherigen Fall dargestellt. Der Bewertungsprozess kann einfach jede ParameterRef-Instanz in der parametrisierten Option von PrintTicket durch den Wert ersetzen, der von der ParameterInit-Instanz von PrintTicket angegeben wird. Dadurch wird eine parametrisierte Option effektiv in eine option konvertiert, die nicht parametrisiert ist. An diesem Punkt kann der herkömmliche Abgleichsprozess verwendet werden.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Fall 3: Nicht parametrisierte PrintTicket-Option, parametrisierte PrintCapabilities-Dokumentoption

In diesem Fall wird die Verweisoption im PrintTicket nicht parametrisiert, während die Kandidatenoption im PrintCapabilities-Dokument parametrisiert wird. Greifen Sie im PrintCapabilities-Dokument auf die ParameterDef-Instanz zu, auf die die ParameterRef-Instanz der Kandidatenoption im PrintTicket verweist, und bestimmen Sie, ob der wert, der in der Verweisoption für die entsprechende ScoredProperty definiert ist, in den von der ParameterDef-Instanz zulässigen Bereich fällt. Wenn ja, betrachten Sie diese ScoredProperty als Übereinstimmung. Wenn nicht, ist diese ScoredProperty keine Übereinstimmung.

Es sollte hervorgehoben werden, dass Sie bestimmen, wie genau zwei Optionsinstanzen mit der Anzahl (und Bedeutung) der übereinstimmenden ScoredProperty-Instanzen übereinstimmen, unabhängig davon, ob die ScoredProperty-Instanzen explizite Value-Instanzen oder ParameterRef-Instanzen enthalten. Es ist möglich, dass eine Kandidatenoption die beste Übereinstimmung ist, obwohl sie mehrere Eigenschafteninstanzen enthält, die nicht mit denen der Verweisoption übereinstimmen oder keine entsprechende Eigenschaft in der Verweisoption aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



