---
description: Legt den BLOB-ETYPE/SAP-Filter fest.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Setnppeer Type esapfilter-Funktion (Netmon. h)
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
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344959"
---
# <a name="setnppetypesapfilter-function"></a>Setnppeer Type esapfilter-Funktion

Die **setnppeer Type esapfilter** -Funktion legt den BLOB-ETYPE/SAP-Filter fest.

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

*hblob* \[ in\]
</dt> <dd>

Ein Handle für das BLOB.

</dd> <dt>

*NSAPs* \[ in\]
</dt> <dd>

Die Anzahl der SAPS.

</dd> <dt>

" *ntypes* \[ " in\]
</dt> <dd>

Die Anzahl der ETYPEs in der ETYPE-Tabelle, die festgelegt wird.

</dd> <dt>

*lpsaptable* \[ in\]
</dt> <dd>

Ein Zeiger auf die festgelegte SAP-Tabelle.

</dd> <dt>

*lpeer typetable* \[ in\]
</dt> <dd>

Ein Zeiger auf die ETYPE-Tabelle, die festgelegt wird.

</dd> <dt>

*Filterflags* \[ in\]
</dt> <dd>

Die Filterflags, die festgelegt werden.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Das Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (sofern vorhanden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

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

[Getnpettypesapfilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




