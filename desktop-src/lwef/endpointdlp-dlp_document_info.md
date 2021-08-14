---
description: Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Vorgang zugeordnet ist.
title: DLP_DOCUMENT_INFO-Struktur (endpointdlp.h)
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
ms.openlocfilehash: 8aa4b6c961b4e80786e9ada480949245b032750499b38f0deead44f97a2d88fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479763"
---
# <a name="dlp_document_info-structure"></a>DLP_DOCUMENT_INFO-Struktur

Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Vorgang zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Member

<dl> <dt>

*Version* \[ In\]
</dt> <dd>

Ein DWORD, das die API-Version angibt. Dieser Wert sollte immer **DLP_DOCUMENT_INFO_V_LATEST** sein. Diese Konstante wird in der Beispielheaderdatei endpointdlp.h im Artikel Endpoint data loss prevention (Verhindern von [Endpunktdatenverlust)](endpointdlp-endpoint-data-loss-prevention.md)definiert.

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der den ursprünglichen Pfad des Dokuments angibt.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der den Pfad zur tatsächlichen Sicherungsdatei des Dokuments angibt.

</dd> </dl>



## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

