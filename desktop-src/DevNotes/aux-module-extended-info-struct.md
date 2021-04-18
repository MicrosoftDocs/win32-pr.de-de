---
description: Enthält Informationen zu erweiterten Modulen.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: AUX_MODULE_EXTENDED_INFO Struktur (AUX \_ KLIB. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354740"
---
# <a name="aux_module_extended_info-structure"></a>\_ \_ Erweiterte \_ Informationsstruktur des aux-Moduls

Enthält Informationen zu erweiterten Modulen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**BasicInfo**
</dt> <dd>

Eine [**\_ \_ grundlegende \_ Informationsstruktur von aux Module**](aux-module-basic-info-struct.md) .

</dd> <dt>

**ImageSize**
</dt> <dd>

Die Größe (in Bytes) des geladenen Moduls.

</dd> <dt>

**Dateinameoffset**
</dt> <dd>

Der Offset des Datei namens innerhalb des **fullpathname** -Puffers.

</dd> <dt>

**Fullpathname**
</dt> <dd>

Der vollständige Pfad des Moduls.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher<br/>                          |
| Header<br/>          | <dl> <dt>AUX \_ KLIB. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Auxklibquerymoduleinformation"**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**\_ \_ grundlegende \_ Informationen zu aux-Modulen**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




