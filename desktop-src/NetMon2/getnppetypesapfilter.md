---
description: Die getnppeer Type esapfilter-Funktion Ruft den ETYPE/SAP-Filter aus einem angegebenen BLOB ab.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Getnppeer Type esapfilter-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351170"
---
# <a name="getnppetypesapfilter-function"></a>Getnppeer Type esapfilter-Funktion

Die **getnppeer Type esapfilter** -Funktion Ruft den ETYPE/SAP-Filter aus einem angegebenen BLOB ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für das BLOB.

</dd> <dt>

*pnsaps* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die zurückgegebene Anzahl von Protokollen in der SAP-Tabelle.

</dd> <dt>

*pnettypes* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die zurückgegebene Anzahl von ETYPEs in der ETYPE-Tabelle.

</dd> <dt>

*ppsaptable* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die zurückgegebene SAP-Tabelle.

</dd> <dt>

*ppeer typetable* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die zurückgegebene ETYPE-Tabelle.

</dd> <dt>

*pfilterflags* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die zurückgegebenen Filterflags.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Handle für einen fehlerblob, der den Speicherort im ursprünglichen BLOB angibt, an dem der Fehler (falls vorhanden) aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Die ETYPE/SAP-Informationen werden in der Kategorie **config** des Abschnitts NPP- **Besitzer** gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Setnppeer Type esapfilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




