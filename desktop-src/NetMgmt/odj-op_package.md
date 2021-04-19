---
title: OP_PACKAGE
description: OP_PACKAGE IDL-Definition
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106339521"
---
# <a name="op_package-structure"></a>OP_PACKAGE Struktur

Enthält eine-Struktur, die eine serialisierte OP_PACKAGE_COLLECTION enthält.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>Member

### <a name="encryptiontype"></a>EncryptionType

Für zukünftige Verwendung reserviert und muss auf GUID_NULL festgelegt werden.

### <a name="encryptioncontext"></a>Verschlüsselungs Kontext

Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.

### <a name="wrappedpartcollection"></a>Wrappedpartcollection

Eine OP_BLOB-Struktur, die eine serialisierte OP_PACKAGE_COLLECTION Struktur enthält.

### <a name="cbdecryptedpartcollection"></a>cbdecryptedpartcollection

Für zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

### <a name="extension"></a>Durchwahl

Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**OP- \_ BLOB**](odj-op_blob.md)

[**\_Paket \_ Sammlung (OP)**](odj-op_package_collection.md)
