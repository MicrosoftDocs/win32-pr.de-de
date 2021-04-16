---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Hinzufügen von Eigenschaften Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393874"
---
# <a name="adding-property-instances"></a>Hinzufügen von Eigenschaften Instanzen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Mit dem Druck Schema können Eigenschaften Instanzen in einer Options Instanz vorhanden sein. Die im printfunktionalitäten-Dokument definierten Eigenschaften Instanzen werden nicht an die Options Instanzen weitergegeben, die in PrintTicket gespeichert sind. Eigenschaften Elemente wirken sich nicht auf das Ergebnis des Bewertungsprozesses aus, wenn zwei Options Instanzen verglichen werden, die ScoredProperty-Instanzen sich jedoch auf diesen Prozess auswirken. Alle Gerätetreiber, die einen Bewertungs Algorithmus implementieren, sollten diese Konvention beachten. Mithilfe von printfunktionsanbietern können einer Option Eigenschafts Instanzen hinzugefügt werden, wenn diese Instanzen für diese bestimmte Option spezifisch sind, oder wenn der Anbieter beabsichtigt, dass der Wert dieser Eigenschaft für jede Option in der Funktion angezeigt wird. Angenommen, die printrate-Eigenschaft ist abhängig von der Option, die für die Funktion PageResolution ausgewählt ist. Wenn die printrate-Eigenschaft auf der Stamm Ebene des printfunktionalitäten-Dokuments abgelegt wurde, wäre sie einwertig und würde nur die Druck Rate für die aktuell ausgewählte Auflösung widerspiegeln. Wenn jedoch die printrate-Eigenschaft in jeder PageResolution-Option platziert wurde, kann jede Instanz der printrate-Eigenschaft die Druck Rate für die PageResolution-Option widerspiegeln, in der Sie enthalten war. Das Dokument printfunktionalitäten enthält mehrere Definitionen für printrate, eines für jede PageResolution-Option. Mit einer kurz Darstellung enthalten die printfunktionen Folgendes:

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

In einigen Situationen ist das Platzieren einer Drucksatz Eigenschaft in jeder Auflösungs Option für den Client bequemer, da der Client auf einen Blick festlegen kann, welche Auswirkung die einzelnen Auflösungsoptionen auf die Druck Rate haben, ohne dass für jede Auflösungseinstellung ein neues printfunktionalitäten-Dokument erforderlich ist.

Beachten Sie auch, dass Eigenschaften Instanzen auch als untergeordnete Elemente von Funktions Elementen hinzugefügt werden können. Dies ist nützlich, wenn Eigenschafts Instanzen oder-Werte von Eigenschaften Instanzen vorhanden sind, die für die einzelnen Features spezifisch sind. Es kann z. b. eine Eigenschaft geben, die angibt, ob nur eine Option gleichzeitig für eine Funktion ausgewählt werden darf oder ob mehrere Optionen ausgewählt werden können. Dabei handelt es sich um die Auswahl \_ . Wählen Sie \_ viele in PPD-und GPD-Dateien verwendete Eigenschaften aus. Da einige featureinstanzen möglicherweise als Pick \_ 1 identifiziert werden, während andere als "Pick many" bezeichnet werden \_ , muss diese Eigenschaft für jede Funktion definiert werden. Wenn Sie die-Eigenschaft als untergeordnetes Element der-Funktion suchen, wird die Zuordnung zwischen der-Eigenschaft und der-Funktion erzeugt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



