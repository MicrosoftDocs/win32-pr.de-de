---
description: Deklariert einen neuen Index in der angegebenen Datenbank.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Sdbdeclareingedex-Funktion
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
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343181"
---
# <a name="sdbdeclareindex-function"></a>Sdbdeclareingedex-Funktion

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

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*TDas* \[ in\]
</dt> <dd>

Dieser Parameter muss eine **\_ Tagtyp \_ Liste** sein.

</dd> <dt>

*TKey* \[ in\]
</dt> <dd>

Das-Tag, das den Typ angibt, der als Schlüssel verwendet werden soll. Dieser Parameter kann keine **\_ Tagtyp \_ Liste** sein.

</dd> <dt>

*dwentries* \[ in\]
</dt> <dd>

Die Anzahl der Einträge, die im Index zuzuordnen sind.

</dd> <dt>

*buniquekey* \[ in\]
</dt> <dd>

Wenn dieser Parameter **true** ist, ist der Index ein Index mit einem eindeutigen Schlüssel.

</dd> <dt>

*piiindex* \[ vorgenommen\]
</dt> <dd>

Die resultierende **IndexID** des neu deklarierten Indexes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird aufgerufen, bevor Tags in den neuen Index geschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INDEXID**](indexid.md)
</dt> <dt>

[**Sdbcommitindexes**](sdbcommitindexes.md)
</dt> <dt>

[**Sdbstartindizierung**](sdbstartindexing.md)
</dt> <dt>

[**Sdbstopindizierung**](sdbstopindexing.md)
</dt> </dl>

 

 




