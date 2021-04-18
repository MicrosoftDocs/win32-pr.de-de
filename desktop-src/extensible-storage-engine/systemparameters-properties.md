---
description: 'Weitere Informationen finden Sie hier: SystemParameters-Eigenschaften'
title: SystemParameters-Eigenschaften
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558439"
---
# <a name="systemparameters-properties"></a>SystemParameters-Eigenschaften

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [System Parameters](./systemparameters-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="properties"></a>Eigenschaften

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">Bookmarkmost</a></td>
<td>Ruft die maximale Größe eines Lesezeichens ab. <a href="dn292149(v=exchg.10).md">Jetgetbookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Ruft die Größe des Daten Bank Caches in Seiten ab oder legt diese fest. Standardmäßig wird der Daten Bank Cache automatisch seine Größe optimieren. wenn diese Eigenschaft auf einen Wert ungleich NULL festgelegt wird, wird der Cache an die Zielgröße angepasst.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">Cachesizemax</a></td>
<td>Ruft die maximale Größe des Cache für die Datenbankseite ab oder legt diese fest. Die Größe befindet sich auf Datenbankseiten. Wenn dieser Parameter auf seinen Standardwert zurückgesetzt wird, wird die maximale Cache Größe auf die Größe des physischen Arbeitsspeichers festgelegt, wenn jetinit aufgerufen wird.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">Cachesizemin</a></td>
<td>Ruft die Mindestgröße des Datenbankseiten Caches in Datenbankseiten ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">Columnskeymost</a></td>
<td>Ruft die maximale Anzahl von Komponenten in einem Sortier-oder Index Schlüssel ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuration</a></td>
<td>Ruft einen Wert ab, der die Standardwerte für den gesamten Satz von Systemparametern angibt, oder legt diesen fest. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt. Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert. Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen. Unterstützt unter Windows Vista und up. Wird unter Windows XP und Windows Server 2003 ignoriert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">Databasepagesize</a></td>
<td>Ruft die Größe der Datenbankseiten in Bytes ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">Enableadvanced</a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt. Dieser Parameter wird zusammen mit der <a href="dn351218(v=exchg.10).md">Konfiguration</a> verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden. Unterstützt unter Windows Vista und up. Wird unter Windows XP und Windows Server 2003 ignoriert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">Enablefilecache</a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine den Dateicache für alle verwalteten Dateien verwenden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">Enableviewcache</a></td>
<td>Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine für Datenbankdateien Datei-e/a für den Speicher</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">Eventlogginglevel</a></td>
<td>Ruft die Detailebene von EventLog-Meldungen ab, die von der Datenbank-Engine an das Ereignisprotokoll ausgegeben werden, oder legt diese fest. Höhere Zahlen führen zu ausführlicheren Ereignisprotokoll Meldungen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">Exceptionaction</a></td>
<td>Ruft den Wert ab oder legt ihn fest, was mit in Jet generierten Ausnahmen zu tun ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">Hungioactions</a></td>
<td>Ruft den Satz von Aktionen ab, die für IOS ausgeführt werden sollen, der nicht reagiert hat, oder legt ihn fest</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">Hungiothreshold</a></td>
<td>Ruft den Schwellenwert für das, was als nicht reagierender e/a angesehen wird, ab oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">Keymost</a></td>
<td>Ruft die maximale Schlüsselgröße ab. Dies hängt von der ESENT-Version und der Datenbankseiten Größe ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">Legacyfile-Namen</a></td>
<td>Ruft die Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">Lvchunksizemost</a></td>
<td>Ruft die Größe des LV-Blöcken ab. Dies hängt von der Größe der Datenbankseite ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">Maxinstance</a></td>
<td>Ruft die maximale Anzahl von Instanzen ab, die erstellt werden können, oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">Mindataforxpress</a></td>
<td>Ruft die kleinste Datenmenge ab, die mit der Xpress-Komprimierung komprimiert werden soll, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">Outstandingiomax</a></td>
<td>Mit diesem Parameter wird gesteuert, wie viele Datenbankdatei-e/a-Vorgänge pro Datenträger im Host Betriebssystem gleichzeitig in eine Warteschlange eingereiht werden können. Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich unterstützen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">Processfriendlyname</a></td>
<td>Ruft den anzeigen Amen für diese Instanz des Prozesses ab oder legt ihn fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">Startflushthreshold</a></td>
<td>Ruft den Schwellenwert ab oder legt diesen fest, an dem der Datenbankseiten Cache mit der Überprüfung von Seiten aus dem Cache beginnt, um Platz für nicht zwischengespeicherte Seiten zu schaffen. Wenn die Anzahl der Seiten Puffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um den Pool der verfügbaren Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer niedriger als der von JET_paramStopFlushThreshold festgelegte Schwellenwert sein. Die Entfernungs Höhe des Start Schwellenwerts bestimmt die Antwortzeit, die der Datenbankseiten Cache aufweisen muss, damit verfügbare Puffer erstellt werden, bevor die Anwendung Sie benötigt. Ein Schwellenwert für hohe Starts gibt dem Hintergrundprozess mehr Zeit für die Reaktion. Ein Schwellenwert für hohe Starts impliziert jedoch einen höheren Schwellenwert für die Beendigung, wodurch die effektive Größe des Datenbankseiten Caches verringert wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">Stopflushthreshold</a></td>
<td>Ruft den Schwellenwert ab, an dem der Datenbankseiten Cache die Überprüfung von Seiten aus dem Cache beendet, um Platz für nicht zwischengespeicherte Seiten zu schaffen, oder legt diesen fest. Wenn die Anzahl der Seiten Puffer im Cache über diesem Schwellenwert liegt, wird der Hintergrundprozess beendet, der zum Auffüllen dieses Pools verfügbarer Puffer gestartet wurde. Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer größer sein als der Start Schwellenwert, der durch JET_paramStartFlushThreshold festgelegt wird. Der Abstand zwischen dem Start Schwellenwert und dem Schwellenwert für das Abbrechen wirkt sich auf die Effizienz aus, mit der Datenbankseiten durch den Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten möglicherweise kombiniert werden. Ein Schwellenwert für hohe Beendigung verringert jedoch die effektive Größe des Datenbankseiten Caches.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[SystemParameters-Klasse](./systemparameters-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
