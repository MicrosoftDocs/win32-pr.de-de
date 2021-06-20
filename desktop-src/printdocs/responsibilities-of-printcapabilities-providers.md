---
description: PrintCapabilities-Anbieter müssen einen Mindestsatz von Funktionen unterstützen, die von der PrintTicket/PrintCapabilities-Anbieterschnittstelle impliziert werden.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Zuständigkeiten von PrintCapabilities-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404913"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Zuständigkeiten von PrintCapabilities-Anbietern

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintCapabilities-Anbieter müssen einen Mindestsatz von Funktionen unterstützen, die von der PrintTicket/PrintCapabilities-Anbieterschnittstelle impliziert werden. Diese Funktionen sind hier aufgeführt.

-   Sie müssen der Propagaterichtung folgen? XML-Attribut, wenn es im entsprechenden Kontext angezeigt wird und einen gültigen Wert für diesen Kontext enthält.

-   Sie müssen ein PrintCapabilities-Dokument generieren, das dem PrintCapabilities-Schema entspricht und die im Druckschema angegebenen Anforderungen erfüllt.

-   Sie müssen ein gültiges PrintTicket erkennen können.

-   Sie müssen in der Lage sein, ein PrintTicket zu interpretieren und die spezifische Konfiguration zu verstehen, die es darstellt.

-   Sie müssen ermitteln können, ob diese Konfiguration Einschränkungskonflikte enthält.

-   Sie müssen in der Lage sein, ein ungültiges oder in Konflikt stehende PrintTicket zu ändern, indem die am wenigsten signifikante Änderung erforderlich ist, um es sowohl gültig als auch konfliktfrei zu machen.

-   Sie müssen in der Lage sein, ein PrintCapabilities-Dokument für eine bestimmte Gerätekonfiguration zu generieren.

-   Sie müssen in der Lage sein, eine Standardkonfiguration oder PrintTicket zu generieren.

-   Sie müssen in der Lage sein, ein PrintCapabilities-Dokument zu generieren, das der Standardkonfiguration entspricht.

-   Sie müssen einen vom Gerätetreiber definierten Optionsbewertungsprozess implementieren, der in der Lage ist, die Nähe der Übereinstimmung zwischen zwei Optionsinstanzen zu bestimmen, die zum gleichen Feature gehören. Dieser Algorithmus wird im PrintTicket-Überprüfungsprozess verwendet.

Zusätzlich zu den geltenden Anforderungen muss das PrintCapabilities-Dokument gültige und richtige Werte für jedes XML-Attribut (z. B. eingeschränkt) jeder Option enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



