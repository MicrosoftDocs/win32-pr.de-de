---
title: ODJ_SID
description: ODJ_SID IDL-Definition
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104039797"
---
# <a name="odj_sid-structure"></a>ODJ_SID Struktur

Enthält eine Sicherheits-ID (SID).

## <a name="syntax"></a>Syntax

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>Member

### <a name="revision"></a>Revision

Muss auf die SID-Revision festgelegt werden.

### <a name="subauthoritycount"></a>Subautoritycount

Muss auf die Anzahl der Elemente in der untergeordneten Autorität festgelegt werden.

### <a name="identifierauthority"></a>Identifiziererautorität

Muss auf den Bezeichner der SID-Autorität festgelegt werden.

### <a name="subauthority"></a>Untergeordnete Autorität

Muss ein Array von sid-untergeordneten Autoritäten enthalten.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**ODJ- \_ sid- \_ \_ Bezeichnerautorität**](odj-sid_identifier_authority.md)
