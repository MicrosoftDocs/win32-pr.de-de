---
title: DO_DOWNLOAD_RANGE_INFO-Struktur
description: Identifiziert ein Array von Bytebereichen, die aus einer Datei heruntergeladen werden sollen.
keywords:
- DO_DOWNLOAD_RANGE_INFO-Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543744"
---
# <a name="do_download_range_info-structure"></a>DO_DOWNLOAD_RANGE_INFO-Struktur

Die **DO_DOWNLOAD_RANGE_INFO-Struktur** identifiziert ein Array von Bytebereichen, die aus einer Datei heruntergeladen werden sollen. Sie wird in der Regel als optionales Argument an die **IDODownload::Start-Funktion** übergeben.

## <a name="syntax"></a>Syntax
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Member

`RangeCount`

Anzahl der Elemente in Bereichen.

`Ranges`

Array von mindestens  einer DO_DOWNLOAD_RANGE-Strukturen, die die herunterzuladende Bereiche angeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
