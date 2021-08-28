---
description: 'Weitere Informationen zu: Transaktionsprotokollparameter'
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
ms.openlocfilehash: 1d8f3ed19d01eece0b22e22b4a2a16d8d985751a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982177"
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

Dieser Parameter legt das Präfix mit drei Buchstaben fest, das für viele dateien verwendet wird, die von der Datenbank-Engine verwendet werden. Die Prüfpunktdatei heißt beispielsweise EDB. CHK standardmäßig, da EDB der Standardbasisname ist. Der Basisname kann verwendet werden, um problemlos zwischen Dateisätzen zu unterscheiden, die zu verschiedenen Instanzen oder anwendungen gehören.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>"edb"</p> | 
| <p>Typ:</p> | <p>String</p> | 
| <p>Gültiger Bereich:</p> | <p>3 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCircularLog*  
17  

Dieser Parameter konfiguriert, wie Transaktionsprotokolldateien von der Datenbank-Engine verwaltet werden.

Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokolldateien auf dem Datenträger beibehalten, bis sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank durchgeführt wurde. In diesem Modus ist es möglich, eine Wiederherstellung aus einer älteren Sicherung durchzuführen und alle beibehaltenen Transaktionsprotokolldateien so weiterzuspielen, dass aufgrund des Notfalls, der die Wiederherstellung erzwungen hat, keine Daten verloren gegangen sind. Regelmäßige vollständige Sicherungen sind erforderlich, um zu verhindern, dass der Datenträger mit Transaktionsprotokolldateien gefüllt wird.

Wenn die zirkuläre Protokollierung aktiviert ist, werden nur Transaktionsprotokolldateien, die älter als der aktuelle Prüfpunkt sind, auf dem Datenträger beibehalten. Der Vorteil dieses Modus besteht darin, dass sicherungen nicht erforderlich sind, um alte Transaktionsprotokolldateien abzumelden. Der Kompromiss besteht darin, dass eine Wiederherstellung ohne Datenverlust nicht mehr möglich ist.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCommitDefault*  
16  

Dieser Parameter steuert die Standardaktion, die ausgeführt wird, wenn für die äußerste Transaktion ein Commit für eine Sitzung ausgeführt wird. Jede gültige Option, die an [JetCommitTransaction](./jetcommittransaction-function.md) übergeben werden kann, kann auch als Standard für alle Sitzungen in einer Instanz und/oder für eine bestimmte Sitzung verwendet werden. Weitere Informationen zu diesen Optionen finden Sie unter [JetCommitTransaction.](./jetcommittransaction-function.md)

Dieser Parameter wirkt sich auf die Zuverlässigkeit und Leistung von Transaktionen aus. Weitere Informationen finden Sie unter [JetCommitTransaction.](./jetcommittransaction-function.md)


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>0</p> | 
| <p>Typ:</p> | <p>JET_GRBIT (ganze Zahl)</p> | 
| <p>Gültiger Bereich:</p> | <p>Eine gültige Option für JetCommitTransaction</p> | 
| <p>Umfang:</p> | <p>Instanz oder Sitzung</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramDeleteOldLogs*  
48  

Wenn dieser Parameter true ist und die Transaktionsprotokolldateien, auf die vom Protokolldateipfad (**JET_paramLogFilePath**) verwiesen wird, alle eine veraltete Version sind, werden diese Transaktionsprotokolldateien automatisch gelöscht.

**Windows 2000:**  Beim Upgrade einer Datenbank von Windows NT auf Windows 2000 muss bei der Verwendung dieses Parameters Vorsicht walten. Wenn sich die Datenbank nicht in einem konsistenten Zustand befindet und die alten Protokolldateien gelöscht werden, geht der Inhalt der Datenbank verloren.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000:</strong>  FALSE</p><p><strong>Windows XP:</strong>  STIMMT</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramIgnoreLogVersion*  
47  

Wenn dieser Parameter true ist, überprüft die Datenbank-Engine die Versionsnummer der Transaktionsprotokolldatei während [JetInit](./jetinit-function.md)nicht.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLegacyFileNames*  
136  

Dieser Parameter bietet Abwärtskompatibilität mit den Dateibenennungskonventionen früherer Versionen der Datenbank-Engine.

Die folgenden Optionen werden derzeit unterstützt:

JET_bitESE98FileNames

Wenn diese Option vorhanden ist, verwendet die Datenbank-Engine die folgenden Benennungskonventionen für ihre Dateien:

  - Transaktionsprotokolldateien verwenden . LOG für die Dateierweiterung

  - Prüfpunktdateien verwenden . CHK für die Dateierweiterung


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Typ:</p> | <p>JET_GRBIT (ganze Zahl)</p> | 
| <p>Gültiger Bereich:</p> | <p>0, JET_bitESE98FileNames</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höhere Versionen</p> | 



*JET_paramLogBuffers*  
12  

Dieser Parameter konfiguriert den Arbeitsspeicher, der zum Zwischenspeichern von Protokolldatensätzen verwendet wird, bevor sie in die Transaktionsprotokolldatei geschrieben werden. Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokolldateien enthält. Die Sektorgröße beträgt fast immer 512 Bytes, daher ist es sicher, diese Größe für die Einheit anzunehmen.

Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell voll werden. Eine größere Cachegröße für die Transaktionsprotokolldatei ist entscheidend für eine gute Updateleistung unter einem solchen hohen Auslastungszustand. Der Standardwert ist für diesen Fall bekanntlich zu klein.

**Windows XP und Windows 2000:**  Bei Windows XP und früheren Versionen wird davon abraten, diesen Parameter auf eine Anzahl von Puffern festzulegen, die größer (in Bytes) als die Hälfte der Größe einer Transaktionsprotokolldatei sind.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 80</p><p><strong>Windows Vista:</strong> 126</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 80 – 2147483647</p><p><strong>Windows Vista:</strong> 1 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLogCheckpointPeriod*  
14  

Mit diesem Parameter wird die Datenbank-Engine so konfiguriert, dass ein Prüfpunkt erstellt wird, wenn die angegebene Anzahl von Protokolldateisektoren generiert wurde.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>1024</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLogFileCreateAsynch*  
69  

Wenn dieser Parameter auf TRUE festgelegt ist, erstellt die Datenbank-Engine die nächste Transaktionsprotokolldatei, wenn die aktuelle Transaktionsprotokolldatei verwendet wird. Die Absicht besteht darin, den Zeitaufwand für den Wechsel von einer Transaktionsprotokolldatei zur nächsten bei hoher Updatelast zu minimieren.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Richtig</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramLogFilePath*  
2 

Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners an, der die Transaktionsprotokolle für die Instanz enthalten soll. Der Pfad muss mit einem umgekehrten Schrägstrich beendet werden, der angibt, dass der Zielpfad ein Ordner ist. Die Transaktionsprotokolldateien enthalten die Informationen, die erforderlich sind, um die Datenbankdateien nach einem Absturz in einen konsistenten Zustand zu bringen. Sie werden in der Regel als EDB \* bezeichnet. PROTOKOLL. Der Inhalt der Transaktionsprotokolldateien ist genauso wichtig (wenn nicht mehr), als die Datenbankdateien selbst. Es sollten alle Anstrengungen unternommen werden, um sie zu schützen.

Es gibt auch zusätzliche reservierte Protokolldateien mit dem Namen RES1. LOG und RES2. LOG wird zusammen mit den normalen Protokolldateien gespeichert. Der Inhalt dieser Dateien ist nicht wichtig, da ihr einziger Zweck darin besteht, Speicherplatz zu reservieren, damit die Engine in einem Szenario mit geringen Datenträgern ordnungsgemäß heruntergefahren werden kann. Dabei handelt es sich auch um eine temporäre Protokolldatei mit dem Namen EDBTMP. LOG in diesem Ordner. Der Inhalt dieser Datei ist ebenfalls nicht wichtig. Diese Datei ist eine neue Protokolldatei, die für die Verwendung vorbereitet wird.

Die Eigenschaften des Hostvolumes der Transaktionsprotokolldateien und ihre Platzierung relativ zu den anderen Dateien, die von der Datenbank-Engine verwendet werden, können die Leistung erheblich beeinträchtigen.

**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>".\"</p> | 
| <p>Typ:</p> | <p>Ordnerpfad (Zeichenfolge)</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 246 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLogFileSize*  
11  

Dieser Parameter konfiguriert die Größe der Transaktionsprotokolldateien. Jede Transaktionsprotokolldatei hat eine feste Größe. Die Größe entspricht der Einstellung dieses Systemparameters in Einheiten von 1.024 Bytes.

Dieser Parameter wirkt sich auf die Zuverlässigkeit aus. Wenn die Einstellung zu klein ist, wird die maximale Anzahl von Protokolldateien (1048575) viel schneller erreicht. In diesem Fall muss die Instanz sauber heruntergefahren werden, die vorhandenen Protokolldateien müssen gelöscht und die Instanz neu gestartet werden. Diese Aktion verringert nicht nur die Verfügbarkeit der Anwendung, sondern macht auch alle vorherigen Sicherungen der Anwendungsdatenbank ungültig.

Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Einstellung sehr groß ist, ist [JetInit](./jetinit-function.md) langsam, da die Datenbank-Engine bei der Initialisierung mindestens die neueste Protokolldatei lesen muss. Wenn die Einstellung sehr groß ist, dauert es auch länger, zwischen Protokolldateien zu wechseln. Wenn die Einstellung sehr klein ist, müssen für eine bestimmte Anzahl von Updates mehr Protokolldateien erstellt werden, was zu einem zusätzlichen Mehraufwand wird.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>5120</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 128 – 32768</p><p><strong>Windows Vista:</strong> 64 – 32768</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLogWaitingUserMax*  
15  

Dieser Parameter versucht, die Leerung des Protokollpuffers zu optimieren, der durch einen permanenten Commit verursacht wird, indem darauf gewartet wird, dass eine bestimmte Anzahl von Sitzungen auf einen dauerhaften Commit wartet, bevor eine Leerung erzwungen wird, in der Hoffen, dass die Leerung von einer anderen Transaktion gemeinsam verwendet wird.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>3</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramRecovery*  
34  

Dieser Parameter ist der Masterschalter, der die Absturzwiederherstellung für eine Instanz steuert. Wenn dieser Parameter auf "Ein" festgelegt ist, wird die Wiederherstellung im ARIES-Stil verwendet, um bei einem Prozess- oder Computerabsturz alle Datenbanken in der Instanz in einen konsistenten Zustand zu bringen. Wenn dieser Parameter auf "Off" festgelegt ist, werden alle Datenbanken in der Instanz ohne den Vorteil einer Absturzwiederherstellung verwaltet. Das heißt, wenn die Instanz nicht mit [JetTerm](./jetterm-function.md) vor dem Beenden oder Herunterfahren des Computers sauber heruntergefahren wird, wird der Inhalt aller Datenbanken in dieser Instanz beschädigt.

Das Deaktivieren der Wiederherstellung ist in besonderen Situationen nützlich, in denen bekannt ist, dass der Inhalt einer Datenbank bei einem Absturz nicht nützlich ist. Die Wiederherstellung sollte für alle anderen Fälle aktiviert sein.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>"Ein"</p> | 
| <p>Typ:</p> | <p>String</p> | 
| <p>Gültiger Bereich:</p> | <p>0 bis 259 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramSystemPath*  
0  

Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners an, der die Prüfpunktdatei für die Instanz enthält. Der Pfad muss mit einem umgekehrten Schrägstrich beendet werden, der angibt, dass der Zielpfad ein Ordner ist. Die Prüfpunktdatei ist eine einfache Datei, die pro Instanz verwaltet wird und die älteste Transaktionsprotokolldatei speichert, die wiedergegeben werden muss, um alle Datenbanken in dieser Instanz nach einem Absturz in einen konsistenten Zustand zu bringen. Die Prüfpunktdatei heißt in der Regel EDB. CHK.

**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>".\"</p> | 
| <p>Typ:</p> | <p>Ordnerpfad (Zeichenfolge)</p> | 
| <p>Gültiger Bereich:</p> | <p>0 bis 246 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramWaitLogFlush*  
13 

Dieser Parameter versucht, die Leerung des Protokollpuffers zu optimieren, die durch einen permanenten Commit verursacht wird, indem er auf einen bestimmten Zeitraum wartet, bevor eine Leerung erzwungen wird, in der Erwartung, dass eine andere Transaktion die Leerung gemeinsam verwendet.

**Windows XP:**  Ab Windows XP ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>0</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz oder Sitzung</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLegacyFileNames*  
136  

Dieser Parameter wird verwendet, um die Dateinamenkompatibilitätsfeatures anzugeben, die mit dem Windows Server 2003 und dem vorherigen Dateibenennungsschema verwaltet werden sollen. Weitere Informationen zu den verschiedenen Dateien und deren Benennung finden Sie unter [Extensible Storage Engine Files](./extensible-storage-engine-files.md).

Der JET_bitESE98FileNames stellt sicher, dass die in den Transaktionsprotokolldateien und der Prüfpunktdatei verwendete Dateierweiterung mit der in Windows Server 2003 verwendeten Datei identisch ist. Beachten Sie, dass bei einem Upgrade von Windows Server 2003 dieses Bit immer noch nicht angegeben werden muss, da die Engine die Dateierweiterungen automatisch aktualisiert, wenn JET_paramCircularLog auf **TRUE** festgelegt ist, oder die ältere Protokollerweiterung beibehalten wird, wenn JET_paramCircularLog **false** ist.

**Hinweis**  Um ein Bit festzulegen, sollte der Wert zuerst abgerufen werden, und dann "or" im gewünschten Kompatibilitätsbit.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Typ:</p> | <p>JET_GRBIT (ganze Zahl)</p> | 
| <p>Gültiger Bereich:</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



## <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
