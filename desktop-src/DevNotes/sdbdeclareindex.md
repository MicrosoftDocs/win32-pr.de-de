---
description: Deklariert einen neuen Index in der angegebenen Datenbank.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: b428699641d5a18bad8a1869f59ab1bb5402e7b667526070c3dc0575e435fc38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666589"
---
# <a name="sdbdeclareindex-function"></a>SdbDeclareIndex-Funktion

Deklariert einen neuen Index in der angegebenen Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tWhich* \[ In\]
</dt> <dd>

Dieser Parameter muss **TAG \_ TYPE LIST \_ sein.**

</dd> <dt>

*tKey* \[ In\]
</dt> <dd>

Das TAG, das den Typ angibt, der als Schlüssel verwendet werden soll. Dieser Parameter darf nicht **TAG \_ TYPE LIST \_ sein.**

</dd> <dt>

*dwEntries* \[ In\]
</dt> <dd>

Die Anzahl der Einträge, die im Index zuteilen sind.

</dd> <dt>

*bUniqueKey* \[ In\]
</dt> <dd>

Wenn dieser Parameter **TRUE ist,** ist der Index ein eindeutiger Schlüsselindex.

</dd> <dt>

*piiIndex* \[ out\]
</dt> <dd>

Die resultierende **INDEXID** des neu deklarierten Indexes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE bei** Erfolg oder **FALSE bei** Einem Fehler zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Funktion auf, bevor Sie Tags in den neuen Index schreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INDEXID**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




