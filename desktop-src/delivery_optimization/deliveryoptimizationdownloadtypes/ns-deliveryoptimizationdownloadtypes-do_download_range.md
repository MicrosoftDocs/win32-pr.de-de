---
title: DO_DOWNLOAD_RANGE Struktur
description: Identifiziert einen einzelnen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.
keywords:
- DO_DOWNLOAD_RANGE Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106341698"
---
# <a name="do_download_range-structure"></a>DO_DOWNLOAD_RANGE Struktur

Die **DO_DOWNLOAD_RANGE** -Struktur identifiziert einen einzelnen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll. Die **DO_DOWNLOAD_RANGE** Struktur ist in **DO_DOWNLOAD_RANGES_INFO** Struktur enthalten, um ein Array von Bereichen zum Herunterladen bereitzustellen.

## <a name="syntax"></a>Syntax
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Member

`Offset`

NULL basierter Offset am Anfang des Bereichs von Bytes, der aus einer Datei heruntergeladen werden soll.

`Length`

Die Länge des Bereichs in Bytes. Geben Sie keine Länge von 0 Byte an. Um anzugeben, dass der Bereich bis zum Ende der Datei reicht, geben Sie **DO_LENGTH_TO_EOF** an.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Deliveryoptimizationdownloadtypes. h |
