---
description: Enthält grundlegende Modul Informationen.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO Struktur (AUX \_ KLIB. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365694"
---
# <a name="aux_module_basic_info-structure"></a>\_ \_ Grundlegende \_ Informationsstruktur des aux-Moduls

Enthält grundlegende Modul Informationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**ImageBase**
</dt> <dd>

Die Basisadresse des Moduls innerhalb des Adressraums des Kernels.

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
</dt> </dl>

 

 




