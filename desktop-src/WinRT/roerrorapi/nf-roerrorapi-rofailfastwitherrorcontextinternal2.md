---
title: RoFailFastWithErrorContextInternal2-Funktion
description: Löst im aktuellen Prozess eine nicht fort Setz Bare Ausnahme aus und ermöglicht es Ihnen außerdem, zusätzlichen Fehler Kontext einzuschließen, der noch nicht vom Betriebssystem erfasst wurde.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106338301"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>RoFailFastWithErrorContextInternal2-Funktion

Löst im aktuellen Prozess eine nicht fort Setz Bare Ausnahme aus und ermöglicht es Ihnen außerdem, zusätzlichen Fehler Kontext einzuschließen, der nicht bereits vom Betriebssystem erfasst wurde.

## <a name="syntax"></a>Syntax

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>Parameter

`hrError`

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Das **HRESULT** , das dem aktuellen Fehler zugeordnet ist. Die Ausnahme wird für jeden Wert von " *hrError*" ausgelöst.

`cStowedExceptions`

Typ: **[ulong](../../winprog/windows-data-types.md)**

Die Anzahl der Elemente im " *astowedexceptionpointer* "-Array.

`aStowedExceptionPointers`

Typ: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Ein Array von Zeigern auf [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) Strukturen. Jede Struktur enthält Informationen, in denen eine verstaute Ausnahme beschrieben wird. Die Informationen in diesen Strukturen werden dann an Windows-Fehlerberichterstattung (wer) zusammen mit den Informationen über die gestaut-Ausnahme gesendet, die von der Plattform aufgezeichnet wurden.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

**RoFailFastWithErrorContextInternal2** ist nicht mit einer Import Bibliothek und einer Header Datei verknüpft. Sie können ihn zuerst mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) -Funktion (Laden `ComBase.dll` ) und dann durch Aufrufen der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen, um die Adresse von **RoFailFastWithErrorContextInternal2** abzurufen.

Weitere Informationen finden Sie unter [rofailfastwitherrorcontext-Funktion](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | – |
| **Bibliothek** | – |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>Siehe auch

* [Rofailfastwitherrorcontext-Funktion](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)