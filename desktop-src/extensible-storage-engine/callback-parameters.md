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
ms.openlocfilehash: a7b904c090852ea3990ac78e37a7ca851e152968
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465217"
---
# <a name="callback-parameters"></a>Rückrufparameter


_**Gilt für:** Windows | Windows Server_

## <a name="callback-parameters"></a>Rückrufparameter

Dieses Thema enthält Parameter, die für Rückrufe verwendet werden.

*JET_paramDisableCallbacks*  
65  

Dieser Parameter deaktiviert alle Datenbank-Engine-Rückrufe für von der Anwendung bereitgestellte Funktionen. Sie dient in erster Linie zur Unterstützung der Hilfsprogramme der Datenbank-Engine und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

Dieser Parameter ermöglicht die Verwendung persistenter Rückrufe in der Datenbank. In Releases vor Windows Vista war die Verwendung persistenter Rückrufe standardmäßig aktiviert. Anwendungen müssen jetzt explizit die Verwendung persistenter Rückrufe zur Laufzeit mit diesem Parameter aktivieren. Wenn dieser Parameter nicht festgelegt ist, schlägt jeder Datenbankvorgang, der den Aufruf eines Rückrufs erfordert, mit JET_errCallbackFailed fehl. Dieser Parameter wirkt sich nicht auf Rückrufe aus, die zur Laufzeit mit den folgenden Mechanismen angegeben werden: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)oder ein expliziter Rückrufparameter für eine JET-API. Es ist weiterhin möglich, Schemaelemente zu erstellen, die persistente Rückrufe enthalten, auch wenn die Verwendung dieser persistenten Rückrufe nicht zulässig ist. Wenn dieser Parameter auf FALSE festgelegt ist, überschreibt er JET_paramDisableCallbacks.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows Vista und höhere Versionen</p> | 



*JET_paramRuntimeCallback*  
73  

Dieser Parameter konfiguriert die Engine mit einer Laufzeitrückruffunktion, die die [JET_CALLBACK-Schnittstelle](./jet-callback-callback-function.md) implementiert. Dieser Rückruf kann aus folgenden Gründen aufgerufen werden: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)oder [JET_cbtypNull](./jet-cbtyp.md). Weitere Informationen finden Sie unter [JetSetLS.](./jetsetls-function.md)


| | | <p>Standardwert:</p> | <p>NULL</p> | | <p>Typ:</p> | <p>Funktionszeiger (JET_API_PTR)</p> | | <p>Gültiger Bereich:</p> | <p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
