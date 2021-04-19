---
title: Asfleakybucketpair
description: Das asfleakybucketpair-Attribut ist ein optionales Attribut, das die Puffer Anforderungen für eine Variable-Bitrate-Datei beschreibt.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Asfleakybucketpairs Windows Media-Format
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342097"
---
# <a name="asfleakybucketpairs"></a>Asfleakybucketpair

Das **asfleakybucketpair** -Attribut ist ein optionales Attribut, das die Puffer Anforderungen für eine Variable-Bitrate-Datei beschreibt.

## <a name="global-constant"></a>Globale Konstante

g \_ wszasfleakybucketpairs

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ typbinär Datei**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut weist das folgende Format auf:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Dabei muss *wReserved* gleich NULL sein, und *Bucket* ist ein Array von WM-Lecks mit einem [**Bucket- \_ \_ \_ paar**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) . Das Array muss mindestens zwei Einträge enthalten, kann jedoch größer sein. Das Reader-Objekt verwendet dieses Attribut, um zu bestimmen, wie viel Inhalt vor der Wiedergabe puffert werden soll.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




