---
description: Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Vorgang zugeordnet ist.
title: DLP_DOCUMENT_INFO -Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495782"
---
# <a name="dlp_document_info-structure"></a>DLP_DOCUMENT_INFO Struktur

Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Vorgang zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Members

<dl> <dt>

*Version* \[ In\]
</dt> <dd>

Ein DWORD, das die API-Version an gibt. Dieser Wert sollte immer **DLP_DOCUMENT_INFO_V_LATEST.** Diese Konstante wird in der Auflistung der Endpointdlp.h-Beispielheaderdatei im Artikel [Endpoint data loss prevention definiert.](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der den ursprünglichen Pfad des Dokuments an gibt.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der den Pfad zur tatsächlichen Hintergrunddatei des Dokuments an gibt.

</dd> </dl>



## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

