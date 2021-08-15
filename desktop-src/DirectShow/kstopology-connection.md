---
description: Dieses Thema gilt für Windows XP Service Pack 2 oder höher. Die KSTOPOLOGY \_ CONNECTION-Struktur beschreibt eine Knotenverbindung innerhalb eines Kernelstreamingfilters (KS). Ein Knoten kann mit einem anderen Knoten innerhalb des Filters oder mit einer Stecknadel im Filter verbunden werden.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION -Struktur (Ks.h)
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
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397244"
---
# <a name="kstopology_connection-structure"></a>KSTOPOLOGY \_ CONNECTION-Struktur

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Die **KSTOPOLOGY \_ CONNECTION-Struktur** beschreibt eine Knotenverbindung innerhalb eines Kernelstreamingfilters (KS). Ein Knoten kann mit einem anderen Knoten innerhalb des Filters oder mit einer Stecknadel im Filter verbunden werden.

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

**FromNode**
</dt> <dd>

Index des Upstreamknotens in der Verbindung. Wenn die Upstreamverbindung ein Pin und kein Knoten ist, ist der Wert KSFILTER \_ NODE.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Wenn der Wert des **FromNode-Felds** KSFILTER NODE ist, gibt dieses Feld den Index \_ des Upstreampins an. Andernfalls wird dieses Feld ignoriert.

</dd> <dt>

**ToNode**
</dt> <dd>

Index des Downstreamknotens in der Verbindung. Wenn die Downstreamverbindung ein Pin und kein Knoten ist, ist der Wert KSFILTER \_ NODE.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Wenn der Wert des **Felds ToNode** KSFILTER NODE ist, gibt dieses Feld den Index \_ des Downstreampins an. Andernfalls wird dieses Feld ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo::get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




