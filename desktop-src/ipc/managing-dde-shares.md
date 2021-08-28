---
description: Network DDE stellt Funktionen bereit, mit denen Sie eine Freigabe löschen, Freigabeinformationen abrufen oder festlegen oder Freigaben aufzählen können.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Verwalten von DDE-Freigaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 145f9906ea2862bf5923b1678f574d495398e7ea9e59f0331b5560293480b86f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716810"
---
# <a name="managing-dde-shares"></a>Verwalten von DDE-Freigaben

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

Network DDE stellt Funktionen bereit, mit denen Sie eine Freigabe löschen, Freigabeinformationen abrufen oder festlegen oder Freigaben aufzählen können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Aufgabe</th>
<th>Vorgehensweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Löschen einer DDE-Freigabe</td>
<td>Verwenden Sie die <a href="nddesharedel.md"><strong>NDdeShareDel-Funktion.</strong></a></td>
</tr>
<tr class="even">
<td>Abrufen von DDE-Freigabeinformationen</td>
<td>Verwenden Sie die <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo-Funktion.</strong></a></td>
</tr>
<tr class="odd">
<td>Festlegen von DDE-Freigabeinformationen</td>
<td>Verwenden Sie die <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo-Funktion.</strong></a></td>
</tr>
<tr class="even">
<td>Aufzählen von DDE-Freigaben</td>
<td>Verwenden Sie die <a href="nddeshareenum.md"><strong>NDdeShareEnum-Funktion.</strong></a> Sie können die vertrauenswürdigen DDE-Freigaben auch mithilfe der <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum-Funktion aufzählen.</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Aufzählen verbundener Benutzer</td>
<td>Verwenden Sie die <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum-Funktion.</strong></a></td>
</tr>
<tr class="even">
<td>Ändern des DDE-Freigabenamens</td>
<td>Löschen Sie die alte Freigabe, und erstellen Sie eine neue Freigabe.
<ol>
<li>Rufen Sie die Freigabeinformationen mit <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>ab.</li>
<li>Entfernen Sie die Freigabe mithilfe von <a href="nddesharedel.md"><strong>NDdeShareDel.</strong></a></li>
<li>Ändern Sie den <strong>lpszShareName-Member</strong> der <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO-Struktur,</strong></a> die von <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>zurückgegeben wird.</li>
<li>Übergeben Sie die geänderte <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO-Struktur</strong></a> an <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

