---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Checklisten für die PrintTicket-Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366565"
---
# <a name="printticket-construction-checklists"></a>Checklisten für die PrintTicket-Erstellung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In diesem Abschnitt wird veranschaulicht, wie der Autor eines PrintTicket-Clients die im Druckschema-Framework definierten Elementtypen verwenden kann, um ein Print Ticket zu erstellen, das Intents für ein Gerät beschreibt. Print Ticket kann generisch (nicht an ein bestimmtes Gerät gebunden) sein, oder es kann gerätespezifisch sein. Die Semantik von PrintTicket wird ausführlicher dargestellt. Darüber hinaus enthält dieser Abschnitt eine Übersicht über die Konzepte und die Terminologie, die in den nachfolgenden Abschnitten ausführlicher behandelt werden.

Es gibt zwei grundlegende Vorgehensweisen zum Erstellen eines PrintTicket. Beide Ansätze können verwendet werden.

-   Richten Sie das PrintTicket mit einem unbekannten oder generischen Gerät ein, indem Sie [ein allgemeines PrintTicket erstellen](creating-a-generic-printticket.md).

    Wenn Ihr Hauptziel darin besteht, die Absicht des Endbenutzers beizubehalten, sollten Sie diese Vorgehensweise durchführen, indem Sie ein nicht validiertes, generisches Print Ticket mit dem Dokument erstellen und speichern.

-   Richten Sie das PrintTicket für ein bestimmtes Gerät ein, indem Sie [eine Device-Specific PrintTicket erstellen](creating-a-device-specific-printticket.md).

    Wenn Sie mehr von allen Features profitieren möchten, die von einem bestimmten Gerät angeboten werden, sollten Sie diesen Ansatz verwenden, indem Sie ein Print Ticket für das jeweilige Gerät erstellen und das überprüfte PrintTicket mit dem Dokument speichern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



