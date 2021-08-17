---
description: Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Kopiervorgang in die Zwischenablage abgeschlossen wurde.
title: DlpNotifyPostCopyToClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: afd054aa0728f3eeb70a5ecbbdeab88460deee2146aa10000665eb56f8d76b65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751849"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a>DlpNotifyPostCopyToClipboard-Funktion

Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Kopiervorgang in die Zwischenablage abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das Dokument enthält, aus dem Inhalt kopiert wurde.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

Ein Zeiger [](enpointdlp-dlp_postop_status.md) auf eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Kopiervorgang in die Zwischenablage enthält.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |