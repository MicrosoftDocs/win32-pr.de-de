---
description: Erfahren Sie, wie der Autor eines PrintTicket-Clients Elementtypen verwenden kann, um ein PrintTicket zu erstellen, das Absichten für ein Gerät beschreibt.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Prüflisten für die PrintTicket-Konstruktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6a3ae0c19fea01738dbf7c6ecfa52f6f156d59f67dae89d6d5a2952059a765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091720"
---
# <a name="printticket-construction-checklists"></a>Prüflisten für die PrintTicket-Konstruktion

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

In diesem Abschnitt wird veranschaulicht, wie der Autor eines PrintTicket-Clients die im Druckschemaframework definierten Elementtypen verwenden kann, um ein PrintTicket zu erstellen, das Absichten für ein Gerät beschreibt. PrintTicket kann generisch (nicht an ein bestimmtes Gerät gebunden) oder gerätespezifisch sein. Die Semantik von PrintTicket wird ausführlicher dargestellt. Darüber hinaus enthält dieser Abschnitt eine Übersicht über Konzepte und Terminologie, die in den nachfolgenden Abschnitten ausführlicher behandelt werden.

Es gibt zwei grundlegend unterschiedliche Ansätze zum Erstellen eines PrintTickets. Beide Ansätze können verwendet werden.

-   Richten Sie printTicket auf ein unbekanntes oder generisches Gerät aus, indem [Sie ein generisches PrintTicket erstellen.](creating-a-generic-printticket.md)

    Wenn Das Hauptziel darin besteht, die Absicht des Endbenutzers beizubehalten, sollten Sie diesen Ansatz verwenden, indem Sie ein nicht validiertes generisches PrintTicket mit dem Dokument erstellen und speichern.

-   Richten Sie printTicket auf ein bestimmtes Gerät aus, indem [Sie einen Device-Specific PrintTicket erstellen.](creating-a-device-specific-printticket.md)

    Wenn Sie mehr daran interessiert sind, alle Features eines bestimmten Geräts zu nutzen, sollten Sie diesen Ansatz verwenden, indem Sie ein PrintTicket für das jeweilige Gerät erstellen und das überprüfte PrintTicket mit dem Dokument speichern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



