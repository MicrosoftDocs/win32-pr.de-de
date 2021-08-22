---
description: Stellt dem System Informationen zu einem Dokument bereit, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.
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
ms.openlocfilehash: b964d7beb5e4418f09d5e5710aa5a9245be9c118c4d8fe821368876c8e58d73e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976540"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a>DlpNotifyPreCopyToClipboard-Funktion

Stellt dem System Informationen zu einem Dokument bereit, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das Dokument enthält, aus dem Inhalt kopiert wird.

</dd> </dl>




## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |