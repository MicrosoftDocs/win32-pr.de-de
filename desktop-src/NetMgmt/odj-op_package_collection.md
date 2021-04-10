---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION IDL-Definition
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104039795"
---
# <a name="op_package_part_collection-structure"></a>OP_PACKAGE_PART_COLLECTION Struktur

Gibt eine-Struktur an, die ein Array von OP_PACKAGE_PART-Strukturen enthält.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a>Member

### <a name="cparts"></a>cparts

Enthält die Anzahl der Elemente in pparts.

### <a name="pparts"></a>pparts

Enthält ein Array von OP_PACKAGE_PART Strukturen.

### <a name="extension"></a>Durchwahl

Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**OP \_ - \_ Paketteil**](odj-op_package_part.md)

[**OP- \_ BLOB**](odj-op_blob.md)

