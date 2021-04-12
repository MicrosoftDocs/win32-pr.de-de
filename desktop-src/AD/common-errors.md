---
title: Häufige Fehler (AD DS)
description: In der folgenden Tabelle finden Sie eine Liste mit häufigen Fehlern, die auf der Grundlage des Bereichs der zu Gruppier enden Gruppe auftreten können.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Allgemeine Fehler anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "104472180"
---
# <a name="common-errors-ad-ds"></a>Häufige Fehler (AD DS)

In der folgenden Tabelle finden Sie eine Liste mit häufigen Fehlern, die auf der Grundlage des Bereichs der zu Gruppier enden Gruppe auftreten können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>HRESULT</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x8007001f</td>
<td>Allgemeiner Fehler. Dieser Fehler tritt auf, wenn Sie Folgendes versuchen:
<ul>
<li>Fügen Sie einer globalen oder universellen Gruppe oder einer lokalen Gruppe einer Domäne in einer anderen Domäne eine lokale Domänen Gruppe hinzu. Lokale Domänen Gruppen können nur anderen lokalen Domänen Gruppen in derselben Domäne als Mitglieder hinzugefügt werden.</li>
<li>Fügen Sie einer globalen Gruppe eine universelle Gruppe hinzu. Universelle Gruppen können universellen und lokalen Domänen Gruppen, aber nicht globalen Gruppen hinzugefügt werden.</li>
</ul></td>
</tr>
<tr class="even">
<td>0x8007202f</td>
<td><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Dieser Fehler tritt auf, wenn Sie versuchen, einer anderen Gruppe in einer Domäne, die im gemischten Modus ausgeführt wird, eine Sicherheitsgruppe hinzuzufügen. Sicherheitsgruppen können nicht im gemischten Modus eingefügt werden. Sicherheitsgruppen können nur im einheitlichen Modus eingefügt werden.</td>
</tr>
</tbody>
</table>



 

 

 




