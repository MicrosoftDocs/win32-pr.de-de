---
description: Korrelation wirkt sich auf den Satz von Klassen aus, die von SMIR zurückgegeben werden.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: WMI-SNMP-Klassen Korrelation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215442"
---
# <a name="wmi-snmp-class-correlation"></a>WMI-SNMP-Klassen Korrelation

Korrelation wirkt sich auf den Satz von Klassen aus, die von SMIR zurückgegeben werden. Korrelierte Klassen sind solche, die ein bestimmtes SNMP-Gerät unterstützt, wenn die Enumeration auftritt. Nicht korrelierte Enumeration gibt alle innerhalb des SMIR vorhandenen Klassen zurück, unabhängig davon, ob Sie vom Gerät unterstützt werden. Die Korrelation ist eine Funktion des WMI-SNMP-Anbieters und kann deaktiviert oder aktiviert werden (Standard).

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Mithilfe der Korrelation können alle Klassen angezeigt werden, die tatsächlich von einem Gerät unterstützt werden. Wenn Sie wissen, dass eine bestimmte Klasse unterstützt wird, aber nicht im SMIR angezeigt wird, kann dies auf verschiedene Gründe zurückzuführen sein, von denen eine Korrelation ist. Sie sollten die Korrelation deaktivieren, bevor Sie auf das betreffende Gerät schreiben. Das Deaktivieren der Korrelation führt jedoch zu der Wahrscheinlichkeit, dass viele vom Gerät nicht unterstützte Klassen in SMIR angezeigt werden. Außerdem entstehen bei der Verwendung der Korrelation Kosten für die Leistung, da das Gerät abgefragt wird, um zu sehen, welche Klassen es unterstützt. Wenn die Korrelation aktiviert ist, verursacht der SNMP-Anbieter eine Enumeration von Geräten unterstützten Klassen, die dem Ergebnis der Ausführung eines *MIB Walk* -Tools ähneln.

Ein Netzwerk-Manager möchte beispielsweise verschiedene wichtige Daten zu allen verwalteten Hubs in einem bestimmten Netzwerk kennen. Eine Datenbank der aktuellen Geräte und ihrer unterstützten MISB ist bereits vorhanden, daher besteht keine Notwendigkeit, sich auf die Korrelations Funktion des Geräts zu verlassen, um die unterstützten Datenelemente bereitzustellen. In diesem Fall könnte die Korrelation deaktiviert werden.

Im folgenden Beispiel wird gezeigt, wie die Korrelation deaktiviert wird.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



Andererseits kann ein anderer Netzwerk-Manager alle UNIX-Computer Laufwerke im Netzwerk überwachen, aber nicht mit den MIB-Daten auf diesen Computern vertraut sein. In diesem Fall würde die Korrelation aktiviert werden.

 

 



