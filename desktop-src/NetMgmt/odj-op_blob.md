---
title: OP_BLOB
description: OP_BLOB IDL-Definition
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 757df1549d1bdb0a9a87ee22373a1903a034a1e267d087d51dac46bb6bc5a762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796890"
---
# <a name="op_blob-structure"></a>OP_BLOB-Struktur

Enthält einen nicht transparenten Bytepuffer.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Member

### <a name="cbblob"></a>cbBlob

Gibt die Größe von pBlob in Bytes an.

### <a name="pblob"></a>pBlob

Zeigt auf einen Bytepuffer.

## <a name="see-also"></a>Weitere Informationen

[**IDL-Definitionen für den Offlinedomänen-Join**](odj-idl.md)
