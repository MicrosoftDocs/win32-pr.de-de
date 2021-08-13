---
title: RoFailFastWithErrorContextInternal2-Funktion
description: Löst eine nicht kontinuierbare Ausnahme im aktuellen Prozess aus und ermöglicht ihnen auch das Aufnehmen zusätzlicher Fehlerkontexte, die nicht bereits vom Betriebssystem erfasst wurden.
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
ms.openlocfilehash: a2e8e2e357b7c4768596ca36cb48cdf1bb2cfdbd839ecc6949a607975d6000c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560626"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>RoFailFastWithErrorContextInternal2-Funktion

Löst eine nicht kontinuierbare Ausnahme im aktuellen Prozess aus und ermöglicht es Ihnen auch, zusätzlichen Fehlerkontext ein include, der nicht bereits vom Betriebssystem erfasst wurde.

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

Das **HRESULT,** das dem aktuellen Fehler zugeordnet ist. Die Ausnahme wird für jeden Wert von *hrError ausgelöst.*

`cStowedExceptions`

Typ: **[ULONG](../../winprog/windows-data-types.md)**

Die Anzahl der Elemente im *Array aStowedExceptionPointers.*

`aStowedExceptionPointers`

Typ: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Ein Array von Zeigern auf [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) Strukturen. Jede -Struktur enthält Informationen, die eine stowed-Ausnahme beschreiben. Die Informationen in diesen Strukturen werden dann an Windows-Fehlerberichterstattung (WER) zusammen mit den stowed-Ausnahmeinformationen übermittelt, die von der Plattform erfasst wurden.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**RoFailFastWithErrorContextInternal2** ist weder einer Importbibliothek noch einer Headerdatei zugeordnet. Sie können sie aufrufen, indem Sie zuerst die [**LoadLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (zum Laden) und dann die GetProcAddress-Funktion aufrufen, um die Adresse von `ComBase.dll` **RoFailFastWithErrorContextInternal2 abzurufen.** [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Weitere Informationen finden Sie unter [RoFailFastWithErrorContext-Funktion](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | Nicht zutreffend |
| **Bibliothek** | Nicht zutreffend |
| **Dll** | ComBase.dll |

## <a name="see-also"></a>Weitere Informationen:

* [RoFailFastWithErrorContext-Funktion](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)