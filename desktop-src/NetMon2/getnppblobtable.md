---
description: Die GetNPPBlobTable-Funktion ruft eine NPP-BLOB-Tabelle ab, die die Register-NICs auf dem lokalen Computer darstellt.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: GetNPPBlobTable-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 49920df1be929eb9b35781aeabdcdf47167e82a94066e2d3237207dd00b08f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910700"
---
# <a name="getnppblobtable-function"></a>GetNPPBlobTable-Funktion

Die **GetNPPBlobTable-Funktion** ruft eine NPP-BLOB-Tabelle ab, die die Register-NICs auf dem lokalen Computer darstellt.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFilterBlob* \[ In\]
</dt> <dd>

Verarbeiten Sie ein Filterblob, das die in der Tabelle zurückgegebenen NPP-BLOBs einschränkt.

</dd> <dt>

*ppBlobTable* \[ out\]
</dt> <dd>

Zeiger auf eine [BLOB \_ TABLE-Struktur,](blob-table.md) die mindestens einen BLOB-Zeiger enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ KEINE \_ NPP-DLL \_**</dt> </dl>         | Im NPP-Verzeichnis wurden keine DLLs gefunden.<br/>                    |
| <dl> <dt>**NMERR \_ KEINE \_ GÜLTIGEN \_ NPP-DLLS \_**</dt> </dl> | Keine der DLLs im NPP-Verzeichnis waren gültige NPP-DLLs.<br/>  |
| <dl> <dt>**NMERR \_ KEINE \_ ÜBEREINSTIMMENDEN \_ NPPS**</dt> </dl>   | NPP-BLOBs wurden ermittelt, aber keiner hat den Filtertest bestanden.<br/> |
| <dl> <dt>**NMERR \_ OUT \_ OF \_ MEMOR**</dt> </dl>       | Netzwerkmonitor konnte keinen Speicher belegen.<br/>            |



 

## <a name="remarks"></a>Hinweise

Das BLOB mit dem Namen *hFilterBlob* kann auch ein spezielles BLOB sein.

Wenn Sie das Flag im Filterblob auf **TRUE** festlegen, kann die zurückgegebene BLOB-Tabelle auch spezielle BLOBs enthalten.

Wenn das BLOB mit dem Namen *hFilterBlob* ein spezielles BLOB ist, versucht die Netzwerkmonitor Benutzeroberfläche, es zu verarbeiten. Angenommen, ein vorheriger Aufruf gibt ein spezielles BLOB vom Remote-NPP zurück. Die Anwendung fügt das erforderliche Tag MACHINE \_ NAME ein. Der Finder übergibt dieses BLOB dann an das Remote-NPP, das dann eine Tabelle der NPP-BLOBs zurückgibt, die dem Computernamen zugeordnet sind.

Um alle zurückgegebenen BLOBs und die BLOB-Tabelle zu zerstören, ist der Aufrufer für den Aufruf der **DestroyBlob-Funktion** verantwortlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




