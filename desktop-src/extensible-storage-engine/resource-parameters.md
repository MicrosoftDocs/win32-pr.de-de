---
description: Weitere Informationen finden Sie unter Ressourcenparameter.
title: Ressourcenparameter
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 87c8c93e70950aca360e4aa9bad62b8280611c6713156dec80e4d11414f346d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978600"
---
# <a name="resource-parameters"></a>Ressourcenparameter


_**Gilt für:** Windows | Windows Server_

## <a name="resource-parameters"></a>Ressourcenparameter

Dieses Thema enthält Parameter, die für Ressourcen verwendet werden.

*JET_paramCachedClosedTables*  
125  

Dieser Parameter steuert die Anzahl der B+-Strukturressourcen, die von der -Instanz zwischengespeichert werden, nachdem die tabellen, die sie darstellen, von der Anwendung geschlossen wurden.

Große Werte für diesen Parameter führen dazu, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, erhöht jedoch die Geschwindigkeit, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 – 2147483647</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramDisablePerfmon*  
107  

Dieser Parameter kann verwendet werden, um zu verhindern, dass die Datenbank-Engine Daten zur Leistung veröffentlicht, um Windows. Dies kann durchgeführt werden, um die Dienstthreadaktivität der Datenbank-Engine zu reduzieren.

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
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramGlobalMinVerPages*  
81  

Mit diesem Parameter können Anwendungen, die im Modus mit mehreren Instanzen arbeiten, Vorabspeicher für Versionsseiten in einem globalen Pool zuordnen, um das ältere Verhalten zu emulieren. Dies ist nützlich, wenn die Anwendung garantieren möchte, dass Transaktionen einer bestimmten Größe später auch dann erfolgreich sein können, wenn der Arbeitsspeicher knapp wird.

**Windows 2000:**  Ausreichend Arbeitsspeicher zum Sichern aller Versionsseiten wird immer zur [JetInit-Zeit](./jetinit-function.md) reserviert.

**Windows XP:**  Ab dem Windows XP gilt dies weiterhin im Einzelinstanzmodus. Im Modus mit mehreren Instanzen wird der Versionsseitenspeicher jedoch dynamisch zugeordnet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCursors*  
8  

Dieser Parameter reserviert die angeforderte Anzahl von Cursorressourcen für die Verwendung durch eine -Instanz. Eine Cursorressource entspricht direkt einem [JET_TABLEID](./jet-tableid.md) Datentyp. Diese Einstellung wirkt sich darauf aus, wie viele Cursor gleichzeitig verwendet werden können. Eine Cursorressource kann nicht von verschiedenen Sitzungen gemeinsam genutzt werden, daher muss dieser Parameter auf einen ausreichend großen Wert festgelegt werden, damit jede Sitzung so viele Cursor verwenden kann, wie erforderlich sind.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxInstances*  
104  

Dieser Parameter steuert die maximale Anzahl von Instanzen, die in einem einzelnen Prozess erstellt werden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1-1024</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxOpenTables*  
6  

Dieser Parameter reserviert die angeforderte Anzahl von B+-Strukturressourcen für die Verwendung durch eine -Instanz. Diese Einstellung wirkt sich darauf aus, wie viele Tabellen gleichzeitig verwendet werden können. Dieser Parameter muss relativ zum physischen Schema der Datenbanken festgelegt werden, die von der Datenbank-Engine verwendet werden, sodass diese Einstellung nicht so einfach wie möglich ist.

Im Allgemeinen benötigen Sie zwei Ressourcen plus eine Ressource pro sekundärem Index pro Tabelle bei gleichzeitiger Verwendung durch die Anwendung.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>300</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxSessions*  
5  

Dieser Parameter reserviert die angeforderte Anzahl von Sitzungsressourcen für die Verwendung durch eine -Instanz. Eine Sitzungsressource [](./jet-sesid.md) entspricht direkt einem JET_SESID-Datentyp. Diese Einstellung wirkt sich darauf aus, wie viele Sitzungen gleichzeitig verwendet werden können.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 30000</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxTemporaryTables*  
10  

Dieser Parameter reserviert die angeforderte Anzahl temporärer Tabellenressourcen für die Verwendung durch eine -Instanz. Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

**Windows XP und höher:**  Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und alle Aktivitäten, die die verwendung der temporären Datenbank erfordern, schlagen fehl. Diese Einstellung kann nützlich sein, um die E/A zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich ist, wenn bekannt ist, dass sie nicht verwendet wird.

**Hinweis**  Die Verwendung einer temporären Tabelle erfordert auch eine Cursorressource.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>20</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxVerPages*  
9  

Dieser Parameter reserviert die angeforderte Anzahl von Versionsspeicherseiten für die Verwendung durch eine -Instanz. Der Versionsspeicher enthält einen Livedatensatz aller verschiedenen Versionen jedes Datensatzes oder Indexeintrags in der Datenbank, der von allen aktiven Transaktionen angezeigt werden kann. Diese Versionen werden verwendet, um die parallele Steuerung mit mehreren Versionen zu unterstützen, die von der Datenbank-Engine verwendet wird, um Transaktionen mit Momentaufnahmeisolation zu unterstützen. Diese Einstellung wirkt sich darauf aus, wie viele Updates gleichzeitig im Arbeitsspeicher gespeichert werden können. Dies wirkt sich wiederum auf die maximale Anzahl von Updates aus, die eine einzelne Transaktion ausführen kann, die maximale Dauer, die eine Transaktion geöffnet bleiben kann, die maximale gleichzeitige Auslastung von Aktualisierungstransaktionen im System oder eine Kombination dieser Transaktionen.

Jede version store-Seite, wie von diesem Parameter konfiguriert, hat eine Größe von 16 KB auf 32-Bit-Computern und 32 KB auf 64-Bit-Computern.

**Windows Vista und höher:**  Die Seitengröße des Versionsspeichers kann über JET_paramVerPageSize gelesen und geändert werden.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

**Hinweis**  Dies ist die mit Abstand gängigste Ressource, die von der Datenbank-Engine erschöpft wird. Die Einstellung des Systemparameters und die Transaktionslast der Anwendung müssen sorgfältig beachtet werden, um zu vermeiden, dass diese Ressource im normalen Betrieb ausgelastete wird. Wenn diese Ressource erschöpft ist, werden Aktualisierungen der Datenbank mit JET_errVersionStoreOutOfMemory abgelehnt. Um einige dieser Ressourcen freizugeben, muss die älteste ausstehende Transaktion abgebrochen werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramPageHintCacheSize*  
101  

Dieser Parameter steuert die Größe eines speziellen Caches, der verwendet wird, um die Suche nach untergeordneten Seitenzeigern der B+-Struktur im Datenbankseitencache zu beschleunigen. Die Größe des Caches ist in Bytes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
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
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und höhere Releases</p></td>
</tr>
</tbody>
</table>


*JET_paramPreferredMaxOpenTables*  
7  

Dieser Parameter versucht, die Anzahl der verwendeten B+-Strukturressourcen unter dem angegebenen Schwellenwert zu halten.

Wenn dieser Parameter auf 0 (null) festgelegt ist, wird standardmäßig 100 % der **JET_paramMaxOpenTables**.

**Windows Vista und höher:**  Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus. Anwendungen sollten stattdessen JET_paramMaxCachedClosedTables verwenden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>0 (100 % der <strong>JET_paramMaxOpenTables</strong>)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramPreferredVerPages*  
63  

Dieser Parameter stellt einen Schwellenwert relativ **zu** einem JET_paramMaxVerPages, der die diskrete Verwendung von Versionsseiten durch die Datenbank-Engine steuert. Wenn die Größe des Versionsspeichers diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundaufgaben verwendet werden, z. B. das Wiederverlangen von gelöschtem Speicherplatz in der Datenbank, stattdessen verfemt, um Platz für Transaktionsinformationen zu erhalten.

**Windows 2000, Windows XP und Windows Server 2003:**  Wenn Sie diesen Parameter auf 0 festlegen, wird der Schwellenwert auf 90 % **JET_paramMaxVerPages.**

**Windows Vista und höher:**  Dies wird nicht mehr unterstützt, und der Standardwert dieses Parameters wurde geändert, um sein Verhalten zu verdeutlichen.

Jede Mit diesem Parameter konfigurierte Versionsspeicherseite hat eine Größe von 16 KB auf 32-Bit-Computern und 32 KB auf 64-Bit-Computern.

**Windows Vista und höher:**  Die Seitengröße des Versionsspeichers kann über die JET_paramVerPageSize.

**Hinweis:**  Wenn die Datenbank-Engine zu oft über diesem Schwellenwert arbeitet, kann die Leistung der Datenbank beeinträchtigt werden. Dies liegt daran, dass die Hintergrundprozesse, die die Datenbank bereinigten, nicht ohne die optionalen Informationen funktionieren, die in diesem Szenario verworfen werden. Die Online- oder Offlinedefragmentierung wirkt sich auf diesen Effekt aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 (90 % der JET_paramMaxVerPages)</p>
<p><strong>Windows Vista:</strong> 58</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 – 2147483647</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramVerPageSize*  
128  

Dieser Parameter steuert die Größe der Versionsspeicherseiten, die von der Datenbank-Engine zum Speichern von Transaktionsinformationen verwendet werden. Der Wert dieses Parameters ist die Einheitengröße für alle anderen Systemparameter im Hinblick auf Versionsseiten (z. B. JET_paramMaxVerPages).

Die Datenbank-Engine verwendet möglicherweise eine größere Seitengröße des Versionsspeichers als angefordert.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>16384</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramVersionStoreTaskQueueMax*  
105  

Dieser Parameter steuert die Anzahl der Arbeitselemente für die Hintergrundbereinigung, die jederzeit im Datenbank-Engine-Threadpool in die Warteschlange gestellt werden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows XP und Windows Server 2003:</strong> 1 – 63</p>
<p><strong>Windows Vista:</strong> 1 – 127</p></td>
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
<td><p><strong>Windows XP und Windows Server 2003:</strong>  Nein</p>
<p><strong>Windows Vista:</strong>  Ja</p></td>
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
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
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
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
