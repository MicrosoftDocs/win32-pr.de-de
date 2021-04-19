---
description: Erstellt ein Delta zwischen der angegebenen Quelldatei und der angegebenen Zieldatei.
title: Funktion "featepatchfileexa/W"
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355268"
---
# <a name="createpatchfileexaw-function"></a>Funktion "featepatchfileexa/W"

Die Funktionen " **epatepatchfileexa** " und " **upatepatchfileexw** " erstellen ein Delta zwischen der angegebenen Quelldatei und der angegebenen Zieldatei. Sowohl die Quell-als auch die Zieldateien werden als Pfade bereitgestellt. Das Ausgabe Delta wird auch in einen bereitgestellten Pfad geschrieben. Diese Funktionen stellen während des Erstellungs Vorgangs Statusberichte bereit.

## <a name="syntax"></a>Syntax

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>Parameter

*Oldfilecount*

Die Gesamtanzahl der Quelldateien. Wird verwendet, um Delta-Dateien für mehrere Quelldateien (maximal 255) zu erstellen.

*Oldfileingefoarray*

Ein Zeiger auf das Quelldatei Informations Array.

*NewFileName*

Der Name der Zieldatei.

*Patchdateiname*

Der Name des Deltas, das erstellt wird.

*Optionflags*

Erstellungsflags.

*ProgressCallback*

Zeiger auf einen Anwendungs definierten Fortschritts Rückruf.

*CallbackContext*

Zeiger auf einen Anwendungs definierten Kontext.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | PatchAPI. h |
| DLL | mspatchc.dll |
| Unicode | Implementiert als "kreatepatchfileexw (Unicode)" und "kreatepatchfileexa" (ANSI) |

## <a name="see-also"></a>Siehe auch

[PatchAPI](patchapi.md)
