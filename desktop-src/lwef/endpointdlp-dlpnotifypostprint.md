---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang abgeschlossen wurde.
title: DlpNotifyPostPrint-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495661"
---
# <a name="dlpnotifypostprint-function"></a>DlpNotifyPostPrint-Funktion

Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das dokument enthält, das dem Druckvorgang zugeordnet ist.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) Struktur, die Informationen zum Druckvorgang enthält.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

Ein Zeiger auf [](enpointdlp-dlp_postop_status.md) eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Druckvorgang enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |