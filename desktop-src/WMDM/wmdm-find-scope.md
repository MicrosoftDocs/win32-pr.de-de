---
title: WMDM_FIND_SCOPE Enumeration
description: Der WMDM \_ FIND \_ SCOPE-Enumerationstyp definiert den Bereich des Speicherobjekts.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE windows Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb7d4902b1acd4223f25bdc5e8a7ca76d4495b5f465687a56b295ad2d5fbfa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863010"
---
# <a name="wmdm_find_scope-enumeration"></a>WMDM \_ FIND \_ SCOPE-Enumeration

Der **WMDM \_ FIND \_ SCOPE-Enumerationstyp** definiert den Bereich des Speicherobjekts.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ FIND \_ SCOPE \_ GLOBAL**
</dt> <dd>

Suchen Sie an einer beliebigen Stelle auf dem Gerät nach dem übereinstimmenden Objekt.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ SUCHEN NACH \_ UNMITTELBAREN \_ DIREKTEN DIREKT-DATEIEN IM \_ BEREICH**
</dt> <dd>

Suchen sie nach dem übereinstimmenden Objekt in diesem Speicher und dessen unteren Objekten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





