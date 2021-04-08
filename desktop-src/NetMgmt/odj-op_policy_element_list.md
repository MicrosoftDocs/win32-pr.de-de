---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST IDL-Definition
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734697"
---
# <a name="op_policy_element_list-structure"></a>OP_POLICY_ELEMENT_LIST Struktur

Definiert einen Stamm Registrierungsschlüssel und ein Array von Registrierungsschlüssel Elementen, die unter diesem Schlüssel konfiguriert werden sollen.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>Member

### <a name="psource"></a>psource

Enthält den Pfad der Gruppenrichtlinie-Datei, aus der die enthaltenen Elemente stammen.

### <a name="ulrootkeyid"></a>ulrootkeyid

Enthält den Bezeichner des Stamm Registrierungsschlüssels. muss derzeit auf HKEY_LOCAL_MACHINE festgelegt werden.

### <a name="celements"></a>cElements

Enthält die Anzahl der Elemente in pelements.

### <a name="pelements"></a>pelements

Enthält ein Array von OP_POLICY_ELEMENT Elementen.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**OP- \_ Richtlinien \_ Element**](odj-op_policy_element.md)
