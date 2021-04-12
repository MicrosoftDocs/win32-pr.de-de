---
description: 'Weitere Informationen über: JET_PFNSTATUS Callback-Funktion'
title: JET_PFNSTATUS Callback-Funktion
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217057"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS Callback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS Callback-Funktion

Die **JET_PFNSTATUS** Callback-Funktion empfängt Informationen zum Fortschritt von Vorgängen mit langer Ausführungszeit, z. b. Defragmentierungs-, Sicherungs-oder Wiederherstellungs Vorgänge. Bei solchen Vorgängen Ruft die Datenbank-Engine diese Rückruffunktion auf, um ein Update für den Fortschritt des Vorgangs zu erhalten.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung vom Typ [JET_SESID](./jet-sesid.md) , mit der die Funktion mit langer Ausführungszeit aufgerufen wurde.

*SNP*

Der Typ des Vorgangs, wie in [JET_SNP](./jet-snp.md)angegeben. Zu den Vorgangs Typen zählen Reparatur, Compact, Restore, Backup, Update, scrube und Update des Daten Satz Formats.

*SNT*

Der Status eines Vorgangs. Zu den Status Typen zählen Anfang, in Bearbeitung, Abschluss oder Fehler. Der Status wird mit dem dritten Parameter des Typs [JET_SNT](./jet-snt.md)angegeben.

*teuren*

Ein optionaler Zeiger auf eine Struktur vom Typ [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der [Fehlercodes für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

Bei Erfolg kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden. In einigen Fällen gibt der Rückruf möglicherweise eine Warnung zurück, die diesen Vorgang beeinflusst.

Bei einem Fehler wird der Vorgang, der den Rückruf ausgegeben hat, normalerweise ordnungsgemäß fortgesetzt oder schlägt fehl.

### <a name="remarks"></a>Bemerkungen

Diese Rückruffunktion wird in einer Status Benachrichtigung verwendet, in der die Struktur den aktuellen Status des Fortschritts angibt. Beachten Sie, dass die Rückruffunktion möglicherweise mehrmals für den Fortschritt des Vorgangs aufgerufen wird.

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

[Fehlercodes für erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)  
[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
