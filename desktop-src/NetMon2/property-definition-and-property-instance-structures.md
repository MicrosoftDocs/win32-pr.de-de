---
description: Netzwerkmonitor eine PROPERTYINFO-Struktur zum Definieren der Eigenschaften eines Protokolls sowie eine PROPERTYINST- und PROPERTYINSTEX-Struktur zum Definieren einer Instanz einer Eigenschaft.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Eigenschaftendefinition und Eigenschafteninstanzstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8289c16bf501d36936b1aba6f292787e1b9a41babdb1225d3c0d53885c0ba31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676814"
---
# <a name="property-definition-and-property-instance-structures"></a>Eigenschaftendefinition und Eigenschafteninstanzstrukturen

Netzwerkmonitor stellt eine [**PROPERTYINFO-Struktur**](propertyinfo.md) zum Definieren der Eigenschaften eines Protokolls und eine [**PROPERTYINST-**](propertyinst.md)und [**PROPERTYINSTEX-Struktur**](propertyinstex.md) zum Definieren einer Instanz einer -Eigenschaft zur Unterstützung der Eigenschaften zurEntspricht.

![Netzwerküberwachungsstrukturen](images/property1.png)

Der Parser ordnet die [**PROPERTYINFO-Struktur**](propertyinfo.md) für alle Eigenschaften zu, die ein Protokoll unterstützt, und füllt sie aus. Der Parser übergibt die -Struktur an Netzwerkmonitor, an der die -Struktur der Protokolleigenschaftsdatenbank [*hinzugefügt wird.*](p.md) Die Informationen in der **PROPERTYINFO-Struktur** werden beim Analyse einer Instanz einer Eigenschaft und beim Formatieren der Daten verwendet, die auf der benutzeroberfläche Netzwerkmonitor werden.

Netzwerkmonitor ordnet die [**PROPERTYINST-**](propertyinst.md) und [**PROPERTYINSTEX-Strukturen**](propertyinstex.md) zu, wenn der Parser eine Eigenschaftendefinition an eine Instanz einer Eigenschaft anfügen.

Im folgenden Verfahren werden die erforderlichen Schritte zum Anfügen einer Eigenschaftendefinition beschrieben.

**So fügen Sie eine Eigenschaftendefinition an**

1.  Identifizieren Sie jede Eigenschaft, die in einer Instanz des Protokolls vorhanden ist. Beim Anfügen einer Definition übergibt Netzwerkmonitor die erfassten Daten an den Parser. Die Daten werden auf Protokollinstanzbasis übergeben.
2.  Bestimmen Sie den Speicherort der Eigenschaft in der Protokollinstanz.
3.  Fügen Sie eine Eigenschaftendefinition an den Speicherort der Eigenschaft an.

Netzwerkmonitor implementiert eine [**PROPERTYINST-Struktur,**](propertyinst.md) wenn der Parser die Eigenschaftsdaten verwendet, wie sie in der Erfassung vorhanden sind. Netzwerkmonitor implementiert eine [**PROPERTYINSTEX-Struktur,**](propertyinstex.md) wenn der Parser die Eigenschaftsdaten in der Erfassung ändern muss.

 

 



