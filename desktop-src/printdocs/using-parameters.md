---
description: Erfahren Sie, wie Sie Parameter in einem PrintCapabilities-Dokument verwenden. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Verwenden von Parametern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc19b6c2b6deb269c0d3a34140bc0e9816febc86d33adfdb6ed0c91fe38f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469325"
---
# <a name="using-parameters"></a>Verwenden von Parametern

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Zusätzlich zur ordnungsgemäßen Bewertung einer Option, die ParameterRef-Instanzen enthält (siehe Verweisen auf [Parameter),](referencing-parameters.md)müssen PrintCapabilities- oder PrintTicket-Anbieter und -Clients darauf vorbereitet sein, die folgenden Situationen im Zusammenhang mit Parametern zu behandeln.

Benutzeroberflächenclients müssen den Benutzer auffordern, Parameterinitialisierer (Werte für ParameterInit-Elemente) für bestimmte Parameter zum entsprechenden Zeitpunkt zur Verfügung zu stellen, damit die entsprechenden ParameterInit-Elemente in PrintTicket eingefügt werden. Benutzeroberflächenclients müssen in der Lage sein, die beiden Typen von Parametern zu unterscheiden: bedingungslos obligatorisch und bedingt obligatorisch, und sie müssen in der Lage sein, jeden Typ entsprechend zu behandeln. Für einen bedingungslos obligatorischen Parameter muss die Benutzeroberfläche sicherstellen, dass ein ParameterInit-Element für diesen Parametertyp bereitgestellt wird. Für einen bedingt obligatorischen Parameter muss die Benutzeroberfläche einen ParameterInit-Wert bereitstellen, wenn auf den Parameter durch eine Option verwiesen wird, die im PrintTicket ausgewählt ist. Der Obligatorische Status eines Parameters wird in einer ParameterDef-Instanz angegeben. Weitere Informationen finden Sie unter [ParameterDef und ParameterInit Elements](parameterdef-and-parameterinit-elements.md). Benutzeroberflächenclients sollten vom Benutzer bereitgestellte ParameterInit-Werte überprüfen, um sicherzustellen, dass sie die in der ParameterDef-Instanz angegebenen Anforderungen erfüllen.

PrintTicket-Anbieter sollten auch die parameterInit-Instanzen überprüfen, die von PrintTicket bereitgestellt werden, um sicherzustellen, dass alle erforderlichen Parameter vorhanden sind und die in der ParameterDef-Instanz angegebenen Anforderungen erfüllen. Der Validierungscode sollte angemessene Standardwerte für den Fall angeben, dass ParameterInit-Werte ungültig sind oder fehlen. Beachten Sie, dass eine ParameterDef zu diesem Zweck das Angeben eines Standardwerts zu diesem Zweck zu lässt. Außerdem sollte der PrintTicket-Validierungscode diese Einschränkung erkennen und das PrintTicket ändern, wenn *CopyCount* größer als N ist, dann verwenden Sie keinen kleinen Kapazitätseingabebehälter.

Wenn printCapabilities von den im PrintTicket angegebenen Parametern abhängig ist, müssen PrintCapabilities-Anbieter die ParameterInit-Werte überwachen und ein entsprechendes PrintCapabilities-Dokument erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



