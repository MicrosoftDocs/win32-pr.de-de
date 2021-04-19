---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Öffentliche Schlüsselwörter von printfunktionalitäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353640"
---
# <a name="printcapabilities-public-keywords"></a>Öffentliche Schlüsselwörter von printfunktionalitäten

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Im folgenden Abschnitt werden sowohl vom benutzerkonfigurierbare Elemente als auch Parameter Definitionen angegeben, die möglicherweise auf ein printfunktionalitäten-Dokument anwendbar sind.

## <a name="user-configurable-elements-usage"></a>Benutzerkonfigurierbare Element Verwendung

Vom benutzerkonfigurierbare Elemente stellen öffentliche Schlüsselwörter des Druck Schemas dar, die in einem printfunktionen-Dokument oder einem PrintTicket vorkommen können. Sie sollen konfigurierbare Geräte Attribute darstellen, die von einem bestimmten Gerät unterstützt werden, oder die Absicht der Druckeinstellung durch eine Anwendung oder einen Benutzer zu übermitteln.

Vom benutzerkonfigurierbare Elemente können auf Parameter Verweis Elemente verweisen. Weitere Informationen finden Sie im Abschnitt [Parameter Verweis Elemente](parameter-reference-elements.md) .

## <a name="parameter-definitions-usage"></a>Verwendung von Parameter Definitionen

Parameter Definitionen verwenden die Form von ParameterDef-Elementtypen in einem Dokument mit Druckfunktionen. ParameterDef-Elementtypen werden in einem PrintTicket mit dem parameterinit-Elementtyp initialisiert. Der Wert des-Parameters wird mit dem parameterinit-Element angegeben. Ein vom Benutzer konfigurierbares Schlüsselwort kann mit dem ParameterRef-Elementtyp auf eine Parameterdefinition verweisen. Weitere Informationen finden Sie im Abschnitt [Parameterkonstrukte](parameter-constructs.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



