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
ms.openlocfilehash: 23caba53e754c54bfd717274b5f889ad224a2dc80fbe54fb97f70125c0c74f23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976580"
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

Ein Zeiger [](endpointdlp-dlp_print_info.md) auf eine DLP_PRINT_INFO-Struktur, die Informationen zum Druckvorgang enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |