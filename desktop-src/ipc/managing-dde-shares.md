---
description: Network DDE stellt Funktionen bereit, mit denen Sie eine Freigabe löschen, Freigabe Informationen erhalten oder festlegen oder Freigaben aufzählen können.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Verwalten von DDE Shares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350949"
---
# <a name="managing-dde-shares"></a>Verwalten von DDE Shares

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Network DDE stellt Funktionen bereit, mit denen Sie eine Freigabe löschen, Freigabe Informationen erhalten oder festlegen oder Freigaben aufzählen können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Aufgabe</th>
<th>Prozedur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Löschen einer DDE-Freigabe</td>
<td>Verwenden Sie die <a href="nddesharedel.md"><strong>nddebug</strong></a> -Funktion.</td>
</tr>
<tr class="even">
<td>Informationen zur DDE-Freigabe erhalten</td>
<td>Verwenden Sie die <a href="nddesharegetinfo.md"><strong>ndde sharegetinfo</strong></a> -Funktion.</td>
</tr>
<tr class="odd">
<td>Festlegen der DDE-Freigabe Informationen</td>
<td>Verwenden Sie die <a href="nddesharesetinfo.md"><strong>nddesharesetinfo</strong></a> -Funktion.</td>
</tr>
<tr class="even">
<td>DDE-Freigaben aufzählen</td>
<td>Verwenden Sie die <a href="nddeshareenum.md"><strong>ndde ShareEnum</strong></a> -Funktion. Sie können auch die vertrauenswürdigen DDE-Freigaben mithilfe der <a href="nddetrustedshareenum.md"><strong>nddebug</strong></a> -Funktion auflisten.<br/></td>
</tr>
<tr class="odd">
<td>Auflisten verbundener Benutzer</td>
<td>Verwenden Sie die Funktion " <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>netzessionenum</strong></a> ".</td>
</tr>
<tr class="even">
<td>Ändern des DDE-Freigabe namens</td>
<td>Löschen Sie die alte Freigabe, und erstellen Sie eine neue Freigabe.
<ol>
<li>Rufen Sie die Freigabe Informationen mit <a href="nddesharegetinfo.md"><strong>nddesharegetinfo</strong></a>ab.</li>
<li>Entfernen Sie die Freigabe mit <a href="nddesharedel.md"><strong>ndabsharedel</strong></a>.</li>
<li>Ändern Sie den <strong>lpszsharename</strong> -Member der <a href="nddeshareinfo-str.md"><strong>ndbeshareinfo</strong></a> -Struktur, die von <a href="nddesharegetinfo.md"><strong>ndbesharegetinfo</strong></a>zurückgegeben wurde.</li>
<li>Übergeben Sie die geänderte <a href="nddeshareinfo-str.md"><strong>ndbeshareingefo</strong></a> -Struktur an <a href="nddeshareadd.md"><strong>ndabshareadd</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

