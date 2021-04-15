---
title: OP_PACKAGE_PART
description: OP_PACKAGE_PART IDL-Definition
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104213076"
---
# <a name="op_package_part-structure"></a>OP_PACKAGE_PART Struktur

Definiert eine-Struktur, die ein DataSet enthält, das durch eine GUID identifiziert wird.

## <a name="syntax"></a>Syntax

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>Member

### <a name="parttype"></a>Paramettype

Identifiziert die serialisierte Struktur, die in einem Teil der folgenden Tabelle enthalten ist:

|Paramettype|Bedeutung|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80F 843f 868c3}|Enthält eine serialisierte ODJ_WIN7_BLOB Struktur.|
|GUID_JOIN_PROVIDER2 {57bfc56b-52b f 9-480c-adcb-91b3f 8a82317}|Enthält eine serialisierte OP_JOIN_PROV2_PART Struktur.|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|Enthält eine serialisierte OP_JOIN_PROV3_PART Struktur.|
|GUID_CERT_PROVIDER {9c0971e9-832b-4873-8e87-ef1419d4781e}|Enthält eine serialisierte OP_CERT_PART Struktur.|
|GUID_POLICY_PROVIDER {68b602a-0c09-48ce-b75f -07b7bd58f EC}|Enthält eine serialisierte OP_POLICY_PART Struktur.|

### <a name="ulflags"></a>ulFlags

Muss auf 0 (null) oder mehrere der folgenden Flags festgelegt werden:

|Wert|Bedeutung|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)|Dieser Paketteil ist als unverzichtbar anzusehen. Wenn der Consumer dieses Paketteil nicht erkennt oder nicht erfolgreich verarbeitet werden kann, muss der gesamte Vorgang fehlschlagen.|

### <a name="part"></a>Teil

Enthält eine serialisierte Struktur in einer OP_BLOB-Struktur. Die jeweilige Struktur wird durch einen "paramettype" bestimmt.

### <a name="extension"></a>Durchwahl

Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.

## <a name="see-also"></a>Siehe auch

[**IDL-Definitionen im Offline-Domänen Beitritt**](odj-idl.md)

[**OP- \_ BLOB**](odj-op_blob.md)
