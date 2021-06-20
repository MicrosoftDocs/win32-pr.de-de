---
description: Erfahren Sie mehr über vom Benutzer konfigurierbare Elemente und Parameterdefinitionen, die möglicherweise auf ein PrintCapabilities-Dokument anwendbar sind.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Öffentliche PrintCapabilities-Schlüsselwörter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d836ca13297f031897598bb2ecbfc6588c49753
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407093"
---
# <a name="printcapabilities-public-keywords"></a>Öffentliche PrintCapabilities-Schlüsselwörter

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Im folgenden Abschnitt werden sowohl vom Benutzer konfigurierbare Elemente als auch Parameterdefinitionen angegeben, die auf ein PrintCapabilities-Dokument anwendbar sein können.

## <a name="user-configurable-elements-usage"></a>Benutzerkonfigurierbare Elementverwendung

Benutzerkonfigurierbare Elemente stellen öffentliche Schlüsselwörter des Druckschemas dar, die entweder in einem PrintCapabilities-Dokument oder einem PrintTicket-Dokument angezeigt werden können. Sie sollen konfigurierbare Geräteattribute darstellen, die von einem bestimmten Gerät unterstützt werden, oder die Absicht der Druckeinstellung durch eine Anwendung oder einen Benutzer kommunizieren.

Benutzerkonfigurierbare Elemente verweisen möglicherweise auf Parameterverweiselemente. Weitere Informationen finden Sie im Abschnitt [Parameterverweiselemente.](parameter-reference-elements.md)

## <a name="parameter-definitions-usage"></a>Verwendung von Parameterdefinitionen

Parameterdefinitionen haben die Form von ParameterDef-Elementtypen in einem Dokument Druckfunktionen. ParameterDef-Elementtypen werden in einem PrintTicket mithilfe des ParameterInit-Elementtyps initialisiert. Der Wert des Parameters wird mit dem ParameterInit-Element angegeben. Ein vom Benutzer konfigurierbares Schlüsselwort kann mithilfe des ParameterRef-Elementtyps auf eine Parameterdefinition verweisen. Weitere Informationen finden Sie im Abschnitt [Parameterkonstrukte.](parameter-constructs.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



