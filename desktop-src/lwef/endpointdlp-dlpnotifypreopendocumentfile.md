---
description: Stellt dem System Informationen zu einer Dokumentdatei zur Verfügung, bevor ein Geöffnet-Vorgang initiiert wird.
title: DlpNotifyPreOpenDocumentFile-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 12caf5230d8affce195a63da155ed6b6ca409b72
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495630"
---
# <a name="dlpnotifypreopendocumentfile-function"></a>DlpNotifyPreOpenDocumentFile-Funktion

Stellt dem System Informationen zu einer Dokumentdatei zur Verfügung, bevor ein Geöffnet-Vorgang initiiert wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das zu öffnende Dokument enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |