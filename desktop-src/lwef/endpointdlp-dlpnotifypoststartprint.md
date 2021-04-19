---
description: Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Druckvorgang gestartet wurde.
title: DlpNotifyPostStartPrint-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495653"
---
# <a name="dlpnotifypoststartprint-function"></a>DlpNotifyPostStartPrint-Funktion

Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Druckvorgang gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das Dokument enthält, das dem Druckvorgang zugeordnet ist.

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