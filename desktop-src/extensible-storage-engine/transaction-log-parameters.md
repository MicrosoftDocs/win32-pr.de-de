---
description: Weitere Informationen finden Sie im Artikel zu Transaktionsprotokoll Parametern.
title: Transaktionsprotokollparameters
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347526"
---
# <a name="transaction-log-parameters"></a>Transaktionsprotokollparameters


_**Gilt für:** Windows | Windows Server_

**Inhalt dieses Artikels:**  
Transaktionsprotokollparameters  
Requirements (Anforderungen)  
Weitere Informationen  

## <a name="transaction-log-parameters"></a>Transaktionsprotokollparameters

Dieses Thema enthält Parameter, die für Transaktionsprotokolle verwendet werden.

*JET_paramBaseName*  
3  

Mit diesem Parameter wird das drei Buchstabe festgelegt, das für viele der von der Datenbank-Engine verwendeten Dateien verwendet wird. Beispielsweise wird die Prüf Punkt Datei als EDB bezeichnet. Standardmäßig chk, da EDB der Standardbasis Name ist. Der Basisname kann verwendet werden, um problemlos zwischen Gruppen von Dateien zu unterscheiden, die zu unterschiedlichen Instanzen oder anderen Anwendungen gehören.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>&quot;EDB&quot;</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>3 Zeichen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCircularLog*  
17  

Mit diesem Parameter wird konfiguriert, wie Transaktionsprotokoll Dateien von der Datenbank-Engine verwaltet werden.

Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokoll Dateien auf dem Datenträger gespeichert, bis Sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank ausgeführt wurde. In diesem Modus ist es möglich, eine Wiederherstellung aus einer älteren Sicherung durchzuführen und alle beibehaltenen Transaktionsprotokoll Dateien durchzuführen, sodass keine Daten verloren gehen, weil der Notfall die Wiederherstellung erzwungen hat. Reguläre vollständige Sicherungen sind erforderlich, um zu verhindern, dass der Datenträger die Transaktionsprotokoll Dateien füllt.

Wenn die zirkuläre Protokollierung auf on festgehalten wird, werden nur Transaktionsprotokoll Dateien auf dem Datenträger beibehalten Der Vorteil dieses Modus besteht darin, dass keine Sicherungen erforderlich sind, um alte Transaktionsprotokoll Dateien abzukoppeln. Der Kompromiss besteht darin, dass eine Wiederherstellung ohne Datenverlust nicht mehr möglich ist.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>False</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCommitDefault*  
16  

Dieser Parameter steuert die Standardaktion, die ausgeführt wird, wenn für die äußere Transaktion ein Commit in einer Sitzung ausgeführt wird. Alle gültigen Optionen, die an [jetcommittransaction](./jetcommittransaction-function.md) übermittelt werden können, können auch als Standard für alle Sitzungen in einer Instanz und/oder für eine bestimmte Sitzung fest gegeben werden. Weitere Informationen zu diesen Optionen finden Sie unter [jetcommittransaction](./jetcommittransaction-function.md) .

Dieser Parameter wirkt sich auf die Zuverlässigkeit und Leistung von Transaktionen aus. Weitere Informationen finden Sie unter [jetcommittransaction](./jetcommittransaction-function.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>Eine gültige Option für jetcommittransaction.</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz oder Sitzung</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOldLogs*  
48  

Wenn dieser Parameter den Wert true hat und die Transaktionsprotokoll Dateien, auf die der Pfad der Protokolldatei (**JET_paramLogFilePath**) verweist, eine veraltete Version aufweisen, werden diese Transaktionsprotokoll Dateien automatisch gelöscht.

**Windows 2000:**  Beachten Sie beim Aktualisieren einer Datenbank von Windows NT auf Windows 2000 die Verwendung dieses Parameters. Wenn sich die Datenbank nicht in einem konsistenten Zustand befindet und die alten Protokolldateien gelöscht werden, geht der Inhalt der Datenbank verloren.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong>  Alarm</p>
<p><strong>Windows XP:</strong>  Fall</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Ja</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramIgnoreLogVersion*  
47  

Wenn dieser Parameter true ist, wird die Versionsnummer der Transaktionsprotokoll Datei von der Datenbank-Engine während [jetinit](./jetinit-function.md)nicht überprüft.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>False</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Ja</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Dieser Parameter stellt Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine bereit.

Derzeit werden die folgenden Optionen unterstützt:

JET_bitESE98FileNames

Wenn diese Option vorhanden ist, verwendet die Datenbank-Engine die folgenden Benennungs Konventionen für die zugehörigen Dateien:

  - Transaktionsprotokoll Dateien werden verwenden. Protokolldatei Erweiterung

  - Prüf Punkt Dateien verwenden. CHK für die Dateierweiterung

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0, JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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


*JET_paramLogBuffers*  
12  

Mit diesem Parameter wird die Menge an Arbeitsspeicher konfiguriert, die zum Zwischenspeichern von Protokolldaten Sätzen verwendet wird, bevor Sie in die Transaktionsprotokoll Datei geschrieben werden. Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokoll Dateien enthält. Die Sektorgröße beträgt fast immer 512 Bytes, sodass es sicher ist, dass diese Größe für die Einheit angenommen wird.

Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Auslastung der Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell vollständig werden. Eine größere Cache Größe für die Transaktionsprotokoll Datei ist wichtig für eine gute Aktualisierungs Leistung bei einer solchen hohen Lade Bedingung. Der Standardwert ist für diesen Fall zu klein.

**Windows XP und Windows 2000:**  Unter Windows XP und früheren Versionen wird empfohlen, diesen Parameter nicht auf eine Anzahl von größeren Puffern (in Bytes) als die Hälfte der Größe einer Transaktionsprotokoll Datei festzulegen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  80</p>
<p><strong>Windows Vista:</strong>  126</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  80 – 2147483647</p>
<p><strong>Windows Vista:</strong>  1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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


*JET_paramLogCheckpointPeriod*  
14  

Mit diesem Parameter wird die Datenbank-Engine so konfiguriert, dass ein Prüfpunkt erstellt wird, wenn die angegebene Anzahl von Protokolldatei Sektoren generiert wurde.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileCreateAsynch*  
69  

Wenn dieser Parameter auf true festgelegt ist, wird die nächste Transaktionsprotokoll Datei von der Datenbank-Engine erstellt, wenn die aktuelle Transaktionsprotokoll Datei verwendet wird. Die Absicht besteht darin, die Zeit zu verkürzen, die für den Wechsel von einer Transaktionsprotokoll Datei zur nächsten bei hoher Update Auslastung aufgewendet wurde.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Richtig</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFilePath*  
2 

Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners an, der die Transaktionsprotokolle für die Instanz enthalten soll. Der Pfad muss mit einem umgekehrten Schrägstrich beendet werden, was darauf hinweist, dass der Zielpfad ein Ordner ist. Die Transaktionsprotokoll Dateien enthalten die Informationen, die erforderlich sind, um die Datenbankdateien nach einem Absturz in einen konsistenten Zustand zu bringen. Sie werden normalerweise als EDB bezeichnet \* . Angezeigt. Der Inhalt der Transaktionsprotokoll Dateien ist ebenso wichtig (falls nicht mehr) als die Datenbankdateien selbst. Jeder Versuch sollte durchgeführt werden, um Sie zu schützen.

Es werden auch weitere Reservierungs Protokolldateien mit dem Namen "RES1" angezeigt. Log und RES2. Das Protokoll wird zusammen mit den normalen Protokolldateien gespeichert. Der Inhalt dieser Dateien ist nicht wichtig, da nur der Speicherplatz reserviert werden muss, damit die Engine in einem Szenario mit geringem Datenträger ordnungsgemäß heruntergefahren werden kann. Dabei handelt es sich auch um eine temporäre Protokolldatei mit dem Namen edbtmp. Melden Sie sich in demselben Ordner an. Der Inhalt dieser Datei ist entweder nicht wichtig. Bei dieser Datei handelt es sich um eine neue Protokolldatei, die zur Verwendung vorbereitet wird.

Die Eigenschaften des Host Volumens der Transaktionsprotokoll Dateien und deren Platzierung in Relation zu den anderen Dateien, die von der Datenbank-Engine verwendet werden, können sich erheblich auf die Leistung auswirken.

**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>&quot;.\& quot</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Ordner Pfad (Zeichenfolge)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 246 Zeichen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileSize*  
11  

Mit diesem Parameter wird die Größe der Transaktionsprotokoll Dateien konfiguriert. Jede Transaktionsprotokoll Datei hat eine Größe mit fester Größe. Die Größe entspricht der Einstellung dieses System Parameters in Einheiten von 1024 Byte.

Dieser Parameter wirkt sich auf die Zuverlässigkeit aus. Wenn die Einstellung zu klein ist, wird die maximale Anzahl von Protokolldateien (1048575) wesentlich schneller erreicht. In diesem Fall muss die Instanz ordnungsgemäß heruntergefahren werden, die vorhandenen Protokolldateien müssen gelöscht werden, und die Instanz muss neu gestartet werden. Durch diese Aktion wird nicht nur die Verfügbarkeit der Anwendung verringert, sondern auch alle vorherigen Sicherungen der Datenbank der Anwendung werden für ungültig erklärt.

Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Einstellung sehr groß ist, ist [jetinit](./jetinit-function.md) langsam, da die Datenbank-Engine die jüngste Protokolldatei (zumindest) lesen muss, wenn Sie initialisiert wird. Wenn die Einstellung sehr groß ist, dauert es auch länger, bis zwischen den Protokolldateien gewechselt wird. Wenn die Einstellung sehr klein ist, müssen für eine bestimmte Anzahl von Updates weitere Protokolldateien erstellt werden, die mehr Aufwand verursachen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>5120</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  128 – 32768</p>
<p><strong>Windows Vista:</strong>  64 – 32768</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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


*JET_paramLogWaitingUserMax*  
15  

Dieser Parameter versucht, die Leerung des Protokoll Puffers zu optimieren, der durch einen permanenten Commit verursacht wurde, indem auf eine angegebene Anzahl von Sitzungen gewartet wird, die auf einen permanenten Commit gewartet wird, bevor eine Leerung durchgeführt wird, um zu erzwingen, dass eine andere Transaktion den Löschvorgang gemeinsam verwendet.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>3</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramRecovery*  
34  

Dieser Parameter ist der Hauptschalter, der die Wiederherstellung von Abstürzen für eine-Instanz steuert. Wenn dieser Parameter auf "on" festgelegt ist, wird die Wiederherstellung im Aries-Stil verwendet, um alle Datenbanken in der Instanz in einen konsistenten Zustand zu bringen, wenn ein Prozess oder ein Computerabsturz erfolgt. Wenn dieser Parameter auf "Off" festgelegt ist, werden alle Datenbanken in der Instanz ohne den Vorteil der Wiederherstellung von Abstürzen verwaltet. Das heißt, wenn die Instanz nicht mit [jetterm](./jetterm-function.md) ordnungsgemäß heruntergefahren wird, bevor der Prozess beendet oder der Computer heruntergefahren wird, wird der Inhalt aller Datenbanken in dieser Instanz beschädigt.

Die Deaktivierung der Wiederherstellung ist in besonderen Situationen nützlich, in denen bekannt ist, dass der Inhalt einer Datenbank im Falle eines Absturzes nicht nützlich ist. Die Wiederherstellung sollte für alle anderen Fälle aktiviert werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>&quot;On&quot;</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 259 Zeichen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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


*JET_paramSystemPath*  
0  

Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners an, der die Prüf Punkt Datei für die Instanz enthalten soll. Der Pfad muss mit einem umgekehrten Schrägstrich beendet werden, was darauf hinweist, dass der Zielpfad ein Ordner ist. Die Prüf Punkt Datei ist eine einfache Datei, die pro Instanz verwaltet wird und die älteste Transaktionsprotokoll Datei speichert, die wiedergegeben werden muss, um alle Datenbanken in dieser Instanz nach einem Absturz in einen konsistenten Zustand zu bringen. Die Prüf Punkt Datei wird in der Regel als EDB bezeichnet. CHK.

**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>&quot;.\& quot</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Ordner Pfad (Zeichenfolge)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 246 Zeichen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramWaitLogFlush*  
13 

Dieser Parameter versucht, die Leerung des Protokoll Puffers zu optimieren, der durch einen permanenten Commit verursacht wurde, indem ein angegebener Zeitraum gewartet wird, bevor eine Leerung in der Hoffnung ausgelöst wird, dass der Löschvorgang von einer anderen Transaktion gemeinsam genutzt wird.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>0</p></td>
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
<td><p>Instanz oder Sitzung</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Dieser Parameter wird verwendet, um die Dateinamen Kompatibilitäts Features anzugeben, die mit Windows Server 2003 und dem vorherigen Datei Benennungs Schema verwaltet werden sollen. Weitere Informationen zu den verschiedenen Dateien und deren Benennung finden Sie unter [Extensible Storage Engine Files](./extensible-storage-engine-files.md).

Der JET_bitESE98FileNames stellt sicher, dass die Dateierweiterung, die für die Transaktionsprotokoll Dateien und die Prüf Punkt Datei verwendet wird, identisch mit der in Windows Server 2003 verwendeten Dateierweiterung ist. Hinweis Wenn Sie ein Upgrade von Windows Server 2003 ausführen, muss dieses Bit noch nicht angegeben werden, da die Engine die Dateierweiterungen automatisch aktualisiert, wenn JET_paramCircularLog auf **true** festgelegt ist, oder die ältere Protokollerweiterung beibehalten, wenn JET_paramCircularLog **false** ist.

**Hinweis**  Wenn Sie ein Bit festlegen möchten, sollte der Wert zuerst abgerufen und anschließend im gewünschten Kompatibilitäts Bit "oder" abgerufen werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Ab Windows Server 2008 und Windows Vista</p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a>Anforderungen

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[Jetterm](./jetterm-function.md)
