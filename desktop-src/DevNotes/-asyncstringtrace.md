---
description: 'AsyncStringTrace-Funktion: Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: ac099b0b69c1417c428aefe04b8e6591f945545a2b69196da588ebce8de23f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076174"
---
# <a name="asyncstringtrace-function"></a>AsyncStringTrace-Funktion

Schließt das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für sprintf-style-Ablaufverfolgungen ab. 

## <a name="syntax"></a>Syntax


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein 32-Bit-Ablaufverfolgungsparameter, der für die Filterung auf Anwendungsebene verwendet wird.

</dd> <dt>

*szFormat* 
</dt> <dd>

Eine auf null endende Zeichenfolge, die das Format der Ablaufverfolgung beschreibt.

</dd> <dt>

*Marker* 
</dt> <dd>

Ein Marker für **vsprintf-Funktionen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die Länge der Ablaufverfolgungs-Anweisung in Bytes zurück.

## <a name="remarks"></a>Hinweise

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Der **Datentyp va \_ list** ist ein Standardtyp, der zum Speichern von Informationen verwendet wird, die von **va \_ arg-** und **va \_ end-Makros** benötigt werden. Weitere Informationen finden Sie unter [Standardtypen.](/cpp/c-runtime-library/standard-types?view=vs-2019)

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

