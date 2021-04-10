---
description: Führt einen Commit für neu erstellte Indizes zur angegebenen Datenbank aus.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Sdbcommitindexes-Funktion
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
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126170"
---
# <a name="sdbcommitindexes-function"></a>Sdbcommitindexes-Funktion

Führt einen Commit für neu erstellte Indizes zur angegebenen Datenbank aus.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in, out\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbdeclareingedex**](sdbdeclareindex.md)
</dt> <dt>

[**Sdbstartindizierung**](sdbstartindexing.md)
</dt> <dt>

[**Sdbstopindizierung**](sdbstopindexing.md)
</dt> </dl>

 

 




