---
description: Weitere Informationen finden Sie unter Rückrufparameter.
title: Rückrufparameter
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9c14940ee98d4f664914794cd4ff6185b78dd04f438b982179a7ab3c5eb6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982810"
---
# <a name="callback-parameters"></a>Rückrufparameter


_**Gilt für:** Windows | Windows Server_

## <a name="callback-parameters"></a>Rückrufparameter

Dieses Thema enthält Parameter, die für Rückrufe verwendet werden.

*JET_paramDisableCallbacks*  
65  

Dieser Parameter deaktiviert alle Datenbank-Engine-Rückrufe für von der Anwendung bereitgestellte Funktionen. Sie ist in erster Linie für die Unterstützung der Datenbank-Engine-Hilfsprogramme vorgesehen und nicht für die Verwendung in Ihrer Anwendung vorgesehen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Falsch</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramEnablePersistedCallbacks*  
156  

Dieser Parameter ermöglicht die Verwendung persistenter Rückrufe in der Datenbank. In Versionen vor Windows Vista war die Verwendung persistenter Rückrufe standardmäßig aktiviert. Anwendungen müssen jetzt explizit die Verwendung von permanenten Rückrufen zur Laufzeit mit diesem Parameter aktivieren. Wenn dieser Parameter nicht festgelegt ist, wird bei jedem Datenbankvorgang, der den Aufruf eines Rückrufs erfordert, ein Fehler JET_errCallbackFailed. Dieser Parameter wirkt sich nicht auf Rückrufe aus, die zur Laufzeit mit den folgenden Mechanismen angegeben werden: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)oder ein expliziter Rückrufparameter für eine JET-API. Es ist weiterhin möglich, Schemaelemente zu erstellen, die persistente Rückrufe enthalten, auch wenn die Verwendung dieser persistenten Rückrufe nicht möglich ist. Wenn dieser Parameter auf FALSE festgelegt ist, überschreibt er JET_paramDisableCallbacks.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Falsch</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramRuntimeCallback*  
73  

Dieser Parameter konfiguriert die Engine mit einer Laufzeitrückruffunktion, die die [JET_CALLBACK](./jet-callback-callback-function.md) implementiert. Dieser Rückruf kann aus folgenden Gründen aufgerufen werden: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)oder [JET_cbtypNull](./jet-cbtyp.md). Weitere Informationen finden Sie unter [JetSetLS.](./jetsetls-function.md)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>NULL</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Funktionszeiger (JET_API_PTR)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und spätere Versionen</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
