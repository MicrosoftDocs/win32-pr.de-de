---
description: Bevor Sie mit der Entwicklung einer Microsoft Windows HTTP-Dienste (WinHTTP)-Anwendung beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Auswählen einer WinHTTP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362523"
---
# <a name="choosing-a-winhttp-interface"></a>Auswählen einer WinHTTP-Schnittstelle

Bevor Sie mit der Entwicklung einer Microsoft Windows HTTP-Dienste (WinHTTP)-Anwendung beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten. In der folgenden Tabelle werden die vor-und Nachteile der einzelnen Ansätze zusammengefasst.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>C/C++-API</th>
<th>COM-Schnittstelle</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vorteile</td>
<td><ul>
<li>Antworten können in Blöcken verarbeitet werden, was effizienter ist.</li>
<li>Post-Vorgänge können auch in Blöcken verarbeitet werden, um die Verarbeitungszeit zu beschleunigen.</li>
<li>AutoProxy-Unterstützung.</li>
<li>Zugriff auf den vollständigen Featuresatz von WinHTTP.</li>
<li>Binäre Daten können problemlos behandelt werden.</li>
</ul></td>
<td><ul>
<li>Das Erstellen einer Anwendung ist einfach und erfordert weniger Codezeilen als die C/C++-API.</li>
<li>Die-Schnittstelle kann von Skriptsprachen verwendet werden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Nachteile</td>
<td><ul>
<li>Die Verarbeitung ist komplexer.</li>
<li>Die C/C++-API erfordert mehr Schritte als die COM-Schnittstelle, um die gleichen Aktionen auszuführen.</li>
<li>Das Einrichten einer Anforderung erfordert mehr Code.</li>
</ul></td>
<td><ul>
<li>Die COM-Schnittstelle bietet keinen Zugriff auf den vollständigen Featuresatz von WinHTTP.</li>
<li>Es ist schwierig, Binär Datentypen in einigen Skriptsprachen wie VBScript und JScript zu verarbeiten.</li>
<li>Die COM-Schnittstelle unterstützt AutoProxy nicht.</li>
<li>Anwendungen müssen das com-APARTMENT_THREADED Modell verwenden.</li>
<li>Bevor eine Antwort verarbeitet werden kann, muss zuerst die gesamte Antwort empfangen und gepuffert werden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



