---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Parametrisierte Optionen im Vergleich zu nicht parametrisierten Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c1da2aba2515662be79da0c3831762de66463d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351848"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Parametrisierte Optionen im Vergleich zu nicht parametrisierten Optionen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Der Print-Funktions-und der PrintTicket-Anbieter müssen parametrisierte Options Instanzen während der PrintTicket-Validierung ordnungsgemäß verarbeiten. Wie in [options Definitionen](option-definitions.md)erläutert, besteht ein Schritt bei der Überprüfung von PrintTicket darin, die Option im PrintOptions-Dokument des aktuellen Geräts (der Candidate-Option) zu finden, das am besten mit der Option übereinstimmt, die in PrintTicket (Verweis Option) angegeben ist. Wenn eine oder beide Options Instanzen parametrisiert werden, gibt es drei mögliche Fälle, die vom Gerätetreiber definierten Bewertungsprozess behandelt werden müssen: der Fall, in dem beide Options Instanzen parametrisiert werden, und die beiden Fälle, in denen eine Option parametrisiert und die andere nicht ist. In den folgenden Fällen wird davon ausgegangen, dass es eine Übereinstimmung zwischen den parametrisierten ScoredProperty-Instanzen in der PrintTicket-Option und einer bestimmten ScoredProperty in der Printworks-Option gibt. Wenn keine Entsprechung vorhanden ist, kann der Bewertungsprozess diese ScoredProperty-Instanzen auf die gleiche Weise behandeln, wie alle anderen nicht entsprechenden ScoredProperty-Instanzen behandelt werden.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Fall 1-parametrisierte PrintTicket-und printfunktionen-Dokument Optionen

In diesem Fall werden sowohl die Verweis Option (in der PrintTicket-Option als auch die Candidate-Option (im Dokument printfunktionalitäten) parametrisiert. Greifen Sie auf die ParameterDef-Instanz zu, auf die von der Candidate-Option verwiesen wird (im Printworks-Dokument), und bestimmen Sie, ob der im PrintTicket angegebene parameterinit-Wert in den von der ParameterDef-Instanz zulässigen Bereich fällt. Wenn dies der Fall ist, sollten Sie diese ScoredProperty als Entsprechung in Erwägung gezogen. Andernfalls ist diese ScoredProperty keine Entsprechung.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Fall 2-parametrisierte PrintTicket-Option, nicht parametrisierte printfunktionen-Dokument Option

In diesem Fall enthält das PrintTicket eine Funktion mit einer parametrisierten Option, während das entsprechende Feature im Printworks-Dokument mindestens eine nicht parametrisierte Option enthält. Auch wenn das printfunktionalitäten-Dokument auch andere Options Instanzen enthält, die parametrisiert sind, muss der Bewertungsprozess auf jede Option angewendet werden, da das Ziel darin besteht, die beste übereinstimmende Option zu identifizieren. Der Client muss in der Lage sein, nicht parametrisierte Options Kandidaten mit einer parametrisierten Verweis Option zu vergleichen.

Da die parametrisierte Option in PrintTicket angezeigt wird, sollten die parameterinit-Instanzen auch wie im vorherigen Fall dargestellt vorhanden sein. Der Bewertungsprozess kann einfach jede beliebige ParameterRef-Instanz in der parametrisierten Option von PrintTicket durch den Wert ersetzen, der von der parameterinit-Instanz von PrintTicket angegeben wird. Dadurch wird eine parametrisierte Option praktisch in eine, die nicht parametrisiert ist, konvertiert. An diesem Punkt kann der konventionelle Vergleichsprozess verwendet werden.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Fall 3-nicht parametrisierte PrintTicket-Option, parametrisierte printfunktionen-Dokument Option

In diesem Fall ist die Reference-Option im PrintTicket nicht parametrisiert, während die Candidate-Option im printfunktionalitäten-Dokument parametrisiert ist. Greifen Sie in dem Printworks-Dokument, auf das von der ParameterRef-Instanz der Kandidaten Option im PrintTicket verwiesen wird, auf die ParameterDef-Instanz zu, und stellen Sie fest, ob der in der reference-Option für die zugehörige ScoredProperty definierte Wert in den von der ParameterDef-Instanz zulässigen Bereich fällt. Wenn dies der Fall ist, sollten Sie diese ScoredProperty als Entsprechung in Erwägung gezogen. Wenn dies nicht der Wert ist, ist diese ScoredProperty keine Entsprechung.

Es sollte hervorgehoben werden, dass Sie feststellen, wie genau zwei Options Instanzen mit der Anzahl (und der Bedeutung) der ScoredProperty-Instanzen übereinstimmen, die übereinstimmen, unabhängig davon, ob die ScoredProperty-Instanzen explizite Wert Instanzen oder ParameterRef-Instanzen enthalten. Es ist möglich, dass eine Kandidaten Option die beste Übereinstimmung ist, auch wenn Sie mehrere Eigenschafts Instanzen enthält, die nicht mit denen der Verweis Option übereinstimmen, oder für die keine entsprechende Eigenschaft in der reference-Option vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



