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
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085798"
---
# <a name="asyncstringtrace-function"></a>AsyncStringTrace-Funktion

Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen. 

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

Eine mit 0 (null) beendete Zeichenfolge, die das Format der Ablaufverfolgung beschreibt.

</dd> <dt>

*Marker* 
</dt> <dd>

Ein Marker für **vsprintf-Funktionen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die Länge der Ablaufverfolgungs-Anweisung in Bytes zurück.

## <a name="remarks"></a>Bemerkungen

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Der **datentyp va \_ list** ist ein Standardtyp, der zum Enthalten von Informationen verwendet wird, die von **va \_ arg-** und **\_ va-End-Makros benötigt** werden. Weitere Informationen finden Sie unter [Standardtypen.](/cpp/c-runtime-library/standard-types?view=vs-2019)

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

