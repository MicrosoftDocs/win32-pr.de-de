---
description: 'Weitere Informationen zu: Fehlerbehandlungsparameter'
title: Fehlerbehandlungsparameter
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a0556d97a0dda0182ee4fe229599030f523accd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474826"
---
# <a name="error-handling-parameters"></a>Fehlerbehandlungsparameter


_**Gilt für:** Windows | Windows Server_

## <a name="error-handling-parameters"></a>Fehlerbehandlungsparameter

Dieses Thema enthält Parameter, die für die Fehlerbehandlung verwendet werden.

*JET_paramErrorToString* 70  

Dieser Parameter kann verwendet werden, um eine [JET_ERR](./jet-err.md) in eine Zeichenfolge zu konvertieren. Dies erfolgt mit einem speziellen Aufruf von [JetGetSystemParameter,](./jetgetsystemparameter-function.md) wobei der Ganzzahlausgabepuffer den zu konvertierenden [JET_ERR](./jet-err.md) Wert enthält (als Eingabeparameter), und der Zeichenfolgenausgabepuffer die entsprechende Fehlerzeichenfolge zurückgibt. Die Zeichenfolge sieht in etwa wie folgt aus: "JET_errSuccess,Erfolgreicher Vorgang". Die Zeichenfolge besteht aus dem symbolischen Namen für die Zeichenfolge, einem Komma und einer einfachen Textbeschreibung des Fehlers. Die Beschreibungszeichenfolge kann selbst Kommas enthalten. Wenn der Fehler nicht erkannt wird, lautet die Zeichenfolge "Unbekannter Fehler, unbekannter Fehler".

**Hinweis**  Dieser Parameter ist schreibgeschützter Parameter.


| | | <p>Standardwert:</p> | <p>Sonderfunktionen</p> | | <p>Typ:</p> | <p>Sonderfunktionen</p> | | <p>Gültiger Bereich:</p> | <p>Sonderfunktionen</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Nein</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 


*JET_paramExceptionAction*  
98  

Dieser Parameter steuert, was geschieht, wenn eine Ausnahme von der Datenbank-Engine oder von code ausgelöst wird, der von der Datenbank-Engine aufgerufen wird. Wenn diese Einstellung auf JET_ExceptionMsgBox festgelegt ist, wird jede Ausnahme an den Windows Ausnahmefilter ausgelöst. Dies führt dazu, dass die Ausnahme als Anwendungsfehler behandelt wird. Die Absicht besteht darin, zu verhindern, dass Anwendungscode fälschlicherweise versucht, eine von der Datenbank-Engine generierte Ausnahme abzufangen und zu ignorieren. Dies kann nicht zugelassen werden, da eine Datenbankbeschädigung auftreten kann. Wenn die Anwendung diese Ausnahmen ordnungsgemäß behandeln möchte, kann der Schutz deaktiviert werden, indem dieser Parameter auf JET_ExceptionNone festgelegt wird.


| | | <p>Standardwert:</p> | <p>JET_ExceptionMsgBox</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>JET_ExceptionMsgBox, JET_ExceptionNone</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  Nein</p><p><strong>Windows Vista:</strong>  Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  Nein</p><p><strong>Windows Vista:</strong>  Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 


### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 


### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungskonstanten](./error-handling-constants.md)  
[Erweiterbare Storage Engine-Fehlercodes](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
