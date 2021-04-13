---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL-Definition
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391172"
---
# <a name="op_policy_part-structure"></a>OP_POLICY_PART Struktur

Enthält ein Array von OP_POLICY_ELEMENT_LIST Strukturen.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>Member

### <a name="celementlists"></a>celementlists

Enthält die Anzahl der Elemente in pelementlists.

### <a name="pelementlists"></a>pelementlists

Enthält ein Array von OP_POLICY_ELEMENT_LIST Strukturen.

### <a name="extension"></a>Durchwahl

Für zukünftige Verwendung reserviert und muss alle Nullen enthalten.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**Liste der OP- \_ Richtlinien \_ Elemente \_**](odj-op_policy_element_list.md)
