---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART IDL-Definition
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fa6853846695c02aabf85d0be865254608b9d4c00f39a372e99f1332e6eb4003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012458"
---
# <a name="op_joinprov2_part-structure"></a>OP_JOINPROV2_PART-Struktur

Enthält zusätzliche Informationen, die zum Konfigurieren eines Clients verwendet werden, der einer Domäne beigetreten ist.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>Member

### <a name="dwflags"></a>dwFlags

Muss entweder auf 0 (null) oder einen der folgenden Werte festgelegt werden:

|Wert|Bedeutung|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|Der in lpSiteName angegebene Standort MUSS als dauerhafter Standort für den Client betrachtet werden.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Enthält den Netbios-Namen des Computerkontos im Unicode-Format.

### <a name="lpsitename"></a>lpSiteName

Enthält den Namen des Active Directory-Standorts, den der Client verwenden soll.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Enthält den primären DNS-Domänennamen, den der Client verwenden soll.

### <a name="dwreserved"></a>dwReserved

Für die zukünftige Verwendung reserviert und muss auf 0 festgelegt werden.

### <a name="lpreserved"></a>lpReserved

Für die zukünftige Verwendung reserviert und muss auf NULL festgelegt werden.

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für den Offlinedomänen-Join**](odj-idl.md)
