---
description: Dieses Thema gilt für Windows XP Service Pack 2 oder höher. Die kstopology \_ -Verbindungs Struktur beschreibt eine Knoten Verbindung innerhalb eines Kernel Streaming-Filters (KS). Ein Knoten kann mit einem anderen Knoten innerhalb des Filters oder mit einer PIN im Filter verbunden werden.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION Struktur (". h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371224"
---
# <a name="kstopology_connection-structure"></a>Kstopology- \_ Verbindungs Struktur

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Die **kstopology- \_ Verbindungs** Struktur beschreibt eine Knoten Verbindung innerhalb eines Kernel Streaming-Filters (KS). Ein Knoten kann mit einem anderen Knoten innerhalb des Filters oder mit einer PIN im Filter verbunden werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>Member

<dl> <dt>

**Fromnode**
</dt> <dd>

Index des Upstream-Knotens in der Verbindung. Wenn die Upstreamverbindung anstelle eines Knotens eine PIN ist, ist der Wert der ksfilter- \_ Knoten.

</dd> <dt>

**Fromnodepin**
</dt> <dd>

Wenn der Wert des Felds **fromnode** ein ksfilter- \_ Knoten ist, gibt dieses Feld den Index der upstreampin an. Andernfalls wird dieses Feld ignoriert.

</dd> <dt>

**ToNode**
</dt> <dd>

Index des Downstream-Knotens in der Verbindung. Wenn die Downstreamverbindung anstelle eines Knotens eine PIN ist, lautet der Wert ksfilter- \_ Knoten.

</dd> <dt>

**Tonodepin**
</dt> <dd>

Wenn der Wert des **ToNode** -Felds der ksfilter- \_ Knoten ist, gibt dieses Feld den Index des Downstream-Pins an. Andernfalls wird dieses Feld ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>. H.</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[**"IKsTopologyInfo:: get \_ ConnectionInfo"**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




