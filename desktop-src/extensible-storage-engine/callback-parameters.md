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
ms.openlocfilehash: 896e525008b0e0c524d940b0378d1225887ce8eb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987623"
---
# <a name="callback-parameters"></a>Rückrufparameter


_**Gilt für:** Windows | Windows Server_

## <a name="callback-parameters"></a>Rückrufparameter

Dieses Thema enthält Parameter, die für Rückrufe verwendet werden.

*JET_paramDisableCallbacks*  
65  

Dieser Parameter deaktiviert alle Datenbank-Engine-Rückrufe für von der Anwendung bereitgestellte Funktionen. Sie ist in erster Linie für die Unterstützung der Datenbank-Engine-Hilfsprogramme vorgesehen und nicht für die Verwendung in Ihrer Anwendung vorgesehen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

Dieser Parameter ermöglicht die Verwendung persistenter Rückrufe in der Datenbank. In Releases vor Windows Vista war die Verwendung von permanenten Rückrufen standardmäßig aktiviert. Anwendungen müssen jetzt explizit die Verwendung von permanenten Rückrufen zur Laufzeit mit diesem Parameter aktivieren. Wenn dieser Parameter nicht festgelegt ist, kann bei jedem Datenbankvorgang, der den Aufruf eines Rückrufs erfordert, ein Fehler JET_errCallbackFailed. Dieser Parameter wirkt sich nicht auf Rückrufe aus, die zur Laufzeit mit den folgenden Mechanismen angegeben werden: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)oder ein expliziter Rückrufparameter für eine JET-API. Es ist weiterhin möglich, Schemaelemente zu erstellen, die persistente Rückrufe enthalten, auch wenn die Verwendung dieser persistenten Rückrufe nicht möglich ist. Wenn dieser Parameter auf FALSE festgelegt ist, überschreibt er JET_paramDisableCallbacks.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und spätere Versionen</p> | 



*JET_paramRuntimeCallback*  
73  

Dieser Parameter konfiguriert die Engine mit einer Laufzeitrückruffunktion, die [die](./jet-callback-callback-function.md) JET_CALLBACK implementiert. Dieser Rückruf kann aus folgenden Gründen aufgerufen werden: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)oder [JET_cbtypNull](./jet-cbtyp.md). Weitere Informationen finden Sie unter [JetSetLS.](./jetsetls-function.md)


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>NULL</p> | 
| <p>Typ:</p> | <p>Funktionszeiger (JET_API_PTR)</p> | 
| <p>Gültiger Bereich:</p> | <p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
