---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT IDL-Definition
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316905"
---
# <a name="op_policy_element-structure"></a>OP_POLICY_ELEMENT Struktur

Definiert einen Registrierungsschlüssel und einen Wertnamen,-Typ und-Wert, die unter diesem Schlüssel konfiguriert werden sollen.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>Member

### <a name="pkeypath"></a>pkeypath

Enthält den Pfad des Registrierungsschlüssels.

### <a name="pvaluename"></a>pvaluename

Enthält den Namen des Registrierungs Werts.

### <a name="ulvaluetype"></a>ulvaluetype

Enthält einen der Werte aus [Registrierungs Werttypen](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>cbvaluedata

Enthält die Größe von pvaluedata in Bytes.

### <a name="ulvaluetype"></a>ulvaluetype

Enthält den Wert des Registrierungs Werts.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)