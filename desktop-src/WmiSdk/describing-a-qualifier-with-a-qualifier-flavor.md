---
description: Eine qualifiziererkonfiguration ist ein Flag, das weitere Informationen zu einem Qualifizierer beschreibt.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215455"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>Beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration

Eine [*qualifiziererkonfiguration*](gloss-q.md) ist ein Flag, das weitere Informationen zu einem Qualifizierer beschreibt. Beispielsweise gibt die eingeschränkte qualifiziererkonfiguration an, dass WMI den zugeordneten Qualifizierer nicht an abgeleitete Klassen oder Instanzen weitergeben soll. Sie können die Varianten entweder mithilfe von MOF-Code oder Programm gesteuert festlegen. Obwohl Sie eine Vielzahl von Effekten mit-Variationen beschreiben können, besteht der Hauptzweck von eingabeflags darin, zu definieren, wie WMI Qualifizierer durch Vererbung propagiert.

WMI definiert mehrere qualifizierervarianten, die Sie an einen beliebigen Qualifizierer anfügen können, unabhängig vom Ursprung des Qualifizierers. Einige Varianten sind jedoch nicht für alle Qualifizierertypen geeignet. Beispielsweise ist die " **desubclass** "-Konfiguration nur für Qualifizierer geeignet, die für eine Klasse definiert wurden. Sie können " **desubclass** " nicht an einen Qualifizierer anfügen, um eine Instanz zu beschreiben.

Mithilfe von Varianten können Sie verschiedene Effekte für Qualifizierer beschreiben. Beispielsweise kann "Flavor" angeben, ob ein Qualifizierer lokalisiert werden kann. Einer der Hauptzwecke der qualifiziererkonfiguration besteht jedoch darin zu beschreiben, ob eine übergeordnete Klasse Qualifizierer an eine Unterklasse oder eine Klasseninstanz übergeben kann. Mithilfe von Varianten können Sie auch bestimmen, ob eine Klassen Eigenschaft einen Qualifizierer an eine Instanzeigenschaft übergibt. Verwenden Sie zum Schluss mithilfe von-Varianten, ob eine Unterklasse den ursprünglichen Wert eines geerbten Qualifizierers überschreiben kann. Qualifizierer, die Sie für eine Klasse oder eine Instanz deklarieren, werden jedoch nicht an die Eigenschaften dieser Klasse oder Instanz weitergegeben. Außerdem sind die Varianten, die Außerkraftsetzungs Berechtigungen einrichten, nur gültig, wenn Sie **auch die "** "-oder " **desubclass** "-Varianten festlegen.

Eine Konfiguration kann Global einem Qualifizierer für eine gesamte MOF-Datei zugewiesen werden. dabei wird die folgende Syntax verwendet, in der Leerraum als Trennzeichen fungiert, wenn mehrere Varianten angegeben werden.

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

Globale Varianten gelten für alle nachfolgenden Verwendungen des Qualifizierers in der MOF-Datei. Globale Geschmacks Anweisungen können an einer beliebigen Stelle in der Datei außerhalb eines objektdeklarations Blocks auftreten. Auf Klassen-, Instanz-oder Eigenschafts Ebene neu definierte Varianten überschreiben die globalen Geschmacks Deklarationen für den Gültigkeitsbereich dieses Objekts.

Sie können keine neue Konfiguration definieren. Obwohl Sie einen neuen Qualifizierer erstellen können, verwenden Sie nur vorhandene [qualifizierervarianten](qualifier-flavors.md) , um den neuen Qualifizierer zu beschreiben

**So definieren Sie qualifizierervarianten in MOF**

-   Deklarieren Sie die Varianten, die einen angegebenen Qualifizierer nach dem Qualifizierernamen beschreiben, zwischen den Qualifizierern Verwenden Sie Leerraum als Trennzeichen zwischen mehreren Varianten.

    Das folgende Beispiel zeigt das Muster für das Anfügen von vordefinierten Qualifizierern.

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

Sie können qualifizierervarianten nur Programm gesteuert in C++ hinzufügen. Dieser Vorgang ist in der Skript- [API für WMI](scripting-api-for-wmi.md)nicht verfügbar. Sie können jedoch einen neuen Qualifizierer hinzufügen, indem Sie " [**austauschen. hinzufügen**](swbemqualifierset-add.md)" aufrufen.

**So weisen Sie eine Konfiguration mithilfe von C++ zu**

-   Aufrufen der Methode [**iwbemqualifierset::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) mit dem *lflavor* -Parameter, der auf eine der für die Methode definierten Konstanten festgelegt ist.

 

 



