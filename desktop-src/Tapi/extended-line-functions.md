---
description: Erweiterte Zeilen Dienste (oder gerätespezifische Zeilen Dienste) enthalten alle vom Dienstanbieter definierten Erweiterungen für die API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Erweiterte Zeilen Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3531a63357276e6b2ea37365b5d5078d5c1de324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526315"
---
# <a name="extended-line-functions"></a>Erweiterte Zeilen Funktionen

Erweiterte Zeilen Dienste (oder gerätespezifische Zeilen Dienste) enthalten alle vom Dienstanbieter definierten Erweiterungen für die API. Die API definiert einen Mechanismus, mit dem Anbieter von Dienstanbietern TAPI mithilfe von gerätespezifischen Erweiterungen erweitern können. Die API definiert nur den Erweiterungsmechanismus und bietet dadurch Zugriff auf gerätespezifische Erweiterungen, aber die API definiert das Verhalten nicht. Das Verhalten wird vom Dienstanbieter vollständig definiert.

TAPI besteht aus skalaren und Bitflag-Konstanten Definitionen, Datenstrukturen, Funktionen und Nachrichten. Es werden Prozeduren definiert, mit denen ein Anbieter die meisten dieser wie folgt erweitern kann.

Für erweiterbare skalare Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte in einem angegebenen Bereich definieren. Da die meisten Daten Konstanten **DWORD** s sind, ist in der Regel der Bereich 0x00000000 bis 0x7FFFFFFF für allgemeine zukünftige Erweiterungen reserviert, während 0x80000000 bis 0xffffffff für herstellerspezifische Erweiterungen verfügbar sind. Es wird davon ausgegangen, dass ein Anbieter Werte definieren würde, bei denen es sich um natürliche Erweiterungen der von der API definierten Datentypen handelt.

Für erweiterbare Bitflag-Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte für angegebene Bits definieren. Da die meisten bitflagkonstanten **DWORD** s sind, sind in der Regel eine bestimmte Anzahl von niedrigeren Bits für allgemeine Erweiterungen reserviert, während die restlichen oberen Bits für herstellerspezifische Erweiterungen verfügbar sind. Allgemeine Bitflags werden aus Bit 0 (null) zugewiesen. herstellerspezifische Erweiterungen sollten von Bit 31 nach unten zugewiesen werden. Dies bietet maximale Flexibilität beim Zuweisen von Bitpositionen zu allgemeinen Erweiterungen im Vergleich zu herstellerspezifischen Erweiterungen. Es wird erwartet, dass ein Anbieter neue Werte definiert, bei denen es sich um natürliche Erweiterungen der von der API definierten Bitflags handelt.

Erweiterbare Datenstrukturen verfügen über ein Feld mit variabler Größe, das für die gerätespezifische Verwendung reserviert ist. Bei der Größenanpassung bestimmt der Dienstanbieter die Menge der Informationen und die Interpretation. Ein Anbieter, der ein Geräte spezifisches Feld definiert, wird davon ausgegangen, dass diese natürlichen Erweiterungen der ursprünglichen Datenstruktur durch die API definiert werden.

Zwei Funktionen, [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) und [**linedevspecificfeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), und zwei verwandte Meldungen, [**line \_ DevSpecific**](line-devspecific.md) und [**line \_ devspecificfeature**](line-devspecificfeature.md), stellen einen herstellerspezifischen Erweiterungsmechanismus bereit. Die **linedevspecific** -Funktion und die zugehörige Zeilen- \_ DevSpecific-Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Zeilen-, Adress-oder Aufruffunktionen, die mit den Basic-oder ergänzenden Telefoniediensten nicht verfügbar sind. Das Parameter Profil der **linedevspecific** -Funktion ist generisch, weil die-API kaum interpretiert werden kann. Die Interpretation der Parameter wird vom Dienstanbieter definiert und muss von einer Anwendung verstanden werden, die Sie verwendet. Die Parameter werden einfach durch TAPI von der Anwendung an den Dienstanbieter übermittelt. Eine Anwendung, die auf gerätespezifischen Erweiterungen basiert, funktioniert nicht in der Regel mit anderen Dienstanbietern. Anwendungen, die in die grundlegenden und ergänzenden Telefoniedienste geschrieben werden, können jedoch mit dem erweiterten Dienstanbieter verwendet werden.

Zur einfacheren Bereitstellung wird auch eine speziellere escapefunktion bereitgestellt. Sie ähnelt [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific), legt aber die Interpretation einiger Parameter fest. Diese speziellere Funktion ist [**linedevspecificfeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), eine gerätespezifische escapefunktion, die das Senden von Switchfeatures an den Switch ermöglicht. Die Nachrichten [**Zeile " \_ devspecificfeature**](line-devspecificfeature.md) " ist die gerätespezifische Nachricht, die an die Anwendung gesendet wird, als Angabe der an den Switch gesendeten Features. Diese Funktion und die zugehörige Nachricht ermöglichen es einer Anwendung, Schaltflächen auf der Telefonnummer der Zeile zu emulieren. Wenn featuretelefone und die Bedeutungen ihrer Schaltflächen Hersteller spezifisch sind, ist der Funktionsaufruf mit [**linedevspecificfeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) auch Anbieter spezifisch.

Wie bereits erwähnt, gibt es keine zentrale Registrierung für Hersteller Bezeichner. Stattdessen wird ein eindeutiger bezeichnergenerator (extidgen) verfügbar gemacht.

 

 



