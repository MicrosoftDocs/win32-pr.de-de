---
title: ASFLeakyBucketPairs
description: Das ASFLeakyBucketPairs-Attribut ist ein optionales Attribut, das die Pufferanforderungen für eine Datei mit variabler Bitrate beschreibt.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs windows Media Format
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76de649a069b0cfec74fabe1a41d6cfa659b39448257a4bc966065e1bce98ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434619"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

Das **ASFLeakyBucketPairs-Attribut** ist ein optionales Attribut, das die Pufferanforderungen für eine Datei mit variabler Bitrate beschreibt.

## <a name="global-constant"></a>Globale Konstante

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BINARY**

## <a name="remarks"></a>Hinweise

Dieses Attribut hat das folgende Format:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Wobei *wReserved* gleich 0 (null) sein muss und *bucket* ein Array von [**WM \_ LEAKY BUCKET \_ \_ PAIR-Strukturen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) ist. Das Array muss mindestens zwei Einträge enthalten, kann jedoch größer sein. Das Readerobjekt verwendet dieses Attribut, um die Menge des Inhalts zu bestimmen, der vor der Wiedergabe gepuffert werden soll.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




