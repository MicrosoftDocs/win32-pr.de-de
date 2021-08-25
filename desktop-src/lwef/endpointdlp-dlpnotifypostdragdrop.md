---
description: Stellt dem System Nach Abschluss eines Drag & Drop-Vorgangs Informationen zu einem Dokument zur Verfügung.
title: DlpNotifyPostDragDrop-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 3d20f9356007973b580d136aef1a74b8206026bf62fe14c5db46eb2cc0cbf1f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062110"
---
# <a name="dlpnotifypostdragdrop-function"></a>DlpNotifyPostDragDrop-Funktion

Stellt dem System Nach Abschluss eines Drag & Drop-Vorgangs Informationen zu einem Dokument zur Verfügung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DocumentInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, das dem Drag Drop-Vorgang zugeordnet ist.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ In\]
</dt> <dd>

A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drag drop.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt void zurück.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |