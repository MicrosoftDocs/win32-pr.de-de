---
UID: ''
title: Capturestackbacktrace-Funktion
description: Erfasst eine Stapel Rückverfolgung, indem der Stapel nach oben durchlaufen wird.
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
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "106341286"
---
# <a name="capturestackbacktrace-function"></a>Capturestackbacktrace-Funktion

## <a name="description"></a>BESCHREIBUNG

Erfasst eine Stapel Rückverfolgung, indem der Stapel nach oben durchlaufen und die Informationen für die einzelnen Frames aufgezeichnet werden.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Parameter

### <a name="framestoskip-in"></a>Framestoskip [in]

Die Anzahl der Rahmen, die vom Anfang der Rückverfolgung ausgelassen werden sollen.

### <a name="framestocapture-in"></a>Framestocapture [in]

Die Anzahl der zu erfassenden Frames.
Sie können bis zu **maxushort** -Frames erfassen.

**Windows Server 2003 und Windows XP:**  Die Summe der Parameter " *framestoskip* " und " *framestocapture* " muss kleiner als 63 sein.

### <a name="backtrace-out"></a>Rückverfolgung [out]

Ein Array von Zeigern, die von der aktuellen Stapel Überwachung aufgezeichnet wurden.

### <a name="backtracehash-out-optional"></a>Backtracehash [out, optional]

Ein Wert, der zum Organisieren von Hash Tabellen verwendet werden kann.
Wenn dieser Parameter **null** ist, wird kein Hashwert berechnet.

Dieser Wert wird basierend auf den Werten der Zeiger berechnet, die im Backtrace-Array zurückgegeben werden.
Zwei identische Stapel Überwachungen generieren identische Hashwerte.

## <a name="returns"></a>Gibt zurück

Die Anzahl der aufgezeichneten Frames.

## <a name="remarks"></a>Bemerkungen

Die **capturestackbacktrace** -Funktion ist als **rtlcapturestackbacktrace** -Funktion definiert (die Definition ist in der Windows SDK ab Windows Vista enthalten).
Weitere Informationen finden Sie unter Winbase. h und WinNT. h.

## <a name="see-also"></a>Siehe auch
