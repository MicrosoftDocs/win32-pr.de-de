---
description: Legt den BLOB-Etype/Sap-Filter fest.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: SetNPPEtypeSapFilter-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 30b2f6ffbefad955034f520162b6fdc44d80198d926f35443ce21fefd80ef5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363826"
---
# <a name="setnppetypesapfilter-function"></a>SetNPPEtypeSapFilter-Funktion

Die **SetNPPEtypeSapFilter-Funktion** legt den BLOB-Etype/Sap-Filter fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hBlob* \[ In\]
</dt> <dd>

Ein Handle für das BLOB.

</dd> <dt>

*nSaps* \[ In\]
</dt> <dd>

Die Anzahl der SAPs.

</dd> <dt>

*nEtypes* \[ In\]
</dt> <dd>

Die Anzahl der Etypes in der Etype-Tabelle, die festgelegt wird.

</dd> <dt>

*lpSapTable* \[ In\]
</dt> <dd>

Ein Zeiger auf die SAP-Tabelle, die festgelegt ist.

</dd> <dt>

*lpEtypeTable* \[ In\]
</dt> <dd>

Ein Zeiger auf die Etype-Tabelle, die festgelegt ist.

</dd> <dt>

*FilterFlags* \[ In\]
</dt> <dd>

Die festgelegten Filterflags.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Das Handle für ein Fehlerblob, das angibt, wo im ursprünglichen BLOB der Fehler aufgetreten ist (sofern ein Fehler aufgetreten ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




