---
description: Die GetNPPEtypeSapFilter-Funktion ruft den Etype/Sap-Filter aus einem bestimmten BLOB ab.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: GetNPPEtypeSapFilter-Funktion (Netmon.h)
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
ms.openlocfilehash: 593030c3b53e7e11b20b9fe1497a3989b2ff68650d3d2df73f52e6491529d58e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982304"
---
# <a name="getnppetypesapfilter-function"></a>GetNPPEtypeSapFilter-Funktion

Die **GetNPPEtypeSapFilter-Funktion** ruft den Etype/Sap-Filter aus einem bestimmten BLOB ab.

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

*hBlob* \[ In\]
</dt> <dd>

Handle für das BLOB.

</dd> <dt>

*pnSaps* \[ out\]
</dt> <dd>

Zeiger auf die zurückgegebene Anzahl von Protokollen in der SAP-Tabelle.

</dd> <dt>

*pnEtypes* \[ out\]
</dt> <dd>

Zeiger auf die zurückgegebene Anzahl von Etypes in der Etype-Tabelle.

</dd> <dt>

*ppSapTable* \[ out\]
</dt> <dd>

Zeiger auf die zurückgegebene SAP-Tabelle.

</dd> <dt>

*ppEtypeTable* \[ out\]
</dt> <dd>

Zeiger auf die zurückgegebene Etype-Tabelle.

</dd> <dt>

*pFilterFlags* \[ out\]
</dt> <dd>

Zeiger auf die zurückgegebenen Filterflags.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Behandeln sie ein Fehler-BLOB, das den Speicherort im ursprünglichen BLOB angibt, an dem der Fehler aufgetreten ist (falls vorhanden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler angibt.

## <a name="remarks"></a>Hinweise

Die Etype/Sap-Informationen werden in der Kategorie **Config** des NPP-Abschnitts **Besitzer** gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




