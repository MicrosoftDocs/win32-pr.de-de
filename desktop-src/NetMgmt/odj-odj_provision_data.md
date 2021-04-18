---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA IDL-Definition
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106339523"
---
# <a name="odj_provision_data-structure"></a>ODJ_PROVISION_DATA Struktur

Gibt die äußerste Serialisierungsstruktur an, die von den Offline-Domänen Beitritt-APIs

## <a name="syntax"></a>Syntax

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>Member

### <a name="ulversion"></a>ulversion

Diese muss auf 1 festgelegt werden.

### <a name="ulcblobs"></a>ulcblosb

Dies muss auf die Anzahl der Elemente im pblobarray festgelegt werden.

### <a name="pblobs"></a>pblobcontainer

Verweist auf ein Array von ODJ_BLOB Strukturen.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**ODJ- \_ BLOB**](odj-odj_blob.md)


