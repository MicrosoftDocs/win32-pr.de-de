---
title: ODJ_BLOB
description: ODJ_BLOB IDL-Definition
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: aa1c2b593e0e9f63a52672eb3b29ee83fbf86ea91d7f4860f2351a8e4538f05d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779570"
---
# <a name="odj_blob-structure"></a>ODJ_BLOB-Struktur

Gibt eine -Struktur an, die entweder eine serialisierte ODJ_WIN7BLOB struktur oder eine serialisierte OP_PACKAGE enthält.

## <a name="syntax"></a>Syntax

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Member

### <a name="ulodjformat"></a>ulODJFormat

Gibt die logische Version der -Struktur an und muss auf einen der folgenden Werte festgelegt werden:

|Wert|Bedeutung|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Die in pBlob enthaltenen Bytes müssen eine serialisierte ODJ_WIN7_BLOB enthalten.|
|ODJ_WIN8_FORMAT (0x00000002)|Die in pBlob enthaltenen Bytes müssen eine serialisierte OP_PACKAGE enthalten.|

### <a name="cbblob"></a>cbBlob

Dies muss auf die Anzahl der Bytes im pBlob-Array festgelegt werden.

### <a name="pblob"></a>pBlob

Zeigt auf einen Bytepuffer, der eine serialisierte Struktur enthält, wie oben von ulODJFormat angegeben.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen für den Offlinedomänen-Join**](odj-idl.md)

