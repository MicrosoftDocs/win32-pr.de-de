---
description: 'Weitere Informationen zu: JET_PFNSTATUS Rückruffunktion'
title: JET_PFNSTATUS Rückruffunktion
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
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482916"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS Rückruffunktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS Rückruffunktion

Die **JET_PFNSTATUS** Rückruffunktion empfängt Informationen über den Fortschritt von Vorgängen mit langer Ausführungszeit, z. B. Defragmentierungs-, Sicherungs- oder Wiederherstellungsvorgänge. Während solcher Vorgänge ruft die Datenbank-Engine diese Rückruffunktion auf, um ein Update des Vorgangsfortschritts durchzuführen.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung vom Typ [JET_SESID,](./jet-sesid.md) mit der die Langlauffunktion aufgerufen wurde.

*Snp*

Der In [JET_SNP](./jet-snp.md)angegebene Vorgangstyp. Zu den Arten von Vorgängen gehören Reparatur, Kompakt, Wiederherstellung, Sicherung, Update, Bereinigung und Aktualisierung des Datensatzformats.

*Snt*

Der Status eines Vorgangs. Zu den Statustypen gehören "Start", "In Bearbeitung", "Abschluss" oder "Fehler". Der Status wird mit dem dritten Parameter vom Typ [JET_SNT](./jet-snt.md)angegeben.

*Pv*

Ein optionaler Zeiger auf eine Struktur vom Typ [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der [Extensible Storage Engine-Fehlercodes](./extensible-storage-engine-error-codes.md)zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

Bei Erfolg kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden. In einigen Fällen gibt der Rückruf möglicherweise eine Warnung zurück, die diesen Vorgang beeinflusst.

Bei einem Fehler kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden oder fehlschlagen.

### <a name="remarks"></a>Hinweise

Diese Rückruffunktion wird in einer Statusbenachrichtigung verwendet, in der die Struktur den aktuellen Status des Fortschritts angibt. Beachten Sie, dass die Rückruffunktion für den Fortschritt des Vorgangs möglicherweise mehrmals aufgerufen wird.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage Engine-Fehlercodes](./extensible-storage-engine-error-codes.md)  
[Erweiterbare Storage-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
