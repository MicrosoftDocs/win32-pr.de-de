---
description: Extrahiert die Headerinformationen aus einem Delta.
title: ExtractPatchHeaderToFileA/W-Funktion
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571800"
---
# <a name="extractpatchheadertofileaw-function"></a>ExtractPatchHeaderToFileA/W-Funktion

Die Funktionen **ExtractPatchHeaderToFileA** und **ExtractPatchHeaderToFileW** extrahieren die Headerinformationen aus einem Delta. Das Delta wird als Dateipfad bereitgestellt. Der Ausgabeheader wird auch in einen angegebenen Pfad geschrieben.

## <a name="syntax"></a>Syntax

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>Parameter

*PatchFileName*

Der Name des Deltas, das den Header enthält.

*PatchHeaderFileName*

Der Name der Headerdatei, die erstellt werden soll.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sie erfolgreich ist. Andernfalls wird **FALSE** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | patchapi.h |
| DLL | mspatchc.dll |
| Unicode | Implementiert als ExtractPatchHeaderToFileW (Unicode) und ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Siehe auch

[PatchAPI](patchapi.md)
