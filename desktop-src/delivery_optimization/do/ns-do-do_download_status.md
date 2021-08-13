---
title: DO_DOWNLOAD_STATUS-Struktur
description: Wird verwendet, um den Status eines bestimmten Downloads abzurufen.
keywords:
- DO_DOWNLOAD_STATUS-Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8775b7daf55d58698d00bcaa2820b909e302933c9f407d1cb6416d6b095a872b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543734"
---
# <a name="do_download_status-structure"></a>DO_DOWNLOAD_STATUS-Struktur

Die **DO_DOWNLOAD_STATUS-Struktur** wird verwendet, um den Status eines bestimmten Downloads abzurufen. Sie wird durch Aufrufen der **IDODownload::GetStatus-Funktion** abgerufen.

## <a name="syntax"></a>Syntax
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>Member

`BytesTotal`

Die Gesamtzahl der herunterzuladende Bytes.

`BytesTransferred`

Die Anzahl der Bytes, die bereits heruntergeladen wurden.

`State`

Der aktuelle Downloadstatus, wie durch die **DODownloadState-Enumeration** definiert.

`Error`

Die Fehlerinformationen (sofern vorhanden), die dem aktuellen Download zugeordnet sind.

`ExtendedError`

Die erweiterten Fehlerinformationen (sofern vorhanden), die dem aktuellen Download zugeordnet sind.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
