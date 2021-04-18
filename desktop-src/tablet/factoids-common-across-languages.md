---
description: Eine Reihe von Faktoiden beschreibt Eingaben, die für alle sprach erkenungen gelten und keine unterschiedlichen Formate für verschiedene Sprachen aufweisen müssen. In der folgenden Tabelle sind die in allen Sprachen gemeinsamen Faktoide aufgeführt.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Sprachen übergreifende Facetten übergreifende Faktoide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343696"
---
# <a name="factoids-common-across-languages"></a>Sprachen übergreifende Facetten übergreifende Faktoide

Eine Reihe von Faktoiden beschreibt Eingaben, die für alle sprach erkenungen gelten und keine unterschiedlichen Formate für verschiedene Sprachen aufweisen müssen. In der folgenden Tabelle sind die in allen Sprachen gemeinsamen Faktoide aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Faktoid</th>
<th>Definition</th>
<th>Beispiele</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Mittleren</strong></td>
<td>Legt den Wert für eine einzelne Ziffer fest. Die Erkennung ist darauf ausgerichtet, nur einzelne Ziffern zurückzugeben, wenn diese Faktoid festgelegt ist.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>E-Mail</strong></td>
<td>Legt einen Bias für eine e-Mail-Adresse fest.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Legt die Abweichung für verschiedene URL-Formate fest.<br/>
<blockquote>
[!Note]<br />
Die Standardeinstellungen für die Erkennung beinhalten das <strong>webfaktoid</strong> . Daher bemerken Sie möglicherweise keinen großen Unterschied zwischen der <strong>webfaktoid</strong> und der Standardeinstellung. Die <strong>Web</strong> -ID unterstützt jedoch die Beseitigung von Leerzeichen zwischen Wörtern in einer URL.
</blockquote>
<br/></td>
<td>http: \\ Microsoft.net<br/> https://microsoft.us/<br/> https: \\ www.Microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world. com<br/> www.Microsoft.US \<br/> http: \\www.microsoft.com\myfile.htm<br/> http: \\www.microsoft.com\myfile.html<br/> http: \\ www. Microsoft. com\meinedatei.ASP<br/> http: \\ www.Microsoft.uk<br/> http: \\ www.Microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>Standard</strong></td>
<td>Gibt die Erkennungsfunktion auf die Standardeinstellungen zurück.<br/></td>
<td>Die Standardeinstellung für Faktoide für westliche Sprachen umfasst das System Wörterbuch, das Benutzerwörterbuch, verschiedene interpunlierungen und die <strong>Web</strong> -und <strong>Number</strong> -Faktoide.<br/> Die Standardeinstellung für Faktoide für ostasiatische Sprachen enthält alle Zeichen, die von der Erkennung unterstützt werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>None</strong></td>
<td>Deaktiviert alle Faktoide, Wörterbücher und das Sprachmodell.<br/></td>
<td>Diese Faktoid sollte nur verwendet werden, wenn Sie nicht möchten, dass die Erkennung Grammatikregeln oder-Wörterbücher verwendet, einschließlich des System Wörterbuchs. Diese Faktoid eignet sich für die Eingabe zufälliger Zeichen folgen, wie z. b. Produktcodes. Verwenden Sie das coerce-Flag nicht mit diesem Faktoid.<br/></td>
</tr>
</tbody>
</table>



 

 

 




