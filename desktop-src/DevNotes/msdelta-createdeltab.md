---
description: Erstellt ein Delta zwischen Quelle und Ziel (bereitgestellt als Puffer) und gibt das Ausgabe Delta als in Msdelta zugewiesener Puffer zurück.
title: CreateDeltaB-Funktion
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357526"
---
# <a name="createdeltab-function"></a>CreateDeltaB-Funktion

Erstellt ein Delta zwischen Quelle und Ziel (bereitgestellt als Puffer) und gibt das Ausgabe Delta als in Msdelta zugewiesener Puffer zurück.

> [!NOTE]
> Sie müssen [Delta Free](msdelta-deltafree.md) anrufen, um den Ausgabepuffer freizugeben, nachdem diese Funktion abgeschlossen wurde.

## <a name="syntax"></a>Syntax

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Parameter

*Filetypeset*

in Der [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) -Wert, der den Dateityp angibt, der für den Erstellungs Prozess verwendet werden soll.

*SetFlags*

in Mindestens ein [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) -Wert, der die Flags angibt, die während des Erstellungs Prozesses verwendet werden sollen, zusätzlich zu den Standardflags.

*Resetflags*

in Mindestens ein [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) -Wert, der die Standardflags angibt, die während des Erstellungs Vorgangs zurückgesetzt werden sollen.

*Quelle*

in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Quelldaten enthält.

*Target*

in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Zieldaten enthält.

*Sourceoptions*

[in]: Reserviert Übergeben Sie eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur, bei der *editable* auf **false** festgelegt ist, *lpstart* auf **null** und *usize* auf 0 festgelegt ist.

*Targetoptions*

[in]: Reserviert Übergeben Sie eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur, bei der *editable* auf **false** festgelegt ist, *lpstart* auf **null** und *usize* auf 0 festgelegt ist.

*GlobalOptions*

[in]: Reserviert Übergeben Sie eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur, wobei *lpstart* auf **null** und *usize* auf 0 festgelegt ist.

*lptargetfiletime*

in Der Zeitstempel, der für die Zieldatei festgelegt ist, nachdem Delta angewendet wurde. Wenn der Wert **null** ist, wird der Ziel Zeitstempel die aktuelle Zeit während des Erstellungs Prozesses sein.

*HashAlgId*

in ALG_ID des Algorithmus, der zum Generieren der Ziel Signatur verwendet werden soll. Einige besondere Werte sind:

- 0 = keine Signatur
- 32 = 32-Bit CRC in msdelta.dll definiert

*lpdelta*

vorgenommen Ein Zeiger auf die [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) Struktur, in die das Delta geschrieben werden soll.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben. Wenn die Funktion " **false**" zurückgibt, können Sie " [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " aufrufen, um den entsprechenden Win32-Systemfehler Code zu erhalten.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | Msdelta. h |
| DLL | msdelta.dll |
| Unicode | Nicht verfügbar |

## <a name="see-also"></a>Siehe auch

[Msdelta](msdelta.md)

[Delta frei](msdelta-deltafree.md)
