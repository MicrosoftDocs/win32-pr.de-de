---
description: Erstellt ein Delta zwischen der angegebenen Quelldatei und der angegebenen Zieldatei.
title: CreatePatchFileExA/W-Funktion
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
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690870"
---
# <a name="createpatchfileexaw-function"></a>CreatePatchFileExA/W-Funktion

Die Funktionen **CreatePatchFileExA** und **CreatePatchFileExW** erstellen ein Delta zwischen der angegebenen Quelldatei und der angegebenen Zieldatei. Sowohl die Quell- als auch die Zieldateien werden als Pfade bereitgestellt. Das Ausgabedelta wird auch in einen angegebenen Pfad geschrieben. Diese Funktionen stellen während des Erstellungsprozesses Statusberichte bereit.

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

*OldFileCount*

Die Gesamtzahl der Quelldateien. Wird verwendet, um Deltas für mehrere Quelldateien zu erstellen (maximal 255).

*OldFileInfoArray*

Zeiger auf das Informationsarray der Quelldatei.

*NewFileName*

Der Name der Zieldatei.

*PatchFileName*

Der Name des Deltas, das erstellt wird.

*OptionFlags*

Erstellungsflags.

*ProgressCallback*

Zeiger auf den anwendungsdefinierte Statusrückruf.

*CallbackContext*

Zeiger auf anwendungsdefinierte Kontexte.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sie erfolgreich ist. Andernfalls wird **FALSE** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | patchapi.h |
| DLL | mspatchc.dll |
| Unicode | Implementiert als CreatePatchFileExW (Unicode) und CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Siehe auch

[PatchAPI](patchapi.md)
