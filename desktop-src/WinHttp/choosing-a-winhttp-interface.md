---
description: Bevor Sie mit der Entwicklung einer WinHTTP-Anwendung (Microsoft Windows HTTP Services) beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Auswählen einer WinHTTP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d00777215ae94d32783f9cb98d0367c7e6499d6b3cd420a86859eac6d7654a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570300"
---
# <a name="choosing-a-winhttp-interface"></a>Auswählen einer WinHTTP-Schnittstelle

Bevor Sie mit der Entwicklung einer WinHTTP-Anwendung (Microsoft Windows HTTP Services) beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten. In der folgenden Tabelle sind die Vor- und Nachteile zusammengefasst, die den einzelnen Ansätzen zugeordnet sind.



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
<li>Antworten können in Blocken verarbeitet werden, was effizienter ist.</li>
<li>POST-Vorgänge können auch in Blocken verarbeitet werden, was die Verarbeitungszeit beschleunigt.</li>
<li>AutoProxy-Unterstützung.</li>
<li>Zugriff auf den vollständigen Funktionssatz von WinHTTP.</li>
<li>Binärdaten können problemlos verarbeitet werden.</li>
</ul></td>
<td><ul>
<li>Das Erstellen einer Anwendung ist einfach und erfordert weniger Codezeilen als die C/C++-API.</li>
<li>Die -Schnittstelle kann von Skriptsprachen verwendet werden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Nachteile</td>
<td><ul>
<li>Die Verarbeitung ist komplexer.</li>
<li>Die C/C++-API erfordert mehr Schritte als die COM-Schnittstelle, um die gleichen Aktionen durchzuführen.</li>
<li>Das Einrichten einer Anforderung erfordert mehr Code.</li>
</ul></td>
<td><ul>
<li>Die COM-Schnittstelle bietet keinen Zugriff auf den vollständigen Funktionssatz von WinHTTP.</li>
<li>Es ist schwierig, binäre Datentypen in einigen Skriptsprachen zu verarbeiten, z. B. VBScript und JScript.</li>
<li>AutoProxy wird von der COM-Schnittstelle nicht unterstützt.</li>
<li>Anwendungen müssen das COM-APARTMENT_THREADED verwenden.</li>
<li>Bevor eine Antwort verarbeitet werden kann, muss zunächst die gesamte Antwort empfangen und gepuffert werden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



