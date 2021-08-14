---
description: 'Weitere Informationen zu: JET_CALLBACK Rückruffunktion'
title: JET_CALLBACK Rückruffunktion
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
ms.openlocfilehash: d50f0f3a0908b725d7f704df962324a0f16af1fc6f7353515a8d604e87edd0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487613"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK Rückruffunktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK Rückruffunktion

Die **JET_CALLBACK-Funktion** ist eine mehrzweckige Rückruffunktion, die von der Datenbank-Engine verwendet wird, um die Anwendung über ein Ereignis zu informieren, das Onlinedefragmentierung und Cursorzustandsbenachrichtigungen umfasst.

Informationen zu bestimmten Einstellungen, die für die Parameter dieser Funktion verwendet werden sollen, finden Sie unter [JET_CBTYP,](./jet-cbtyp.md) da sich diese Einstellungen je nach **JET_CBTYP** Option unterscheiden, die für die Verwendung im *cbtyp-Parameter* ausgewählt ist.

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

*sesid*

Die Sitzung, für die der Rückruf erfolgt.

*Dbid*

Die Datenbank, für die der Rückruf erfolgt.

*tableid*

Der Cursor, für den der Rückruf ausgeführt wird.

*cbtyp*

Der Punkt im Vorgang, an dem der Rückruf erfolgt. Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie jeweils eine Liste der Werte und die Bedeutung der folgenden Parameter.

*pvArg1*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des Rückrufs verwendet wird. Informationen zur Verwendung dieses Parameters für jeden rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP.](./jet-cbtyp.md)

*pvArg2*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des Rückrufs verwendet wird. Informationen zur Verwendung dieses Parameters für jeden rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP.](./jet-cbtyp.md)

*pvContext*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des Rückrufs verwendet wird. Informationen zur Verwendung dieses Parameters für jeden rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP.](./jet-cbtyp.md)

*ulUnused*

Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des Rückrufs verwendet wird. Informationen zur Verwendung dieses Parameters für jeden rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP.](./jet-cbtyp.md)

#### <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen der [Extensible Storage Engine-Fehlercodes](./extensible-storage-engine-error-codes.md)zurück. Informationen zum Zurückgeben dieser Codes als HRESULTs finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md). Bei Erfolg kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden. In einigen Fällen gibt der Rückruf möglicherweise eine Warnung zurück, die diesen Vorgang beeinflusst. Informationen zur Verwendung dieser Warnungen durch den Vorgang finden Sie unter [JET_CBTYP.](./jet-cbtyp.md)

Bei einem Fehler kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden oder fehlschlagen. Informationen zur Verwendung des Fehlercodes durch den Vorgang finden Sie unter [JET_CBTYP.](./jet-cbtyp.md)

#### <a name="remarks"></a>Hinweise

Wenn der Rückruf einen Cursor an die Anwendung übergibt, ist es wichtig zu wissen, dass dieser Cursor absichtlich auf einen kleineren Satz von Funktionen beschränkt ist, um Rekursion und andere Hässlichkeiten zu vermeiden. Die folgenden Vorgänge sind zulässig:

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCurrentIndex](./jetgetcurrentindex-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordPosition](./jetgetrecordposition-function.md)

  - [JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)

  - [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetRegisterCallback](./jetregistercallback-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUnregisterCallback](./jetunregistercallback-function.md)

Berücksichtigen Sie beim Entwerfen des Rückrufs, dass der Rückruf auch bei diesen Einschränkungen weiterhin fehlschlägt.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
