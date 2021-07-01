---
description: Grundlegendes zu Parametern im PrintCapabilities-Dokument. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parameter im PrintCapabilities-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118625"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parameter im PrintCapabilities-Dokument

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Wie unter [Parameterverweiselemente](parameter-reference-elements.md)erläutert, kann auf ParameterInit-Elemente innerhalb von Option-Instanzen verwiesen werden, aber das Parameterkonstrukt verfügt auch über eine Verwendung, die von diesem Elementtyp unabhängig ist.

Ein Beispiel für ein Gerätekonfigurationsattribut, das sich gut für die Parameterdarstellung eignet, ist CopyCount. Die zulässigen Werte für dieses Gerätekonfigurationsattribut können einfach und präzise definiert werden, ohne dass sie explizit aufgelistet werden. Obwohl es zwar mühsam wäre, jeden CopyCount-Wert in einer eigenen Option aufzulisten, können einige Gerätekonfigurationsattribute einfach nicht mit einem Feature-/Optionskonstrukt dargestellt werden. Betrachten Sie beispielsweise ein Gerät, das eine Textzeichenfolge akzeptiert, die dann verwendet wird, um auf jeder Ausgabeseite ein virtuelles Wasserzeichen zu erzeugen. Der Satz aller möglichen Textzeichenfolgen kann nicht einfach explizit aufzählen, aber die Textzeichenfolge kann leicht mithilfe eines ParameterDef-Elements beschrieben werden.

Das Dokument Print Schema Keywords (Schlüsselwörter für Druckschemas) definiert eine Reihe häufig verwendeter Parameterkonstrukte, aber PrintCapabilities-Anbieter können zusätzliche eigene Parameterkonstrukte definieren. Diese privat definierten Parameterkonstrukte sind jedoch nicht auf andere Geräte übertragbar, da ein von einer anderen Partei bereitgestelltes PrintCapabilities-Dokument ein solches Parameterkonstrukt nicht definiert. Unabhängig davon, ob schemadefiniert oder privat definiert, muss die ParameterDef-Instanz im PrintCapabilities-Dokument vorhanden sein, bevor der Parameter erkannt und von Clients verwendet wird. Diese Parameter werden als *festgelegte Parameter* bezeichnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



