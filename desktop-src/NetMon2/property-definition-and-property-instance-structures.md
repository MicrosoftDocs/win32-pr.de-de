---
description: Netzwerkmonitor stellt eine PropertyInfo-Struktur zum Definieren der Eigenschaften eines Protokolls und eine propertyinst-Struktur sowie eine propertyinstex-Struktur zum Definieren einer Instanz einer Eigenschaft bereit.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Eigenschafts Definition und eigenschafteninstanzstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756209"
---
# <a name="property-definition-and-property-instance-structures"></a>Eigenschafts Definition und eigenschafteninstanzstrukturen

Netzwerkmonitor stellt eine [**PropertyInfo**](propertyinfo.md) -Struktur zum Definieren der Eigenschaften eines Protokolls und eine [**propertyinst**](propertyinst.md)-Struktur sowie eine [**propertyinstex**](propertyinstex.md) -Struktur zum Definieren einer Instanz einer Eigenschaft bereit.

![Netzwerkmonitor Strukturen](images/property1.png)

Der Parser weist die [**PropertyInfo**](propertyinfo.md) -Struktur für alle Eigenschaften zu, die ein Protokoll unterstützt, und füllt diese aus. Der Parser übergibt die Struktur an Netzwerkmonitor, wo die Struktur der Protokoll [*Eigenschaften Datenbank*](p.md)hinzugefügt wird. Die Informationen in der **PropertyInfo** -Struktur werden beim Auswerten einer Instanz einer Eigenschaft und beim Formatieren der Daten verwendet, die in der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.

Netzwerkmonitor ordnet die Strukturen [**propertyinst**](propertyinst.md) und [**propertyinstex**](propertyinstex.md) zu, wenn der Parser eine Eigenschafts Definition an eine Instanz einer Eigenschaft anfügt.

Im folgenden Verfahren werden die Schritte beschrieben, die zum Anfügen einer Eigenschafts Definition erforderlich sind.

**So fügen Sie eine Eigenschaften Definition an**

1.  Identifizieren Sie jede Eigenschaft, die in einer Instanz des Protokolls vorhanden ist. Beim Anfügen einer Definition übergibt Netzwerkmonitor die erfassten Daten an den Parser. Die Daten werden auf der Basis einer Protokoll Instanz übermittelt.
2.  Bestimmen Sie den Speicherort der Eigenschaft in der Protokoll Instanz.
3.  Fügen Sie eine Eigenschaften Definition an den Speicherort der Eigenschaft an.

Netzwerkmonitor implementiert eine [**propertyinst**](propertyinst.md) -Struktur, wenn der Parser die Eigenschafts Daten verwendet, die in der Erfassung vorhanden sind. Netzwerkmonitor implementiert eine [**propertyinstex**](propertyinstex.md) -Struktur, wenn der Parser die Eigenschafts Daten in der Erfassung ändern muss.

 

 



