---
description: 'Weitere Informationen: Fehler Behandlungsparameter'
title: Fehler Behandlungsparameter
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
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868735"
---
# <a name="error-handling-parameters"></a>Fehler Behandlungsparameter


_**Gilt für:** Windows | Windows Server_

## <a name="error-handling-parameters"></a>Fehler Behandlungsparameter

Dieses Thema enthält Parameter, die für die Fehlerbehandlung verwendet werden.

*JET_paramErrorToString* 70  

Dieser Parameter kann verwendet werden, um eine [JET_ERR](./jet-err.md) in eine Zeichenfolge zu konvertieren. Dies erfolgt mithilfe eines speziellen Aufrufens von [jetgetsystemparameter](./jetgetsystemparameter-function.md) , bei dem der ganzzahlige Ausgabepuffer den zu konvertierenden [JET_ERR](./jet-err.md) Wert enthält (als Eingabeparameter), und der Zeichen folgen-Ausgabepuffer die übereinstimmende Fehler Zeichenfolge zurückgibt. Die Zeichenfolge sieht in etwa wie folgt aus: "JET_errSuccess, erfolgreicher Vorgang". Die Zeichenfolge besteht aus dem symbolischen Namen für die Zeichenfolge, einem Komma und einer einfachen Textbeschreibung des Fehlers. Die Beschreibungs Zeichenfolge kann selbst Kommas enthalten. Wenn der Fehler nicht erkannt wird, lautet die Zeichenfolge "Unbekannter Fehler, unbekannter Fehler".

**Hinweis**  Dieser Parameter ist schreibgeschützt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Sonderfunktionen</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Sonderfunktionen</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>Sonderfunktionen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
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

*JET_paramExceptionAction*  
98  

Dieser Parameter steuert, was geschieht, wenn eine Ausnahme von der Datenbank-Engine oder vom Code ausgelöst wird, der von der Datenbank-Engine aufgerufen wird. Wenn JET_ExceptionMsgBox festgelegt ist, wird eine Ausnahme für den Filter für nicht behandelte Windows-Ausnahmen ausgelöst. Dies führt dazu, dass die Ausnahme als Anwendungsfehler behandelt wird. Der Zweck besteht darin, dass der Anwendungscode fälschlicherweise versucht, eine Ausnahme abzufangen und zu ignorieren, die von der Datenbank-Engine generiert wurde. Dies ist nicht zulässig, da eine Daten Bank Beschädigung auftreten könnte. Wenn die Anwendung diese Ausnahmen ordnungsgemäß verarbeiten möchte, kann der Schutz deaktiviert werden, indem dieser Parameter auf JET_ExceptionNone festgelegt wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>JET_ExceptionMsgBox</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>JET_ExceptionMsgBox JET_ExceptionNone</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:  </strong>  Nein</p>
<p><strong>Windows Vista:</strong>  Zwar</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:  </strong>  Nein</p>
<p><strong>Windows Vista:</strong>  Zwar</p></td>
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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a>Weitere Informationen

[Fehler Behandlungs Konstanten](./error-handling-constants.md)  
[Fehler Codes für erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
