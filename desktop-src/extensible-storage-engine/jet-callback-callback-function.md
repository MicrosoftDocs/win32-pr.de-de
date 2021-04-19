---
description: 'Weitere Informationen über: JET_CALLBACK Callback-Funktion'
title: JET_CALLBACK Callback-Funktion
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348833"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK Callback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK Callback-Funktion

Die **JET_CALLBACK** -Funktion ist eine multizweck-Rückruffunktion, die von der Datenbank-Engine verwendet wird, um die Anwendung über ein Ereignis zu informieren, das Online Defragmentierung und Cursor Zustands Benachrichtigungen umfasst.

Informationen zu bestimmten Einstellungen, die für die Parameter dieser Funktion verwendet werden können, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) , da sich diese Einstellungen abhängig von der **JET_CBTYP** Option unterscheiden, die für die Verwendung im *cbyp* -Parameter ausgewählt ist.

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, für die der Rückruf erstellt wird.

*DBID*

Die Datenbank, für die der Rückruf erstellt wird.

*TableID*

Der Cursor, für den der Rückruf erstellt wird.

*cbyp*

Der Punkt in dem Vorgang, an dem der Rückruf durchgeführt wird. Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie eine Liste der Werte und die Bedeutung der folgenden Parameter in jedem Fall.

*pvArg1*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird. Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .

*pvArg2*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird. Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .

*pvcontext*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird. Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .

*ulungenutzt*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird. Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .

#### <a name="return-value"></a>Rückgabewert

Die-Funktion gibt einen der [Fehlercodes für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)zurück. Informationen dazu, wie diese Codes als HRESULTs zurückgegeben werden, finden Sie unter [Fehler bei Extensible Storage Engine](./extensible-storage-engine-errors.md). Bei Erfolg kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden. In einigen Fällen gibt der Rückruf möglicherweise eine Warnung zurück, die diesen Vorgang beeinflusst. Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie Informationen zur Verwendung dieser Warnungen durch den-Vorgang.

Bei einem Fehler wird der Vorgang, der den Rückruf ausgegeben hat, normalerweise ordnungsgemäß fortgesetzt oder schlägt fehl. Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie Informationen zur Verwendung des Fehlercodes durch den Vorgang.

#### <a name="remarks"></a>Bemerkungen

Wenn der Rückruf einen Cursor an die Anwendung übergibt, ist es wichtig zu wissen, dass dieser Cursor absichtlich auf einen kleineren Satz von Funktionen beschränkt ist, um Rekursion und andere Hässlichkeit zu vermeiden. Die folgenden Vorgänge sind zulässig:

  - [Jetdupcursor](./jetdupcursor-function.md)

  - [Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)

  - [Jetgetbookmark](./jetgetbookmark-function.md)

  - [Jetgetcurrentindex](./jetgetcurrentindex-function.md)

  - [Jetgetcursor Info](./jetgetcursorinfo-function.md)

  - [Jetgetls](./jetgetls-function.md)

  - [Jetgetrecordposition](./jetgetrecordposition-function.md)

  - [Jetgetsecondaryindexbookmark](./jetgetsecondaryindexbookmark-function.md)

  - [Jetgettablecolumninfo](./jetgettablecolumninfo-function.md)

  - [Jetgettableindexinfo](./jetgettableindexinfo-function.md)

  - [Jetgettableinfo](./jetgettableinfo-function.md)

  - [Jetregistercallback](./jetregistercallback-function.md)

  - [Jetretrievecolumschlag](./jetretrievecolumn-function.md)

  - [Jetretrievecolumschlag](./jetretrievecolumns-function.md)

  - [Jetretrievekey](./jetretrievekey-function.md)

  - [Jetsetcolumn](./jetsetcolumn-function.md)

  - [Jetsetcolumns](./jetsetcolumns-function.md)

  - [Jetsetls](./jetsetls-function.md)

  - [Jetunregistercallback](./jetunregistercallback-function.md)

Berücksichtigen Sie beim Entwerfen Ihres Rückrufs, dass auch mit diesen Einschränkungen das Fehlschlagen des Rückrufs möglich ist.

#### <a name="requirements"></a>Anforderungen

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
