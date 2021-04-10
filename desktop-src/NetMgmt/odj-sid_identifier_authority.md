---
title: SID_IDENTIFIER_AUTHORITY
description: SID_IDENTIFIER_AUTHORITY IDL-Definition
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102526"
---
# <a name="sid_identifier_authority-structure"></a>SID_IDENTIFIER_AUTHORITY Struktur

Enthält eine SID-Bezeichnerautorität.

## <a name="syntax"></a>Syntax

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Member

### <a name="value"></a>Wert

Muss auf die sechs Bytes der SID-Bezeichnerautorität festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)