---
description: Stellt dem System Informationen zu einer Dokumentdatei bereit, nachdem der Vorgang zum Öffnen abgeschlossen wurde.
title: DlpNotifyPostOpenDocumentFile-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2957b09282fe64e41805f09a1761ca75aa3551ca70e9d4aa5b52517374fd9ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976600"
---
# <a name="dlpnotifypostopendocumentfile-function"></a>DlpNotifyPostOpenDocumentFile-Funktion

Stellt dem System Informationen zu einer Dokumentdatei bereit, nachdem ein Vorgang zum Öffnen abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger [](endpointdlp-dlp_document_info.md) auf eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das geöffnete Dokument enthält.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

Ein Zeiger [](enpointdlp-dlp_postop_status.md) auf eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Vorgang des geöffneten Dokuments enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |