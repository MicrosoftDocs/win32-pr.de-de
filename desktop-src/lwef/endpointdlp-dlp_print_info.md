---
description: Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Druckvorgang zugeordnet ist.
title: DLP_PRINT_INFO -Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495781"
---
# <a name="dlp_print_info-structure"></a>DLP_PRINT_INFO-Struktur

Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Druckvorgang zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>Members

<dl> <dt>

*Version* \[ In\]
</dt> <dd>

Ein DWORD, das die API-Version an gibt. Dieser Wert sollte immer **DLP_PRINT_INFO_V_LATEST.** Diese Konstante wird in der Auflistung der Endpointdlp.h-Beispielheaderdatei im Artikel [Endpoint data loss prevention definiert.](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*PrinterName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der den Zieldrucker identifiziert.

</dd> </dl>

<dl> <dt>

*JobName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der den Namen des Druckauftrags an gibt.

</dd> </dl>

<dl> <dt>

*OutputFileName* \[ In\]
</dt> <dd>

Ein LPCWSTR, der beim Drucken in eine Datei den Pfad zur Ausgabedatei an gibt.

</dd> </dl>



## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

