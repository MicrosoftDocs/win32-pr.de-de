---
title: OP_JOINPROV3_PART
description: OP_JOINPROV3_PART IDL-Definition
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391169"
---
# <a name="op_joinprov3_part-structure"></a>OP_JOINPROV3_PART Struktur

Enthält zusätzliche Informationen, die zum Konfigurieren eines Clients verwendet werden, der einer Domäne hinzugefügt wurde.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Member

### <a name="rid"></a>Gesagt

Muss auf den relativen Bezeichner der SID des Computer Kontos festgelegt werden.

### <a name="lpsid"></a>lpsid

Muss auf die SID des Computer Kontos in Form einer Zeichenfolge festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)
