---
description: Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im sprintf-Stil.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Asyncstringtrace-Funktion
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
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358336"
---
# <a name="asyncstringtrace-function"></a>Asyncstringtrace-Funktion

Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im **sprintf**-Stil.

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

Ein 32-Bit-Ablauf Verfolgungs Parameter, der für die Filterung auf Anwendungsebene verwendet wird.

</dd> <dt>

*szformat* 
</dt> <dd>

Eine NULL terminierte Zeichenfolge, die das Format der Ablauf Verfolgung beschreibt.

</dd> <dt>

*setzen* 
</dt> <dd>

Ein Marker für **vsprintf** -Funktionen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die Länge der Ablauf Verfolgungs Anweisung in Bytes zurück.

## <a name="remarks"></a>Bemerkungen

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Beim Datentyp der **VA- \_ Liste** handelt es sich um einen Standardtyp, der für die von **VA \_ arg** und **VA \_** benötigten Informationen verwendet wird. Weitere Informationen finden Sie unter [Standard Typen](/cpp/c-runtime-library/standard-types?view=vs-2019).

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

