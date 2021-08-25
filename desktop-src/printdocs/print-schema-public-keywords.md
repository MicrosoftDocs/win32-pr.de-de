---
description: In diesem Artikel werden die öffentlichen Schlüsselwörter angegeben, die für das Druckschema definiert sind, sowie deren Verwendung für PrintCapabilities und PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Öffentliche Schlüsselwörter des Druckschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbcab9ce943b7f344ce12c378252bc07c69260f75c607b36f7af54c107d3f84a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886360"
---
# <a name="print-schema-public-keywords"></a>Öffentliche Schlüsselwörter des Druckschemas

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Im folgenden Abschnitt werden die öffentlichen Schlüsselwörter angegeben, die für das Druckschema definiert sind.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Verwendung öffentlicher Schlüsselwörter des Druckschemas für Druckfunktionen

Schlüsselwörter, die unter PrintCapabilities Public Keywords angegeben sind, können in einem Dokument zu Druckfunktionen angezeigt werden. Weitere Informationen dazu, wie diese Schlüsselwörter mit der PrintCapabilities-Technologie interagieren, finden Sie im Abschnitt [Übersicht über PrintCapabilities.](overview-of-the-printcapabilities.md)

Öffentliche Schlüsselwörter, die für PrintTicket spezifisch sind, SOLLTEN NICHT in einem PrintCapabilities-Dokument angezeigt werden.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Verwendung öffentlicher Schlüsselwörter des Druckschemas für PrintTicket

Schlüsselwörter, die unter PrintTicket Public Keywords angegeben sind, können in einem PrintTicket angezeigt werden. PrintTicket-Schlüsselwörter werden als Property-Elementtyp implementiert. Weitere Informationen dazu, wie diese Schlüsselwörter mit der PrintTicket-Technologie interagieren, finden Sie im Abschnitt [Konfigurationsinformationen, die nicht mit PrintCapabilities in Zusammenhang stehen.](configuration-information-not-related-to-printcapabilities.md)

Schlüsselwörter, die unter PrintCapabilities Public Keywords angegeben sind, können abhängig von der Implementierung von PrintTicket in einer Anwendung und/oder einem Treiber in einem PrintTicket angezeigt werden. Dies bietet Eine Auswahl für Geräteattribute, die im PrintCapabilities-Dokument definiert sind. Weitere Informationen zur Interaktion zwischen PrintCapabilities-Schlüsselwörtern und PrintTicket finden Sie im Abschnitt Zweck des Abschnitts [PrintTicket.](purpose-of-the-printticket.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



