---
description: Erfahren Sie mehr über benutzerkonfigurierbare Elemente und Parameterdefinitionen, die für ein PrintCapabilities-Dokument gelten können.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Öffentliche PrintCapabilities-Schlüsselwörter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cccfa2cb22d8e784e8d4b82e548b9f4ae9772d1bd216573f5229d00f2f6d633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600620"
---
# <a name="printcapabilities-public-keywords"></a>Öffentliche PrintCapabilities-Schlüsselwörter

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Im folgenden Abschnitt werden sowohl vom Benutzer konfigurierbare Elemente als auch Parameterdefinitionen angegeben, die für ein PrintCapabilities-Dokument gelten können.

## <a name="user-configurable-elements-usage"></a>Verwendung von vom Benutzer konfigurierbaren Elementen

Vom Benutzer konfigurierbare Elemente stellen öffentliche Schlüsselwörter des Druckschemas dar, die entweder in einem PrintCapabilities-Dokument oder einem PrintTicket angezeigt werden können. Sie sollen konfigurierbare Geräteattribute darstellen, die von einem bestimmten Gerät unterstützt werden, oder die Absicht der Druckeinstellung von einer Anwendung oder einem Benutzer kommunizieren.

Benutzerkonfigurierbare Elemente können auf Parameterverweiselemente verweisen. Weitere Informationen finden Sie im Abschnitt [Parameterreferenzelemente.](parameter-reference-elements.md)

## <a name="parameter-definitions-usage"></a>Verwendung von Parameterdefinitionen

Parameterdefinitionen haben die Form von ParameterDef-Elementtypen in einem Print Capabilities-Dokument. ParameterDef-Elementtypen werden in einem PrintTicket mithilfe des ParameterInit-Elementtyps initialisiert. Der Wert des Parameters wird mit dem ParameterInit-Element angegeben. Ein vom Benutzer konfigurierbares Schlüsselwort kann mithilfe des ParameterRef-Elementtyps auf eine Parameterdefinition verweisen. Weitere Informationen finden Sie im Abschnitt [Parameterkonstrukte.](parameter-constructs.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



