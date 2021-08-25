---
description: 'Weitere Informationen zu: SystemParameters-Eigenschaften'
title: SystemParameters-Eigenschaften
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 13b2735f699fe2943dcb63bf262c8c708e61df754ed6799f2fb948119755d2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890678"
---
# <a name="systemparameters-properties"></a>SystemParameters-Eigenschaften

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [SystemParameters-Typ](./systemparameters-class.md) macht die folgenden Member verfügbar.

## <a name="properties"></a>Eigenschaften

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">BookmarkMost</a></td>
<td>Ruft die maximale Größe eines Lesezeichens ab. <a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Ruft die Größe des Datenbankcaches auf Seiten ab oder legt diese fest. Standardmäßig wird die Größe des Datenbankcaches automatisch angepasst. Wenn diese Eigenschaft auf einen Wert ungleich 0 festgelegt wird, wird der Cache an die Zielgröße angepasst.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>Ruft die maximale Größe des Datenbankseitencaches ab oder legt diese fest. Die Größe wird auf Datenbankseiten angezeigt. Wenn dieser Parameter auf seinen Standardwert festgelegt wird, wird die maximale Größe des Caches auf die Größe des physischen Arbeitsspeichers festgelegt, wenn JetInit aufgerufen wird.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>Ruft die Mindestgröße des Datenbankseitencaches auf Datenbankseiten ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>Ruft die maximale Anzahl von Komponenten in einem Sortier- oder Indexschlüssel ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuration</a></td>
<td>Ruft einen Wert ab, der die Standardwerte für den gesamten Satz von Systemparametern angibt, oder legt einen Wert fest. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameterwerte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden globale Systemparameter nicht auf ihre Standardwerte zurückgesetzt. Kleine Konfiguration (0): Die Datenbank-Engine ist für die Arbeitsspeichernutzung optimiert. Legacykonfiguration (1): Die Datenbank-Engine hat ihre herkömmlichen Standardwerte. Wird ab Windows Vista unterstützt. Wird auf Windows XP und Windows Server 2003 ignoriert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>Ruft die Größe der Datenbankseiten in Bytes ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableErweitert</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt, oder legt diesen fest. Dieser Parameter wird in Verbindung mit <a href="dn351218(v=exchg.10).md">Configuration</a> verwendet, um zu verhindern, dass einige Systemparameter von den Standardwerten der ausgewählten Konfiguration entfernt werden. Wird ab Windows Vista unterstützt. Wird auf Windows XP und Windows Server 2003 ignoriert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Datenbank-Engine den Betriebssystemdateicache für alle verwalteten Dateien verwenden soll, oder legt den Wert fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Datenbank-Engine speicherzuordnungsdatei-E/A für Datenbankdateien verwenden soll, oder legt den Wert fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>Ruft die Detailebene von Ereignisprotokollmeldungen ab, die von der Datenbank-Engine an das Ereignisprotokoll ausgegeben werden, oder legt diese fest. Höhere Zahlen führen zu ausführlicheren Ereignisprotokollmeldungen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ExceptionAction</a></td>
<td>Ruft den Wert ab, der codiert, was mit in JET generierten Ausnahmen geschehen soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">HungIOActions</a></td>
<td>Ruft den Satz von Aktionen ab, die für IOs ausgeführt werden sollen, die hängen angezeigt werden, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>Ruft den Schwellenwert für eine hängende E/A ab, auf die reagiert werden soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">KeyMost</a></td>
<td>Ruft die maximale Schlüsselgröße ab. Dies hängt von der Esent-Version und der Größe der Datenbankseite ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>Ruft die Abwärtskompatibilität mit den Dateibenennungskonventionen früherer Versionen der Datenbank-Engine ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Ruft die Größe der LV-Blöcke ab. Dies hängt von der Größe der Datenbankseite ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>Ruft die maximale Anzahl von Instanzen ab, die erstellt werden können, oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>Ruft die kleinste Datenmenge ab, die mit der XPRESS-Komprimierung komprimiert werden soll, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>Dieser Parameter steuert, wie viele Datenbankdatei-E/A-Warteschlangen pro Datenträger im Hostbetriebssystem gleichzeitig in die Warteschlange eingereiht werden können. Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich verbessern.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>Ruft den Anzeigenamen für diese Instanz des Prozesses ab oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>Ruft den Schwellenwert ab, ab dem der Datenbankseitencache beginnt, Seiten aus dem Cache zu entfernen, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden, oder legt diesen fest. Wenn die Anzahl der Seitenpuffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer kleiner als der durch JET_paramStopFlushThreshold festgelegte Stoppschwellenwert sein. Die Entfernungshöhe des Startschwellenwerts bestimmt die Antwortzeit, die der Datenbankseitencache benötigt, um verfügbare Puffer zu erzeugen, bevor die Anwendung sie benötigt. Ein hoher Startschwellenwert gibt dem Hintergrundprozess mehr Zeit zum Reagieren. Ein hoher Startschwellenwert impliziert jedoch einen höheren Stoppschwellenwert, der die effektive Größe des Datenbankseitencaches reduziert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>Ruft den Schwellenwert ab, an dem der Datenbankseitencache das Entfernen von Seiten aus dem Cache beendet, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden, oder legt diesen fest. Wenn die Anzahl der Seitenpuffer im Cache diesen Schwellenwert überschreitet, wird der Hintergrundprozess beendet, der gestartet wurde, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer größer als der Startschwellenwert sein, der von JET_paramStartFlushThreshold festgelegt wird. Der Abstand zwischen dem Startschwellenwert und dem Beendigungsschwellenwert wirkt sich auf die Effizienz aus, mit der Datenbankseiten vom Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten kombiniert werden können. Ein hoher Stopschwellenwert verringert jedoch die effektive Größe des Datenbankseitencaches.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[SystemParameters-Klasse](./systemparameters-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
