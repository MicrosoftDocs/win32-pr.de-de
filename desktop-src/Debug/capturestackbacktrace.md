---
UID: ''
title: CaptureStackBackTrace-Funktion
description: Erfasst eine Stapelrückverfolgung, indem der Stapel nach oben geleitet wird.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279501"
---
# <a name="capturestackbacktrace-function"></a>CaptureStackBackTrace-Funktion

## <a name="description"></a>BESCHREIBUNG

Erfasst eine Stapelrückverfolgung, indem der Stapel hochläuft und die Informationen für jeden Frame aufgezeichnet werden.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Parameter

### <a name="framestoskip-in"></a>FramesToSkip [in]

Die Anzahl der Frames, die ab dem Anfang der Rückverfolgung übersprungen werden sollen.

### <a name="framestocapture-in"></a>FramesToCapture [in]

Die Anzahl der zu erfassenden Frames.
Sie können bis zu **MAXUSHORT-Frames** erfassen.

**Windows Server 2003 und Windows XP:**  Die Summe der *FramesToSkip-* und *FramesToCapture-Parameter* muss kleiner als 63 sein.

### <a name="backtrace-out"></a>BackTrace [out]

Ein Array von Zeigern, die aus der aktuellen Stapelüberwachung erfasst werden.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, optional]

Ein -Wert, der zum Organisieren von Hashtabellen verwendet werden kann.
Wenn dieser Parameter **NULL** ist, wird kein Hashwert berechnet.

Dieser Wert wird basierend auf den Werten der Zeiger berechnet, die im BackTrace-Array zurückgegeben werden.
Zwei identische Stapelüberwachungen generieren identische Hashwerte.

## <a name="returns"></a>Gibt zurück

Die Anzahl der erfassten Frames.

## <a name="remarks"></a>Hinweise

Die **CaptureStackBackTrace-Funktion** ist als **die RtlCaptureStackBackTrace-Funktion** definiert (die Definition ist ab Windows Vista im Windows SDK enthalten).
Weitere Informationen finden Sie unter WinBase.h und WinNT.h.

## <a name="see-also"></a>Weitere Informationen
