---
description: Erweiterte Liniendienste (oder gerätespezifische Liniendienste) enthalten alle vom Dienstanbieter definierten Erweiterungen der API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Erweiterte Linienfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394ad011a5752a45f82de4934a3f87c9f1590870b245fdc113f57badb4298290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003658"
---
# <a name="extended-line-functions"></a>Erweiterte Linienfunktionen

Erweiterte Liniendienste (oder gerätespezifische Liniendienste) enthalten alle vom Dienstanbieter definierten Erweiterungen der API. Die API definiert einen Mechanismus, der es Dienstanbieteranbietern ermöglicht, TAPI mit gerätespezifischen Erweiterungen zu erweitern. Die API definiert nur den Erweiterungsmechanismus und ermöglicht dadurch den Zugriff auf gerätespezifische Erweiterungen, aber die API definiert ihr Verhalten nicht. Das Verhalten wird vollständig vom Dienstanbieter definiert.

TAPI besteht aus konstanten Definitionen für Skalar- und Bitflags, Datenstrukturen, Funktionen und Meldungen. Es sind Prozeduren definiert, die es einem Anbieter ermöglichen, die meisten dieser Verfahren wie folgt zu erweitern.

Für erweiterbare skalare Datenkonst constants kann ein Dienstanbieteranbieter neue Werte in einem angegebenen Bereich definieren. Da die meisten Datenkonst konstanten **DWORD-Werte** sind, ist der Bereich 0x00000000 bis 0x7FFFFFFF in der Regel für gängige zukünftige Erweiterungen reserviert, während 0x80000000 bis 0xFFFFFFFF für anbieterspezifische Erweiterungen verfügbar sind. Es wird davon ausgegangen, dass ein Anbieter Werte definiert, die natürliche Erweiterungen der von der API definierten Datentypen sind.

Für erweiterbare Bitflag-Datenkonst constants kann ein Dienstanbieteranbieter neue Werte für angegebene Bits definieren. Da es sich bei den meisten Bitflagkonstoren um **DWORD-Konstanten** handelt, ist in der Regel eine bestimmte Anzahl der unteren Bits für allgemeine Erweiterungen reserviert, während die verbleibenden oberen Bits für anbieterspezifische Erweiterungen verfügbar sind. Allgemeine Bitflags werden von Bit 0 (null) nach oben zugewiesen. Anbieterspezifische Erweiterungen sollten von Bit 31 nach unten zugewiesen werden. Dies bietet maximale Flexibilität beim Zuweisen von Bitpositionen zu allgemeinen Erweiterungen im Vergleich zu anbieterspezifischen Erweiterungen. Es wird erwartet, dass ein Anbieter neue Werte definiert, die natürliche Erweiterungen der von der API definierten Bitflags sind.

Erweiterbare Datenstrukturen verfügen über ein Feld mit unterschiedlicher Größe, das für die gerätespezifische Verwendung reserviert ist. Da die Größe variabel ist, entscheidet der Dienstanbieter über die Menge der Informationen und die Interpretation. Ein Anbieter, der ein gerätespezifisches Feld definiert, muss diese natürlichen Erweiterungen der ursprünglichen Datenstruktur erstellen, die von der API definiert wird.

Zwei Funktionen, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) und [**lineDevSpecificFeature,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)und zwei verwandte Nachrichten, [**LINE \_ DEVSPECIFIC**](line-devspecific.md) und [**LINE \_ DEVSPECIFICFEATURE,**](line-devspecificfeature.md)bieten einen anbieterspezifischen Erweiterungsmechanismus. Die **lineDevSpecific-Funktion** und die zugehörige LINE DEVSPECIFIC-Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Zeilen-, Adress- oder Anruffunktionen, die mit den Basic- oder Supplementary Telefoniediensten nicht verfügbar \_ sind. Das Parameterprofil der **lineDevSpecific-Funktion** ist generisch, da die API die Parameter nur wenig interpretiert. Die Interpretation der Parameter wird vom Dienstanbieter definiert und muss von einer Anwendung verstanden werden, die sie verwendet. Die Parameter werden einfach über TAPI von der Anwendung an den Dienstanbieter übergeben. Eine Anwendung, die auf gerätespezifischen Erweiterungen basiert, funktioniert im Allgemeinen nicht mit anderen Dienstanbietern. Anwendungen, die in die Dienste "Basic" und "Supplementary Telefony" geschrieben werden, funktionieren jedoch mit dem erweiterten Dienstanbieter.

Der Einfachheit halber wird auch eine speziellere Escapefunktion bereitgestellt. Sie ähnelt [**lineDevSpecific,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)legt aber die Interpretation auf einige der Parameter fest. Diese speziellere Funktion ist [**lineDevSpecificFeature,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)eine gerätespezifische Escapefunktion zum Senden von Switchfeatures an den Switch. Die Meldung [**LINE \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) ist die gerätespezifische Nachricht, die als Hinweis auf features, die an den Switch gesendet werden, an die Anwendung gesendet wird. Diese Funktion und die zugehörige Meldung ermöglichen einer Anwendung das Emulieren von Tastendrucken auf dem Funktionstelefon der Zeile. Da Funktionstelefone und die Bedeutungen ihrer Schaltflächen herstellerspezifisch sind, ist der Funktionsaufruf mit [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) auch herstellerspezifisch.

Wie bereits erwähnt, gibt es keine zentrale Registrierung für Herstellerbezeichner. Stattdessen wird ein Generator für eindeutige Bezeichner (EXTIDGEN) verfügbar gemacht.

 

 



