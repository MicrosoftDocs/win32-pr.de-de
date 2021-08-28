---
description: 'Weitere Informationen zu: Temporäre Datenbankparameter'
title: Temporäre Datenbankparameter
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: 427ed51c2757075ccb28fd70e5554c49dc8db4e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986823"
---
# <a name="temporary-database-parameters"></a>Temporäre Datenbankparameter


_**Gilt für:** Windows | Windows Server_

## <a name="temporary-database-parameters"></a>Temporäre Datenbankparameter

Dieses Thema enthält Parameter, die für die temporäre Datenbank verwendet werden.

*JET_paramEnableTempTableVersioning*  
46  

Dieser Parameter steuert die Verwendung von Transaktionen in temporären Tabellen. Wenn dieser Parameter false ist, sind temporäre Tabellen schneller, aber es ist nicht möglich, ein Rollback von Aktualisierungen in einer Transaktion durchzuführen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Richtig</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramPageTempDBMin*  
19  

Dieser Parameter steuert die Anfangsgröße der temporären Datenbank. Die Größe wird auf Datenbankseiten angezeigt. Die Größe 0 (null) gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll.

Es ist häufig wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren. Wenn Sie diesen Parameter auf 14 festlegen, wird die kleinstmögliche temporäre Datenbank erreicht. Beachten Sie, dass die temporäre Datenbank auch vollständig entfernt werden kann, indem **JET_paramMaxTemporaryTables** auf 0 (null) festgelegt wird.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>0</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramTempPath*  
1  

Dieser Parameter gibt den relativen oder absoluten Dateisystempfad des Ordners oder der Datei an, der bzw. die die temporäre Datenbank für die Instanz enthalten soll. Wenn der Pfad zu einem Ordner ist, der die temporäre Datenbank enthält, muss er mit einem umgekehrten Schrägstrich beendet werden. Die temporäre Datenbank wird verwendet, um flüchtige Daten zu speichern, die bei der Verarbeitung von ESE-API-Informationsaufrufen, dem Erstellen von Indizes oder dem Speichern des Inhalts einer temporären Tabelle generiert werden.

**Hinweis**  Wenn ein relativer Pfad angegeben wird, ist er relativ zum aktuellen Arbeitsverzeichnis des Prozesses, der die Anwendung hostet, die die Datenbank-Engine verwendet.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>"tmp.edb"</p> | 
| <p>Typ:</p> | <p>Pfad (Zeichenfolge)</p> | 
| <p>Gültiger Bereich:</p> | <p>0 bis 247 Zeichen</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
