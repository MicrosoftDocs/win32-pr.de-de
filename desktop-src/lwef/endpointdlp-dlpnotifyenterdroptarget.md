---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel eingegeben wird.
title: DlpNotifyEnterDropTarget-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 42ac6939f42cd79463a0fe7d76a200f4aa1a206005375fbbf54835b49f0b1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976640"
---
# <a name="dlpnotifyenterdroptarget-function"></a>DlpNotifyEnterDropTarget-Funktion

Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel eingegeben wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das dokument enthält, das dem Abbruchvorgang zugeordnet ist.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |