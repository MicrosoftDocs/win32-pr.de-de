---
description: Erstellt ein Delta zwischen Quelle und Ziel (als Puffer bereitgestellt) und gibt das Ausgabedelta als von MSDelta zugeordneten Puffer zurück.
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
ms.openlocfilehash: ae13dfb82d4699bbb8cc222b4cd1aaa2615e8efaa578de60483f00552faf2086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826924"
---
# <a name="createdeltab-function"></a>CreateDeltaB-Funktion

Erstellt ein Delta zwischen Quelle und Ziel (als Puffer bereitgestellt) und gibt das Ausgabedelta als von MSDelta zugeordneten Puffer zurück.

> [!NOTE]
> Sie müssen [DeltaFree](msdelta-deltafree.md) aufrufen, um den Ausgabepuffer freizugeben, nachdem diese Funktion abgeschlossen wurde.

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

*FileTypeSet*

[in] Der [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) Wert, der den dateityp angibt, der für den Erstellungsprozess verwendet werden soll.

*SetFlags*

[in] Ein oder [](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) mehrere DELTA_FLAG_TYPE-Werte, die zusätzlich zu den Standardflags die während des Erstellungsprozesses zu verwendenden Flags angeben.

*ResetFlags*

[in] Ein oder [](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) mehrere DELTA_FLAG_TYPE-Werte, die die Standardflags angeben, die während des Erstellungsprozesses zurückgesetzt werden sollen.

*Quelle*

[in] Eine [](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) DELTA_INPUT-Struktur, die einen Zeiger auf den Puffer enthält, der die Quelldaten enthält.

*Target*

[in] Eine [](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) DELTA_INPUT-Struktur, die einen Zeiger auf den Puffer enthält, der die Zieldaten enthält.

*SourceOptions*

[in]: Reserviert Übergeben Sie eine [DELTA_INPUT-Struktur,](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) wobei *Editable* auf **FALSE,** *lpStart* auf **NULL** und *uSize* auf 0 festgelegt ist.

*TargetOptions*

[in]: Reserviert Übergeben Sie eine [DELTA_INPUT-Struktur,](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) wobei *Editable* auf **FALSE,** *lpStart* auf **NULL** und *uSize* auf 0 festgelegt ist.

*GlobalOptions*

[in]: Reserviert Übergeben Sie eine [DELTA_INPUT-Struktur,](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) bei der *lpStart* auf **NULL** und *uSize* auf 0 festgelegt ist.

*lpTargetFileTime*

[in] Der Zeitstempel, der für die Zieldatei festgelegt ist, nachdem das Delta angewendet wurde. Bei **NULL** ist der Zielzeitstempel die aktuelle Zeit während des Erstellungsprozesses.

*HashAlgId*

[in] ALG_ID des Algorithmus, der zum Generieren der Zielsignatur verwendet werden soll. Einige besondere Werte sind:

- 0 = Keine Signatur
- 32 = in msdelta.dll definierte 32-Bit-CRC

*lpDelta*

[out] Zeiger auf die [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) Struktur, in die das Delta geschrieben werden soll.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sie erfolgreich ist. Andernfalls wird **FALSE** zurückgegeben. Wenn die Funktion **FALSE** zurückgibt, können Sie [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um den entsprechenden Win32-Systemfehlercode abzurufen.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | msdelta.h |
| DLL | msdelta.dll |
| Unicode | Nicht zutreffend |

## <a name="see-also"></a>Siehe auch

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
