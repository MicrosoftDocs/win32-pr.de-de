---
title: ODJ_BLOB
description: ODJ_BLOB IDL-Definition
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104474590"
---
# <a name="odj_blob-structure"></a>ODJ_BLOB Struktur

Gibt eine-Struktur an, die entweder eine serialisierte ODJ_WIN7BLOB Struktur oder eine serialisierte OP_PACKAGE Struktur enthält.

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

### <a name="ulodjformat"></a>ulodjformat

Gibt die logische Version der Struktur an und muss auf einen der folgenden Werte festgelegt werden:

|Wert|Bedeutung|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Die in pBlob enthaltenen Bytes müssen eine serialisierte ODJ_WIN7_BLOB Struktur enthalten.|
|ODJ_WIN8_FORMAT (0x00000002)|Die in pBlob enthaltenen Bytes müssen eine serialisierte OP_PACKAGE Struktur enthalten.|

### <a name="cbblob"></a>cbblob

Dieser Wert muss auf die Anzahl der Bytes im pBlob-Array festgelegt werden.

### <a name="pblob"></a>pBlob

Verweist auf einen Byte Puffer, der eine serialisierte Struktur enthält, wie von dem oben genannten "ulodjformat" angegeben.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

