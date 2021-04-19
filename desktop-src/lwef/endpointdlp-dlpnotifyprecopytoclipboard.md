---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.
title: DlpNotifyPreCopyToClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495645"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a>DlpNotifyPreCopyToClipboard-Funktion

Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, aus dem Inhalt kopiert wird.

</dd> </dl>




## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |