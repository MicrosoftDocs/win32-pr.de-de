---
description: Die Korrelation wirkt sich auf den Satz von Klassen aus, die vom SMIR zurückgegeben werden.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: WMI-SNMP-Klassenkorrelation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d795b7e998e3b7392baa45c23d688f1a2cef6a4069f6671d4c209788e7c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815703"
---
# <a name="wmi-snmp-class-correlation"></a>WMI-SNMP-Klassenkorrelation

Die Korrelation wirkt sich auf den Satz von Klassen aus, die vom SMIR zurückgegeben werden. Korrelierte Klassen sind klassen, die von einem bestimmten SNMP-Gerät zum Zeitpunkt der Enumeration unterstützt werden. Nicht korrelierte Enumeration gibt alle Klassen zurück, die in SMIR vorhanden sind, unabhängig davon, ob das Gerät sie unterstützt. Die Korrelation ist ein Feature des WMI-SNMP-Anbieters und kann deaktiviert oder aktiviert werden (Standardeinstellung).

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Die Korrelation verhindert möglicherweise, dass alle Klassen angezeigt werden, die tatsächlich von einem Gerät unterstützt werden. Wenn Sie wissen, dass eine bestimmte Klasse unterstützt wird, sie aber nicht im SMIR angezeigt wird, kann dies mehrere Gründe haben, von denen einer die Korrelation ist. Erwägen Sie, die Korrelation zu deaktivieren, bevor Sie auf das gerät schreiben. Das Deaktivieren der Korrelation führt jedoch zur Wahrscheinlichkeit, dass viele Klassen, die vom Gerät nicht unterstützt werden, im SMIR angezeigt werden. Außerdem gibt es Leistungskosten bei der Verwendung der Korrelation, da das Gerät abgefragt wird, um zu sehen, welche Klassen es unterstützt. Wenn die Korrelation aktiviert ist, verursacht der SNMP-Anbieter eine Enumeration von vom Gerät unterstützten Klassen, die dem Ergebnis der Ausführung eines *mib-Walk-Tools* ähnelt.

Ein Netzwerk-Manager möchte beispielsweise mehrere wichtige Daten zu allen verwalteten Hubs in einem bestimmten Netzwerk kennen. Eine Datenbank mit den aktuellen Geräten und den unterstützten MIBs ist bereits vorhanden, daher ist es nicht notwendig, sich auf die Korrelationsfunktion des Geräts zu verlassen, um die unterstützten Datenelemente bereitstellen zu können. In diesem Fall kann die Korrelation deaktiviert werden.

Das folgende Beispiel zeigt, wie die Korrelation deaktiviert wird.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



Auf der anderen Seite möchte ein anderer Netzwerk-Manager möglicherweise alle Laufwerke der UNIX-Computer im Netzwerk überwachen, ist aber mit den MIB-Daten auf diesen Computern nicht vertraut. In diesem Fall wird die Korrelation aktiviert.

 

 



