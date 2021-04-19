---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING IDL-Definition
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106341973"
---
# <a name="odj_unicode_string-structure"></a>ODJ_UNICODE_STRING Struktur

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

Muss auf die Anzahl der Bytes im Puffer mit der Zeichenfolge festgelegt werden, ohne das NULL-Terminator.

### <a name="maximumlength"></a>MaximumLength

Dies muss auf die Gesamtzahl der Bytes im Puffer festgelegt werden, ohne das NULL-Terminator.

### <a name="buffer"></a>Buffer

Dabei muss es sich um eine Unicode-Zeichenfolge handeln.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)
