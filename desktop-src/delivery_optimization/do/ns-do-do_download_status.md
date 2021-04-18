---
title: DO_DOWNLOAD_STATUS Struktur
description: Dient zum Abrufen des Status eines bestimmten Downloads.
keywords:
- DO_DOWNLOAD_STATUS Struktur
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
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106338642"
---
# <a name="do_download_status-structure"></a>DO_DOWNLOAD_STATUS Struktur

Die **DO_DOWNLOAD_STATUS** Struktur wird verwendet, um den Status eines bestimmten Downloads abzurufen. Sie wird durch Aufrufen der **idodownload:: GetStatus** -Funktion abgerufen.

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

Die Gesamtzahl der herunter zuladenden bytes.

`BytesTransferred`

Die Anzahl von Bytes, die bereits heruntergeladen wurden.

`State`

Der aktuelle Download Zustand, wie von der **dodownloadstate** -Enumeration definiert.

`Error`

Die Fehlerinformationen (sofern vorhanden), die dem aktuellen Download zugeordnet sind.

`ExtendedError`

Die erweiterten Fehlerinformationen (sofern vorhanden), die dem aktuellen Download zugeordnet sind.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
