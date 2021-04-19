---
description: Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im sprintf-Stil.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Setasynctraceparamsex-Funktion
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
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354110"
---
# <a name="setasynctraceparamsex-function"></a>Setasynctraceparamsex-Funktion

Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im **sprintf**-Stil.

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

*pszmodule* 
</dt> <dd>

Der Name des Moduls, das der Ablauf Verfolgung zugeordnet ist.

</dd> <dt>

*pszFile* 
</dt> <dd>

Der Name der Quelldatei, die die Ausnahme enthält.

</dd> <dt>

*Lline* 
</dt> <dd>

Die Zeilennummer der Ausnahme in der Quelldatei.

</dd> <dt>

*pszfunction* 
</dt> <dd>

Der Funktionsname der Ausnahme.

</dd> <dt>

*dwtracemask* 
</dt> <dd>

Eine Ablaufverfolgungsflag-Konstante, die einen der verfügbaren Ablauf Verfolgungs Typen darstellt. Dieser Parameter kann einen der folgenden Werte aufweisen.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>Schwerwiegend **\_ Ablauf Verfolgungs \_ Maske** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Fehler \_ Ablauf Verfolgungs \_ Maske** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Debuggen \_ Ablauf Verfolgungs \_ Maske** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Status \_ Ablauf Verfolgungs \_ Maske** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**Funct \_ Ablauf Verfolgungs \_ Maske** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Nachricht \_ Ablauf Verfolgungs \_ Maske** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Alle \_ Ablauf Verfolgungs \_ Maske** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt 1 zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird 0 zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
