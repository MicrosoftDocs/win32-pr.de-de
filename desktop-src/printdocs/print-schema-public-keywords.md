---
description: In diesem Artikel werden die öffentlichen Schlüsselwörter angegeben, die für das Druckschema definiert sind, und deren Verwendung für PrintCapabilities und PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Öffentliche Schlüsselwörter für Das Schema drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407143"
---
# <a name="print-schema-public-keywords"></a>Öffentliche Schlüsselwörter für Das Schema drucken

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Im folgenden Abschnitt werden die öffentlichen Schlüsselwörter angegeben, die für das Druckschema definiert sind.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Print Schema: Verwendung öffentlicher Schlüsselwörter für Druckfunktionen

Schlüsselwörter, die unter Öffentliche PrintCapabilities-Schlüsselwörter angegeben sind, können in einem Dokument druckfunktionen angezeigt werden. Weitere Informationen zur Interaktion dieser Schlüsselwörter mit der PrintCapabilities-Technologie finden Sie im Abschnitt [Übersicht über PrintCapabilities.](overview-of-the-printcapabilities.md)

Öffentliche Schlüsselwörter, die für PrintTicket spezifisch sind, SOLLTEN NICHT in einem PrintCapabilities-Dokument angezeigt werden.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Print Schema: Verwendung öffentlicher Schlüsselwörter für PrintTicket

Schlüsselwörter, die unter Öffentliche PrintTicket-Schlüsselwörter angegeben sind, können in einem PrintTicket angezeigt werden. PrintTicket-Schlüsselwörter werden als Property-Elementtyp implementiert. Weitere Informationen zur Interaktion dieser Schlüsselwörter mit der PrintTicket-Technologie finden Sie im Abschnitt Konfigurationsinformationen, die sich [nicht auf PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) beziehen.

Schlüsselwörter, die unter Öffentliche PrintCapabilities-Schlüsselwörter angegeben sind, können abhängig von der Implementierung von PrintTicket in einer Anwendung und/oder einem Treiber in einem PrintTicket angezeigt werden. Dies bietet Auswahl für Geräteattribute, die im PrintCapabilities-Dokument definiert sind. Weitere Informationen zur Interaktion zwischen PrintCapabilities-Schlüsselwörtern und PrintTicket finden Sie im Abschnitt Zweck [des Abschnitts PrintTicket.](purpose-of-the-printticket.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



