---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING IDL-Definition
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3578c62f110eafd053ed97bbe1f8b5015156d02c4b879ff8111ff13f28dfab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891239"
---
# <a name="odj_unicode_string-structure"></a>ODJ_UNICODE_STRING-Struktur

Enthält eine Unicode-Zeichenfolge.

## <a name="syntax"></a>Syntax

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a>Member

### <a name="length"></a>Länge

Muss auf die Anzahl der Bytes in Buffer festgelegt werden, die die Zeichenfolge enthalten, ohne das NULL-Abschlusszeichen.

### <a name="maximumlength"></a>MaximumLength

Dies MUSS auf die Gesamtzahl der Bytes in Buffer festgelegt werden, ohne das NULL-Abschlusszeichen einzuschließt.

### <a name="buffer"></a>Buffer

Dabei muss es sich um eine Unicode-Zeichenfolge handeln.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen für Den Offlinedomänen join**](odj-idl.md)
