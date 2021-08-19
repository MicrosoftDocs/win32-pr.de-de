---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT IDL-Definition
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983384"
---
# <a name="op_policy_element-structure"></a>OP_POLICY_ELEMENT-Struktur

Definiert einen Registrierungsschlüssel und einen Wertnamen, -typ und -wert, der unter diesem Schlüssel konfiguriert werden soll.

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

### <a name="pkeypath"></a>pKeyPath

Enthält den Pfad des Registrierungsschlüssels.

### <a name="pvaluename"></a>pValueName

Enthält den Namen des Registrierungswerts.

### <a name="ulvaluetype"></a>ulValueType

Enthält einen der Werte aus [Registrierungswerttypen.](../sysinfo/registry-value-types.md)

### <a name="cbvaluedata"></a>cbValueData

Enthält die Größe von pValueData in Bytes.

### <a name="ulvaluetype"></a>ulValueType

Enthält den Wert des Registrierungswerts.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen für Den Offlinedomänen join**](odj-idl.md)