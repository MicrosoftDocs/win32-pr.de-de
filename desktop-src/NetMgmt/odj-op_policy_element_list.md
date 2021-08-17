---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST IDL-Definition
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 1fde1bb1d2794be4fd1bf799282a0257b78ae213453566208ff64bcf7a312654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796861"
---
# <a name="op_policy_element_list-structure"></a>OP_POLICY_ELEMENT_LIST-Struktur

Definiert einen Stammregistrierungsschlüssel und ein Array von Registrierungsschlüsselelementen, die unter diesem Schlüssel konfiguriert werden sollen.

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

### <a name="psource"></a>pSource

Enthält den Pfad der Gruppenrichtlinie, aus der die enthaltenen Elemente stammen.

### <a name="ulrootkeyid"></a>ulRootKeyId

Enthält den Bezeichner des Stammregistrierungsschlüssels. muss derzeit auf HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Enthält die Anzahl der Elemente in pElements.

### <a name="pelements"></a>pElements

Enthält ein Array von OP_POLICY_ELEMENT Elementen.

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für den Offlinedomänen-Join**](odj-idl.md)

[**OP \_ \_ POLICY-ELEMENT**](odj-op_policy_element.md)
