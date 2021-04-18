---
description: Extrahiert die Header Informationen aus einem Delta.
title: Extractpatchheaderabflea/W-Funktion
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
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357666"
---
# <a name="extractpatchheadertofileaw-function"></a>Extractpatchheaderabflea/W-Funktion

Die Funktionen **extractpatchheaderdefilea** und **extractpatchheaderdefilew** extrahieren die Header Informationen aus einem Delta. Das Delta wird als Dateipfad bereitgestellt. Der Ausgabe Header wird auch in einen bereitgestellten Pfad geschrieben.

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

*Patchdateiname*

Der Name des Deltas, das den Header enthält.

*Patchheaderfilename*

Der Name der Header Datei, die erstellt werden soll.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | PatchAPI. h |
| DLL | mspatchc.dll |
| Unicode | Implementiert als extractpatchheaderpatfilew (Unicode) und extractpatchheaderumfilea (ANSI) |

## <a name="see-also"></a>Siehe auch

[PatchAPI](patchapi.md)
