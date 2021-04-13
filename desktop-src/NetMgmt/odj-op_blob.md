---
title: OP_BLOB
description: OP_BLOB IDL-Definition
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391173"
---
# <a name="op_blob-structure"></a>OP_BLOB Struktur

Enthält einen nicht transparenten Byte Puffer.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Member

### <a name="cbblob"></a>cbblob

Gibt die Größe des pBlob in Bytes an.

### <a name="pblob"></a>pBlob

Verweist auf einen Byte Puffer.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)
