---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Vorgang zum Speichern unter abgeschlossen wurde.
title: DlpNotifyPostSaveAsDocument-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495654"
---
# <a name="dlpnotifypostsaveasdocument-function"></a>DlpNotifyPostSaveAsDocument-Funktion

Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Vorgang zum Speichern unter abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das gespeicherte Dokument enthält.

</dd> </dl>

<dl> <dt>

*Ziel* \[ In\]
</dt> <dd>

Ein **LPCWSTR mit** dem Zielpfad des gespeicherten Dokuments.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

Ein Zeiger auf [](enpointdlp-dlp_postop_status.md) eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Save as-Vorgang enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |