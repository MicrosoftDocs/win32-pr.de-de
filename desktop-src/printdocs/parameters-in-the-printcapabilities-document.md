---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parameter im printfunktionalitäten-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351829"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parameter im printfunktionalitäten-Dokument

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Wie in [Parameter Verweis Elementen](parameter-reference-elements.md)erläutert, kann auf parameterinit-Elemente in Options Instanzen verwiesen werden, aber das Parameter Konstrukt verfügt auch über eine Verwendung, die von diesem Elementtyp unabhängig ist.

Ein Beispiel für ein Geräte Konfigurations Attribut, das sich gut für die Parameter Darstellung eignet, ist CopyCount. Die zulässigen Werte für dieses Geräte Konfigurations Attribut können problemlos und kurz definiert werden, ohne dass Sie explizit aufgelistet werden. Obwohl es möglich wäre, aber mühsam jeden CopyCount-Wert in einer eigenen Option aufzulisten, können einige Geräte Konfigurations Attribute einfach nicht mithilfe eines Funktions-/optionskonstrukts dargestellt werden. Angenommen, ein Gerät akzeptiert eine Text Zeichenfolge, mit der dann auf jeder Ausgabe Seite ein virtueller Wasserzeichen erzeugt wird. Der Satz aller möglichen Text Zeichenfolgen kann nicht leicht explizit aufgelistet werden, aber die Text Zeichenfolge kann problemlos mithilfe eines ParameterDef-Elements beschrieben werden.

Das Dokument mit den Schlüsselwörtern für den Druck Schema definiert eine Reihe häufig verwendeter Parameterkonstrukte, aber printfunktionalitäten-Anbieter können zusätzliche eigene Parameter definieren. Diese privat definierten Parameterkonstrukte können jedoch nicht auf andere Geräte portiert werden, da ein von einer anderen Partei bereitgestelltes Printworks-Dokument kein solches Parameter Konstrukt definiert. Unabhängig davon, ob das Schema definiert oder privat definiert ist, muss die ParameterDef-Instanz im printfunktionalitäten-Dokument vorhanden sein, bevor der Parameter erkannt und von Clients verwendet wird. Diese Parameter werden als fest *gelegte Parameter* bezeichnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



