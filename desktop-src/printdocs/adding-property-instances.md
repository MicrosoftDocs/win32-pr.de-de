---
description: Erfahren Sie mehr über das Hinzufügen von Eigenschafteninstanzen. Mit dem Druckschema können Eigenschaftsinstanzen in einer Option-Instanz vorhanden sein.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Hinzufügen von Eigenschafteninstanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409693"
---
# <a name="adding-property-instances"></a>Hinzufügen von Eigenschafteninstanzen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Mit dem Druckschema können Eigenschaftsinstanzen in einer Option-Instanz vorhanden sein. Die im PrintCapabilities-Dokument definierten Eigenschafteninstanzen werden nicht an die Option-Instanzen weitergegeben, die im PrintTicket gespeichert sind. Eigenschaftselemente wirken sich nicht auf das Ergebnis des Bewertungsprozesses aus, wenn zwei Optionsinstanzen verglichen werden, aber ScoredProperty-Instanzen wirken sich auf diesen Prozess aus. Alle Gerätetreiber, die einen Bewertungsalgorithmus implementieren, sollten diese Konvention einhalten. PrintCapabilities-Anbieter dürfen Einer Option Eigenschafteninstanzen hinzufügen, wenn diese Instanzen spezifisch für diese bestimmte Option und keine anderen sind oder wenn der Anbieter beabsichtigt, dass der Wert dieser Eigenschaft für jede Option in der Funktion angezeigt wird. Angenommen, die PrintRate-Eigenschaft hängt von der Option ab, die für das PageResolution-Feature ausgewählt wurde. Wenn die PrintRate-Eigenschaft auf der Stammebene des PrintCapabilities-Dokuments platziert würde, wäre sie einwertig und würde nur die Druckrate für die aktuell ausgewählte Auflösung widerspiegeln. Wenn die PrintRate-Eigenschaft jedoch innerhalb jeder PageResolution-Option platziert wird, kann jede Instanz der PrintRate-Eigenschaft die Druckrate für die PageResolution-Option widerspiegeln, die sie enthielt. Das PrintCapabilities-Dokument würde mehrere Definitionen für PrintRate enthalten, eine für jede PageResolution-Option. Mithilfe einer Kurzformdarstellung würden die PrintCapabilities Folgendes enthalten:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

In einigen Situationen ist das Platzieren einer Eigenschaft für die Druckrate innerhalb jeder Auflösungsoption für den Client praktischer, da der Client auf einen Blick den Effekt jeder Auflösungsoption auf die Druckrate bestimmen kann, ohne dass für jede Auflösungseinstellung ein neues PrintCapabilities-Dokument erhalten werden muss.

Beachten Sie auch, dass Eigenschafteninstanzen auch als untergeordnete Elemente von Feature-Elementen hinzugefügt werden können. Dies ist nützlich, wenn Eigenschafteninstanzen oder Werte von Eigenschafteninstanzen vorhanden sind, die für jedes Feature spezifisch sind. Beispielsweise kann eine Eigenschaft vorhanden sein, die angibt, ob nur eine Option gleichzeitig für ein Feature ausgewählt werden darf oder ob mehrere Optionen ausgewählt werden können. Dies ist die \_ PICK ONE- und PICK \_ MANY-Eigenschaft, die in PPD- und GPD-Dateien verwendet wird. Da einige Featureinstanzen als PICK ONE identifiziert werden \_ können, während andere als PICK MANY identifiziert werden \_ können, muss diese Eigenschaft für jedes Feature definiert werden. Das Suchen der Eigenschaft als untergeordnetes Element des Features erzeugt die Zuordnung zwischen der Eigenschaft und dem Feature.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



