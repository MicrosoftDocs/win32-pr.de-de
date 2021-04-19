---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.
title: DlpNotifyPostPasteFromClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495662"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a>DlpNotifyPostPasteFromClipboard-Funktion

Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, in das der Inhalt kopiert wurde.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

Ein Zeiger auf [](enpointdlp-dlp_postop_status.md) eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Einfügen aus der Zwischenablage enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |