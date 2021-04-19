---
description: 'Weitere Informationen finden Sie hier: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
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
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359497"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**Gilt für:** Windows | Windows Server_

## <a name="jet_cbtyp"></a>JET_CBTYP

Die **JET_CBTYP** Gruppe von Konstanten beschreibt alle möglichen Punkte in einem Vorgang, die von der Datenbank-Engine durch Aufrufen der [JET_CALLBACK](./jet-callback-callback-function.md) Callback-Funktion benachrichtigt werden. Die Datenbank-Engine übergibt eine dieser Konstanten im *cbyp* -Parameter der Rückruffunktion. Die Bedeutung der anderen Parameter, die von der Datenbank-Engine in diesem-Befehl weitergegeben werden, hängt von der spezifischen **JET_CBTYP** ab.

**Windows XP:**  Die **JET_CBTYP** Gruppe von Konstanten wird in Windows XP eingeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante/Wert</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_cbtypNull<br />
0x00000000</p></td>
<td><p>Dieser Rückruf ist reserviert und wird immer als ungültig angesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Dieser Rückruf ist für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Dieser Rückruf tritt direkt vor dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen <a href="gg269288(v=exchg.10).md">jetupdate</a>-Rückruf auf.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert. Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>gsid</em>: die Sitzung, die den einzufügenden Datensatz enthält.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den einzufügenden Datensatz enthält.</p></li>
<li><p><em>TableID</em>: der Cursor, der den neuen Datensatz vorbereitet hat, der eingefügt werden soll. Es ist wichtig zu beachten, dass der Wert einer beliebigen Version oder der AutoIncrement-Spalten zu diesem Zeitpunkt möglicherweise nicht korrekt ist.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong> wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Dieser Rückruf tritt unmittelbar nach dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">jetupdate</a> auf, aber bevor <a href="gg269288(v=exchg.10).md">jetupdate</a> an seinen Aufrufer zurückgegeben wird.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert. Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>ssisid</em>: die Sitzung, die den soeben eingefügten Datensatz enthält.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den soeben eingefügten Datensatz enthält.</p></li>
<li><p><em>TableID</em>: ein Cursor in der Tabelle, in die der soeben eingefügte Datensatz eingefügt wurde. Beachten Sie, dass sich der Cursor immer noch auf demselben Index Eintrag befindet wie der vor dem Einfügen-Rückruf. Beachten Sie, dass dieser Index Eintrag in keiner Weise mit dem eingefügten Datensatz verknüpft werden kann.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong> , wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Dieser Rückruf tritt direkt vor einem vorhandenen Datensatz in einer Tabelle auf, die durch einen <a href="gg269288(v=exchg.10).md">jetupdate</a>-Rückruf geändert wird.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert. Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>gsid</em>: die Sitzung, die den Datensatz enthält, der geändert werden soll.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den zu ändernden Datensatz enthält.</p></li>
<li><p><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der dem Datensatz zugeordnet ist, der geändert werden soll. Es ist wichtig zu beachten, dass der Wert einer beliebigen Version oder der AutoIncrement-Spalten zu diesem Zeitpunkt möglicherweise nicht korrekt ist.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong> wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">jetupdate</a> geändert wurde, aber bevor <a href="gg269288(v=exchg.10).md">jetupdate</a> an seinen Aufrufer zurückgegeben wurde.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert. Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>ssisid</em>: die Sitzung mit dem Datensatz, der soeben geändert wurde.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den soeben geänderten Datensatz enthält.</p></li>
<li><p><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der dem Datensatz zugeordnet ist, der gerade geändert wurde.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong> , wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Dieser Rückruf tritt auf, kurz bevor ein vorhandener Datensatz in einer Tabelle durch einen <a href="gg269315(v=exchg.10).md">jetdelete</a>-Rückruf gelöscht wird.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert. Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>gsid</em>: die Sitzung, die den Datensatz enthält, der gelöscht werden soll.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den zu löschenden Datensatz enthält.</p></li>
<li><p><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der mit dem zu löschenden Datensatz verknüpft ist.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong> wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269315(v=exchg.10).md">jetdelete</a> gelöscht wurde, aber bevor <a href="gg269315(v=exchg.10).md">jetdelete</a> an seinen Aufrufer zurückgegeben wird.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert. Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>ssisid</em>: die Sitzung, die den soeben gelöschten Datensatz enthält.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den soeben gelöschten Datensatz enthält.</p></li>
<li><p><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der mit dem soeben gelöschten Datensatz verknüpft ist.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong></p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die Engine den benutzerdefinierten Standardwert einer Spalte aus der Anwendung abrufen muss. Bei diesem Rückruf handelt es sich im Wesentlichen um eine eingeschränkte Implementierung von <a href="gg269198(v=exchg.10).md">jetretrievecolumgen</a> , die von der Anwendung ausgewertet wird. Für einen benutzerdefinierten Standardwert können maximal ein Spaltenwert zurückgegeben werden.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird entweder über eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur an <a href="gg294122(v=exchg.10).md">jetaddcolumn</a> übergeben oder mithilfe einer <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur in einer <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur in einer <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> Struktur an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>SSID</em>: die Sitzung, von der der benutzerdefinierte Standardwert berechnet wird.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Tabelle, die den benutzerdefinierten Standardwert enthält.</p></li>
<li><p><em>TableID</em>: ein Cursor, der auf dem Datensatz positioniert ist, für den der benutzerdefinierte Standardwert abgerufen wird.</p></li>
<li><p><em>pvArg1</em>: der Ausgabepuffer für den benutzerdefinierten Standardwert.</p></li>
<li><p><em>pvArg2</em>: bei Eingabe ist dies die Größe des Ausgabepuffers. Bei der Ausgabe ist dies die tatsächliche Größe des benutzerdefinierten Standardwerts. in beiden Fällen ist die Größe eine 32-Bit-Ganzzahl ohne Vorzeichen.</p></li>
<li><p><em>pvcontext</em>: ein Zeiger auf einen Puffer, der die Benutzerdaten enthält, die in der <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur beim Erstellen der Spalte angegeben wurden, oder NULL, wenn kein Kontext angegeben wurde.</p></li>
<li><p><em>ulungenutzt</em>: die Spalten-ID der Spalte, für die der benutzerdefinierte Standardwert abgerufen wird.</p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</p>
<p>Wenn JET_wrnBufferTruncated durch den Rückruf zurückgegeben wird, wird der Vorgang fortgesetzt, aber der gesamte Wert wird während des Rückrufs nicht abgerufen.</p>
<p>Wenn JET_wrnColumnNull durch den Rückruf zurückgegeben wird, wird der Vorgang fortgesetzt, aber der benutzerdefinierte Standardwert für die Spalte ist NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die Online Defragmentierung einer Datenbank, die von <a href="gg269317(v=exchg.10).md">jetdefragment</a> initiiert wurde, beendet wurde, weil entweder der Prozess abgeschlossen oder das Zeitlimit erreicht wurde.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird an <a href="gg269317(v=exchg.10).md">jetdebug-Fragment</a>übermittelt. Weitere Informationen finden Sie unter <a href="gg269317(v=exchg.10).md">jetdefragment</a>.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>gsid</em>: die Sitzung, mit der die Online Defragmentierung für die Datenbank oder JET_sesidNil für eine Streamingdatei durchgeführt wird.</p></li>
<li><p><em>DBID</em>: die Datenbank-ID der Datenbank, die defragmentiert oder für eine Streamingdatei JET_dbidNil.</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: <strong>null</strong></p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong></p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einem Cursor zugeordnet ist, der von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter <a href="gg269243(v=exchg.10).md">jetsetls</a>.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>konfiguriert.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p>- <em>sid</em>: JET_sesidNil</p></li>
<li><p><em>DBID</em>: JET_dbidNil</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: das mit <a href="gg269243(v=exchg.10).md">jetsetls</a> festgelegte Kontext Handle</p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: <strong>null</strong></p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong></p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einer Tabelle zugeordnet ist, die von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter <a href="gg269243(v=exchg.10).md">jetsetls</a>.</p>
<p>Der Funktionszeiger für diesen Rückruf Grund wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>konfiguriert.</p>
<p>Die Rückruf Parameter verfügen über die folgenden Werte:</p>
<ul>
<li><p>- <em>sid</em>: JET_sesidNil</p></li>
<li><p><em>DBID</em>: JET_dbidNil</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: das Kontext Handle, das mithilfe von <a href="gg269243(v=exchg.10).md">jetsetls</a>festgelegt wurde.</p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvcontext</em>: <strong>null</strong></p></li>
<li><p><em>ulungenutzt</em>: <strong>null</strong></p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></td>
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
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)
