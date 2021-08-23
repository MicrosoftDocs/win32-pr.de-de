---
description: Enthält grundlegende Modulinformationen.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO-Struktur (Aux \_ klib.h)
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
ms.openlocfilehash: e1a25af780016c226acf46348573def8505669e16f1f645fcfce1c9324bb086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956149"
---
# <a name="aux_module_basic_info-structure"></a>STRUKTUR \_ DER GRUNDLEGENDEN INFORMATIONEN DES AUX-MODULs \_ \_

Enthält grundlegende Modulinformationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Imagebase**
</dt> <dd>

Die Basisadresse des Moduls im Adressraum des Kernels.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Hilfs-API-Bibliothek, Version 1.0 oder höher<br/>                          |
| Header<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




