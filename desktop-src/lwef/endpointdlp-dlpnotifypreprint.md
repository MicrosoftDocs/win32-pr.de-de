---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Druckvorgang initiiert wird.
title: DlpNotifyPrePrint-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1cf0ef44031677495d9b9bedf990877ee931cae245b217faa4225b334df1b3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479441"
---
# <a name="dlpnotifypreprint-function"></a>DlpNotifyPrePrint-Funktion

Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Druckvorgang initiiert wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das zu druckende Dokument enthält.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) Struktur, die Informationen zum Druckvorgang enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |