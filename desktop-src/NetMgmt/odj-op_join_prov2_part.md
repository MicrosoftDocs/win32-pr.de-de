---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART IDL-Definition
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102523"
---
# <a name="op_joinprov2_part-structure"></a>OP_JOINPROV2_PART Struktur

Enthält zusätzliche Informationen, die zum Konfigurieren eines Clients verwendet werden, der einer Domäne hinzugefügt wurde.

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

Muss entweder auf NULL oder auf einen der folgenden Werte festgelegt werden:

|Wert|Bedeutung|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|Die in "lpsitename" angegebene Site muss als dauerhafter Standort für den Client angesehen werden.|

### <a name="lpnetbiosname"></a>lpnetbiosname

Enthält den NetBIOS-Namen des Computer Kontos im Unicode-Format.

### <a name="lpsitename"></a>lpsitename

Enthält den Namen der Active Directory Site, die vom Client verwendet werden soll.

### <a name="lpprimarydnsdomain"></a>lpprimarydnsdomain

Enthält den primären DNS-Domänen Namen, den der Client verwenden soll.

### <a name="dwreserved"></a>dwReserved

Für zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

### <a name="lpreserved"></a>lpReserved

Für zukünftige Verwendung reserviert und muss auf NULL festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)
