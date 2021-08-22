---
description: Committet neu erstellte Indizes in die angegebene Datenbank.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: SdbCommitIndexes-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1c133b55456dec402e54c3bcd24b7e84c81752d467be5cf7872896deaafdf424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571340"
---
# <a name="sdbcommitindexes-function"></a>SdbCommitIndexes-Funktion

Committet neu erstellte Indizes in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ in, out\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE** bei Erfolg oder **FALSE** bei Einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




