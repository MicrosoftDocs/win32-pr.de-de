---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Verwenden von Parametern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fe8fc7c79ed27c467b59ef67132e816cdcd63
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219063"
---
# <a name="using-parameters"></a>Verwenden von Parametern

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Zusätzlich zur ordnungsgemäßen Bewertung einer Option, die ParameterRef-Instanzen enthält (siehe [Verweis Parameter](referencing-parameters.md)), müssen printfunktionen oder PrintTicket-Anbieter und-Clients darauf vorbereitet sein, die folgenden Situationen mit Parametern zu behandeln.

Benutzeroberflächen Clients (UI) müssen den Benutzer auffordern, parameterinitialisierer (Werte für parameterinit-Elemente) für bestimmte Parameter zum richtigen Zeitpunkt anzugeben, damit die entsprechenden parameterinit-Elemente in das PrintTicket eingefügt werden. Benutzeroberflächen Clients müssen in der Lage sein, die beiden Typen von Parametern, uneingeschränkt obligatorisch und bedingt obligatorisch, zu unterscheiden. Sie müssen dann in der Lage sein, jeden Typ entsprechend zu verarbeiten. Für einen bedingungslosen Parameter muss die Benutzeroberfläche sicherstellen, dass für diesen Parametertyp ein parameterinit-Element bereitgestellt wird. Bei einem bedingt obligatorischen Parameter muss die Benutzeroberfläche einen parameterinit-Wert bereitstellen, wenn durch eine Option, die in PrintTicket ausgewählt ist, auf den Parameter verwiesen wird. Der obligatorische Status eines Parameters wird in einer ParameterDef-Instanz angegeben. Weitere Informationen finden Sie unter [ParameterDef-und parameterinit-Elemente](parameterdef-and-parameterinit-elements.md). UI-Clients sollten vom Benutzer bereitgestellte parameterinit-Werte überprüfen, um sicherzustellen, dass Sie die in der ParameterDef-Instanz angegebenen Anforderungen erfüllen.

Print Ticket-Anbieter sollten außerdem die parameterinit-Instanzen überprüfen, die von PrintTicket bereitgestellt werden, um zu überprüfen, ob alle benötigten Parameter vorhanden sind und die in der ParameterDef-Instanz angegebenen Anforderungen erfüllen. Der Validierungscode sollte angemessene Standardwerte angeben, wenn parameterinit-Werte ungültig sind oder fehlen. Beachten Sie, dass ein ParameterDef einen Standardwert für diesen Zweck zulässt. Wenn z. b. Einschränkungen in Bezug auf die Parameter vorhanden sind, z. b. "Wenn *CopyCount* größer als N ist, dann keinen kleinen Kapazitäts-Eingabe Korb verwenden", sollte der PrintTicket-Validierungscode diese Einschränkung erkennen und das PrintTicket ändern, um die Aktivierung der Einschränkung zu vermeiden.

Wenn eine Abhängigkeit von Print-Funktionen für die im PrintTicket angegebenen Parameter vorliegt, müssen PrintValues-Anbieter die parameterinit-Werte überwachen und ein entsprechendes printfunktionalitäten-Dokument liefern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



