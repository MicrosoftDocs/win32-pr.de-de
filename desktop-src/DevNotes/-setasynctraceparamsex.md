---
description: 'SetAsyncTraceParamsEx-Funktion: Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen.'
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 6c41369e8a0d73a56dc5d9d831d0028e87a7ecec300f2e43a625f17bd25bede1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538865"
---
# <a name="setasynctraceparamsex-function"></a>SetAsyncTraceParamsEx-Funktion

Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen. 

## <a name="syntax"></a>Syntax


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszModule* 
</dt> <dd>

Der Name des Moduls, das der Ablaufverfolgung zugeordnet ist.

</dd> <dt>

*pszFile* 
</dt> <dd>

Der Name der Quelldatei, die die Ausnahme enthält.

</dd> <dt>

*lLine* 
</dt> <dd>

Die Zeilennummer der Ausnahme in der Quelldatei.

</dd> <dt>

*pszFunction* 
</dt> <dd>

Der Funktionsname der Ausnahme.

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

Eine Ablaufverfolgungsflag-Konstante, die einen der verfügbaren Ablaufverfolgungstypen darstellt. Dieser Parameter kann einen der folgenden Werte enthalten.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**SCHWERWIEGENDER FEHLER \_ TRACE \_ MASK** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**FEHLER \_ TRACE \_ MASK** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUGGEN \_ TRACE \_ MASK** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE \_ TRACE \_ MASK** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_ TRACE \_ MASK** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE \_ TRACE \_ MASK** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL \_ TRACE \_ MASK** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt 1 zurück, wenn die Funktion erfolgreich ist. Andernfalls wird 0 zurückgegeben.

## <a name="remarks"></a>Hinweise

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
