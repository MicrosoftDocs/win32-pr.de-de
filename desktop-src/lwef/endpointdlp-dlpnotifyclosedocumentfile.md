---
description: Stellt dem System Informationen zu einem Dokument bereit, bevor der Vorgang zum Schließen der Dokumentdatei initiiert wird.
title: DlpNotifyCloseDocumentFile-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: fc4aff982ebfa8e16f4a7d2c0cd42a847825b422af761416d4a410a03df66446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062140"
---
# <a name="dlpnotifyclosedocumentfile-function"></a>DlpNotifyCloseDocumentFile-Funktion

Stellt dem System Informationen zu einem Dokument bereit, bevor der Vorgang zum Schließen der Dokumentdatei initiiert wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
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