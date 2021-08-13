---
title: DO_DOWNLOAD_RANGE-Struktur
description: Identifiziert einen einzelnen Bytebereich, der aus einer Datei heruntergeladen werden soll.
keywords:
- DO_DOWNLOAD_RANGE-Struktur
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
ms.openlocfilehash: 39672bff2e3a7194f7d674b2184d5de8c9c3c601e4a7777ef31ace80f5f9f327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047118"
---
# <a name="do_download_range-structure"></a>DO_DOWNLOAD_RANGE-Struktur

Die **DO_DOWNLOAD_RANGE-Struktur** identifiziert einen einzelnen Bytebereich, der aus einer Datei heruntergeladen werden soll. Die **DO_DOWNLOAD_RANGE-Struktur** ist in **DO_DOWNLOAD_RANGES_INFO** -Struktur enthalten, um ein Array von Bereichen zum Herunterladen bereitzustellen.

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

Nullbasierter Offset bis zum Anfang des Bytebereichs, der aus einer Datei heruntergeladen werden soll.

`Length`

Die Länge des Bereichs in Bytes. Geben Sie keine Länge von 0 Byte an. Um anzugeben, dass sich der Bereich bis zum Ende der Datei erstreckt, geben Sie **DO_LENGTH_TO_EOF** an.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
