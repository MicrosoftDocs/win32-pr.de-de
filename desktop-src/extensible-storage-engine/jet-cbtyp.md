---
description: 'Weitere Informationen finden Sie unter: JET_CBTYP'
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
ms.openlocfilehash: fa797fac58b0a2663c918e7fef739c6c5ab536dcfa9dc91be13b8196aed5ef43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945910"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**Gilt für:** Windows | Windows Server_

## <a name="jet_cbtyp"></a>JET_CBTYP

Die **JET_CBTYP** Gruppe von Konstanten beschreibt alle möglichen Punkte in einem Vorgang, dass [](./jet-callback-callback-function.md) die Datenbank-Engine eine Anwendung benachrichtigt, indem sie die JET_CALLBACK aufruft. Die Datenbank-Engine übergibt eine dieser Konstanten im *cbtyp-Parameter* der Rückruffunktion. Die Bedeutung der anderen Parameter, die von der Datenbank-Engine in diesem Aufruf übergeben werden, hängt von der jeweiligen **übergebenen JET_CBTYP** ab.

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
<td><p>Dieser Rückruf ist reserviert und gilt immer als ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Dieser Rückruf ist für die zukünftige Verwendung reserviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Dieser Rückruf erfolgt direkt vor dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder <a href="gg294146(v=exchg.10).md">mithilfe</a> von JET_TABLECREATE an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben oder zur Laufzeit mit <a href="gg269175(v=exchg.10).md">jetRegisterCallback konfiguriert.</a> Weitere Informationen finden Sie <a href="gg294146(v=exchg.10).md">unter</a> JET_TABLECREATE <a href="gg269175(v=exchg.10).md">oder JetRegisterCallback</a>.</p>
<p>Die Rückrufparameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung mit dem datensatz, der eingefügt werden soll.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den zu einfügenden Datensatz enthält.</p></li>
<li><p><em>tableid:</em>Der Cursor, der das Einfügen des neuen Datensatzes vorbereitet hat. Es ist wichtig zu beachten, dass der Wert von Versions- oder Automatischinkrementspalten zu diesem Zeitpunkt möglicherweise nicht korrekt ist.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>Der Kontextzeiger, der an <a href="gg269175(v=exchg.10).md">JetRegisterCallback oder</a> <strong>NULL übergeben wird.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong> Wenn ein Fehler vom Rückruf zurückgegeben wird, tritt bei dem Vorgang, der den Rückruf verursacht, ein Fehler auf.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Dieser Rückruf erfolgt direkt nach dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">JetUpdate,</a> aber bevor <a href="gg269288(v=exchg.10).md">JetUpdate</a> zum Aufrufer zurückkehrt.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder <a href="gg294146(v=exchg.10).md">mithilfe</a> von JET_TABLECREATE an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben oder zur Laufzeit mit <a href="gg269175(v=exchg.10).md">jetRegisterCallback konfiguriert.</a> Weitere Informationen finden Sie <a href="gg294146(v=exchg.10).md">unter</a> JET_TABLECREATE <a href="gg269175(v=exchg.10).md">oder JetRegisterCallback</a>.</p>
<p>Die Rückrufparameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung mit dem Datensatz, der gerade eingefügt wurde.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den datensatz enthält, der gerade eingefügt wurde.</p></li>
<li><p><em>tableid:</em>Ein Cursor auf der Tabelle, in die der Datensatz eingefügt wurde. Beachten Sie, dass der Cursor weiterhin auf demselben Indexeintrag positioniert ist, wie er sich im Voreinfügerückrufenen befindet. Beachten Sie außerdem, dass dieser Indexeintrag in irgendeiner Weise mit dem eingefügten Datensatz verknüpft sein kann.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>Der Kontextzeiger, der an <a href="gg269175(v=exchg.10).md">JetRegisterCallback oder</a> <strong>NULL übergeben wird.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong> Wenn ein Fehler vom Rückruf zurückgegeben wird, wird er ignoriert.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Dieser Rückruf erfolgt direkt vor einem vorhandenen Datensatz in einer Tabelle, der durch einen Aufruf von <a href="gg269288(v=exchg.10).md">JetUpdate geändert wird.</a></p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder <a href="gg294146(v=exchg.10).md">mithilfe</a> von JET_TABLECREATE an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben oder zur Laufzeit mit <a href="gg269175(v=exchg.10).md">jetRegisterCallback konfiguriert.</a> Weitere Informationen finden Sie <a href="gg294146(v=exchg.10).md">unter</a> JET_TABLECREATE <a href="gg269175(v=exchg.10).md">oder JetRegisterCallback</a>.</p>
<p>Die Rückrufparameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung mit dem zu ändernden Datensatz.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den zu ändernden Datensatz enthält.</p></li>
<li><p><em>tableid:</em>Ein Cursor, der auf einem Indexeintrag positioniert ist, der dem zu ändernden Datensatz zugeordnet ist. Es ist wichtig zu beachten, dass der Wert von Versions- oder Automatischinkrementspalten zu diesem Zeitpunkt möglicherweise nicht korrekt ist.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>Der Kontextzeiger, der an <a href="gg269175(v=exchg.10).md">JetRegisterCallback oder</a> <strong>NULL übergeben wird.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong> Wenn ein Fehler vom Rückruf zurückgegeben wird, tritt bei dem Vorgang, der den Rückruf verursacht, ein Fehler auf.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Dieser Rückruf erfolgt direkt, nachdem ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">JetUpdate</a> geändert wurde, aber bevor <a href="gg269288(v=exchg.10).md">JetUpdate</a> zum Aufrufer zurückkehrt.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder <a href="gg294146(v=exchg.10).md">mithilfe</a> von JET_TABLECREATE an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben oder zur Laufzeit mit <a href="gg269175(v=exchg.10).md">jetRegisterCallback konfiguriert.</a> Weitere Informationen finden Sie <a href="gg294146(v=exchg.10).md">unter</a> JET_TABLECREATE <a href="gg269175(v=exchg.10).md">oder JetRegisterCallback</a>.</p>
<p>Die Rückrufparameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung mit dem Datensatz, der gerade geändert wurde.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den soeben geänderten Datensatz enthält.</p></li>
<li><p><em>tableid:</em>Ein Cursor, der auf einem Indexeintrag positioniert ist, der dem soeben geänderten Datensatz zugeordnet ist.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>Der Kontextzeiger, der an <a href="gg269175(v=exchg.10).md">JetRegisterCallback oder</a> <strong>NULL übergeben wird.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong> Wenn ein Fehler vom Rückruf zurückgegeben wird, wird er ignoriert.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Dieser Rückruf erfolgt, kurz bevor ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269315(v=exchg.10).md">JetDelete gelöscht wird.</a></p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder <a href="gg294146(v=exchg.10).md">mithilfe</a> von JET_TABLECREATE an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben oder zur Laufzeit mit <a href="gg269175(v=exchg.10).md">jetRegisterCallback konfiguriert.</a> Weitere Informationen finden Sie <a href="gg294146(v=exchg.10).md">unter</a> JET_TABLECREATE <a href="gg269175(v=exchg.10).md">oder JetRegisterCallback</a>.</p>
<p>Die Rückrufparameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung mit dem zu löschenden Datensatz.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den zu löschenden Datensatz enthält.</p></li>
<li><p><em>tableid:</em>Ein Cursor, der auf einem Indexeintrag positioniert ist, der dem zu löschenden Datensatz zugeordnet ist.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>Der Kontextzeiger, der an <a href="gg269175(v=exchg.10).md">JetRegisterCallback oder</a> <strong>NULL übergeben wird.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong> Wenn ein Fehler vom Rückruf zurückgegeben wird, tritt bei dem Vorgang, der den Rückruf verursacht, ein Fehler auf.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Dieser Rückruf erfolgt direkt, nachdem ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269315(v=exchg.10).md">JetDelete</a> gelöscht wurde, aber bevor <a href="gg269315(v=exchg.10).md">JetDelete</a> an den Aufrufer zurückkehrt.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder <a href="gg294146(v=exchg.10).md">mithilfe</a> von JET_TABLECREATE an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben oder zur Laufzeit mit <a href="gg269175(v=exchg.10).md">jetRegisterCallback konfiguriert.</a> Weitere Informationen finden Sie <a href="gg294146(v=exchg.10).md">unter</a> JET_TABLECREATE <a href="gg269175(v=exchg.10).md">oder JetRegisterCallback</a>.</p>
<p>Die Rückrufparameter verfügen über die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung mit dem Datensatz, der gerade gelöscht wurde.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den soeben gelöschten Datensatz enthält.</p></li>
<li><p><em>tableid:</em>Ein Cursor, der auf einem Indexeintrag positioniert ist, der dem soeben gelöschten Datensatz zugeordnet ist.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>Der Kontextzeiger, der an <a href="gg269175(v=exchg.10).md">JetRegisterCallback oder</a> <strong>NULL übergeben wird.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong></p></li>
</ul>
<p>Wenn ein Fehler vom Rückruf zurückgegeben wird, wird er ignoriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die Engine den benutzerdefinierten Standardwert einer Spalte aus der Anwendung abrufen muss. Dieser Rückruf ist im Wesentlichen eine eingeschränkte Implementierung von <a href="gg269198(v=exchg.10).md">JetRetrieveColumn,</a> die von der Anwendung ausgewertet wird. Maximal ein Spaltenwert kann für einen benutzerdefinierten Standardwert zurückgegeben werden.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird entweder mithilfe einer <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT-Struktur</a> an <a href="gg294122(v=exchg.10).md">JetAddColumn</a> oder mithilfe einer <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT-Struktur</a> in einer <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE-Struktur</a> in einer <a href="gg294146(v=exchg.10).md">JET_TABLECREATE-Struktur</a> an <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> übergeben.</p>
<p>Die Rückrufparameter haben die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung, die den benutzerdefinierten Standardwert berechnen soll.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Tabelle, die den benutzerdefinierten Standardwert enthält.</p></li>
<li><p><em>tableid:</em>Ein Cursor, der auf dem Datensatz positioniert ist, für den der benutzerdefinierte Standardwert abgerufen wird.</p></li>
<li><p><em>pvArg1:</em>Der Ausgabepuffer für den benutzerdefinierten Standardwert.</p></li>
<li><p><em>pvArg2:</em>Bei eingabe ist dies die Größe des Ausgabepuffers. Bei der Ausgabe ist dies die tatsächliche Größe des benutzerdefinierten Standardwerts. in beiden Fällen ist die Größe eine 32-Bit-Ganzzahl ohne Vorzeichen.</p></li>
<li><p><em>pvContext:</em>Ein Zeiger auf einen Puffer, der die in der <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> -Struktur angegebenen Benutzerdaten enthält, als die Spalte erstellt wurde, oder NULL, wenn kein Kontext bereitgestellt wurde.</p></li>
<li><p><em>ulUnused:</em>Die Spalten-ID der Spalte, für die der benutzerdefinierte Standardwert abgerufen wird.</p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang, von dem der Rückruf stammt, mit diesem Fehler fehl.</p>
<p>Wenn JET_wrnBufferTruncated vom Rückruf zurückgegeben wird, wird der Vorgang fortgesetzt, aber der gesamte Wert wird während des Rückrufs nicht abgerufen.</p>
<p>Wenn JET_wrnColumnNull vom Rückruf zurückgegeben wird, wird der Vorgang fortgesetzt, aber der benutzerdefinierte Standardwert für die Spalte ist NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die online von <a href="gg269317(v=exchg.10).md">JetDefragment</a> initiierte Onlinedefragmentierung einer Datenbank beendet wurde, weil entweder der Prozess abgeschlossen oder das Zeitlimit erreicht wurde.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird an <a href="gg269317(v=exchg.10).md">JetDefragment</a>übergeben. Weitere Informationen finden Sie unter <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</p>
<p>Die Rückrufparameter haben die folgenden Werte:</p>
<ul>
<li><p><em>sesid:</em>Die Sitzung, die zum Ausführen der Onlinedefragmentierung für die Datenbank oder JET_sesidNil für eine Streamingdatei verwendet wird.</p></li>
<li><p><em>dbid:</em>Die Datenbank-ID der Datenbank, die defragmentiert oder für eine Streamingdatei JET_dbidNil wird.</p></li>
<li><p><em>tableid:</em>JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: <strong>NULL</strong></p></li>
<li><p><em>pvArg2</em>: <strong>NULL</strong></p></li>
<li><p><em>pvContext</em>: <strong>NULL</strong></p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong></p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Dieser Rückruf tritt auf, wenn die Anwendung das Kontexthandle für die lokale Storage bereinigen muss, die einem Cursor zugeordnet ist, der von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> mit <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>konfiguriert.</p>
<p>Die Rückrufparameter haben die folgenden Werte:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>tableid:</em>JET_tableidNil</p></li>
<li><p><em>pvArg1:</em>Das Kontexthandle, das mit <a href="gg269243(v=exchg.10).md">JetSetLS</a> festgelegt wurde</p></li>
<li><p><em>pvArg2</em>: <strong>NULL</strong></p></li>
<li><p><em>pvContext</em>: <strong>NULL</strong></p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong></p></li>
</ul>
<p>Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Dieser Rückruf tritt auf, weil die Anwendung das Kontexthandle für die lokale Storage bereinigen muss, die einer Tabelle zugeordnet ist, die von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>Der Funktionszeiger für diesen Rückrufgrund wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> mit <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>konfiguriert.</p>
<p>Die Rückrufparameter haben die folgenden Werte:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>tableid:</em>JET_tableidNil</p></li>
<li><p><em>pvArg1:</em>Das Kontexthandle, das mit <a href="gg269243(v=exchg.10).md">JetSetLS</a>festgelegt wird.</p></li>
<li><p><em>pvArg2</em>: <strong>NULL</strong></p></li>
<li><p><em>pvContext</em>: <strong>NULL</strong></p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong></p></li>
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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)
