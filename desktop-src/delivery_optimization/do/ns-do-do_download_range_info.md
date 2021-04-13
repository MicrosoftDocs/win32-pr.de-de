---
title: DO_DOWNLOAD_RANGE_INFO Struktur
description: Gibt ein Array von Byte Bereichen an, das aus einer Datei heruntergeladen werden soll.
keywords:
- DO_DOWNLOAD_RANGE_INFO Struktur
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
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389648"
---
# <a name="do_download_range_info-structure"></a>DO_DOWNLOAD_RANGE_INFO Struktur

Die **DO_DOWNLOAD_RANGE_INFO** -Struktur identifiziert ein Array von Byte Bereichen, die aus einer Datei heruntergeladen werden sollen. Sie wird in der Regel als optionales Argument an die **idodownload:: Start** -Funktion übermittelt.

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

Array aus mindestens einer **DO_DOWNLOAD_RANGE** -Struktur, die die Bereiche angeben, die heruntergeladen werden sollen.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
