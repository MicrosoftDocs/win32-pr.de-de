---
description: Berechnen des Aufwands mit netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Berechnen des Aufwands mit netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348182"
---
# <a name="calculating-overhead-with-netstat"></a>Berechnen des Aufwands mit netstat

Die Berechnung des Aufwands mit netstat sollte in einem stillen Netzwerk durchgeführt werden, um zu vermeiden, dass andere Netzwerk Datenverkehr von Daten verzerrt wird, z. b. Broadcast-oder Multicast Verkehr.

**So berechnen Sie den Netzwerk Aufwand einer Anwendung mithilfe von netstat**

1.  Rufen Sie die aktuelle Schnittstellen Statistik mithilfe von netstat ab.
2.  Führen Sie die Anwendung aus.
3.  Stellen Sie die Schnittstellen Statistik mit netstat wieder her.
4.  Berechnen Sie die Anzahl der Bytes, die zwischen den beiden netstat-Messungen empfangen werden.

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht diese Schritte, wobei Ttcp zum Senden von 10 Bytes an Daten, jeweils ein Byte, verwendet wird.

Zuerst wird ein theoretischer mehr Aufwand für die Anwendung berechnet. Für diesen Test sind alle Pakete 60 bytes (das mindestens Ethernet). Diese Übertragung erfordert drei Pakete, um die Verbindung einzurichten, 10 Datenpakete, 10 Bestätigungs Pakete (verzögerte Bestätigung wird fast jedes Mal ausgelöst) und vier Pakete, um die Verbindung ordnungsgemäß zu schließen.

Dies entspricht 27 Paketen mit jeweils 60 bytes, oder 1620 bytes (3 + 4 + 10 + 10) \* 60 = 1620). Da nur 10 Bytes an Daten übertragen werden, beträgt der mehr Aufwand 1610 bytes, was über 99% Protokoll Mehraufwand liegt.

### <a name="commands"></a>Befehle

**netstat-e**

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat-e**

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a>Berechnungen

**Gesendet:** 816 bytes

**Empfangen:** 674 bytes

**Bytes gesamt:** 1490

**Benutzer bytes:** 10

**Overhead:** 1480/1490 = 99,3%

* * Goodput: * * = 5 Bytes/Sekunde (oder 40 Bits/s)

> [!Note]  
> Tatsächlich übertragene Bytes stimmen nicht mit den theoretischen Werten aus, da die Füll Zeichen nicht in den netstat-Werten berücksichtigt werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsverhalten](application-behavior-2.md)
</dt> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



