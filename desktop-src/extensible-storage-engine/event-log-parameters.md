---
description: Weitere Informationen finden Sie unter Ereignisprotokollparameter.
title: Ereignisprotokollparameter
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 6fdf19d493e60cf229178872f7e33710210cfbec
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985333"
---
# <a name="event-log-parameters"></a>Ereignisprotokollparameter


_**Gilt für:** Windows | Windows Server_

## <a name="event-log-parameters"></a>Ereignisprotokollparameter

Dieses Thema enthält Parameter, die für das Ereignisprotokoll verwendet werden.

JET_paramEventLogCache  
Dieser Parameter steuert die Größe (in Bytes) eines Ereignisprotokoll-Nachrichtencaches, der ereignisprotokollierte Nachrichten enthält, die von der Datenbank-Engine ausgegeben werden, während der Eventlog-Dienst beendet wird. Diese zwischengespeicherten Nachrichten werden in das Ereignisprotokoll geleert, wenn der Dienst betriebsbereit wird. Alle Nachrichten, die über den Cache überlaufen, werden gelöscht.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>0</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramEventLoggingLevel*  
  
Dieser Parameter konfiguriert die Detailebene von Ereignisprotokollmeldungen, die von der Datenbank-Engine an das Ereignisprotokoll ausgegeben werden. Eine höhere Anzahl führt zu ausführlicheren Ereignisprotokollmeldungen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>JET_EventLoggingLevelMax</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramEventSource*  
4  

Dieser Parameter stellt eine anwendungsspezifische Zeichenfolge zur Verfügung, die allen Ereignisprotokollmeldungen hinzugefügt wird, die von der Datenbank-Engine ausgegeben werden. Dies ermöglicht eine einfache Korrelation von Ereignisprotokollmeldungen mit der Quellanwendung. Wenn eine leere Zeichenfolge angegeben wird (wie die Standardeinstellung), wird der Name der ausführbaren Hostanwendung verwendet.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>""</p> | 
| <p>Typ:</p> | <p>String</p> | 
| <p>Gültiger Bereich:</p> | <p>0 bis 259 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramEventSourceKey*  
49  

Dieser Parameter kann verwendet werden, um zu steuern, welches Ereignisprotokoll die Datenbank-Engine für ihre Ereignisprotokollmeldungen verwendet. Standardmäßig werden alle Ereignisprotokollmeldungen an das Anwendungsereignisprotokoll gesendet. Wenn der Registrierungsschlüsselname für ein anderes Ereignisprotokoll konfiguriert ist, werden stattdessen die Ereignisprotokollmeldungen dort angezeigt.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>""</p> | 
| <p>Typ:</p> | <p>String</p> | 
| <p>Gültiger Bereich:</p> | <p>0 bis 259 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramNoInformationEvent*  
50  

Wenn dieser Parameter true ist, werden Informationsereignisprotokollmeldungen unterdrückt, die normalerweise von der Datenbank-Engine generiert werden.


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
| <p>Betrifft Ressourcen:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
