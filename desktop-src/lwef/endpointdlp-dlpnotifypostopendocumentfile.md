---
description: Stellt dem System Informationen zu einer Dokumentdatei zur Verfügung, nachdem der Vorgang zum Öffnen abgeschlossen wurde.
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
ms.openlocfilehash: 0aed30cc0eca066b569ad1299392430c4d1adeff
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495686"
---
# <a name="dlpnotifypostopendocumentfile-function"></a>DlpNotifyPostOpenDocumentFile-Funktion

Stellt dem System Informationen zu einer Dokumentdatei zur Verfügung, nachdem ein Geöffnet-Vorgang abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das geöffnete Dokument enthält.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) Struktur, die Statusinformationen über den Vorgang zum Öffnen eines Dokuments enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |