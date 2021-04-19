---
title: WMDM_FIND_SCOPE-Enumeration
description: Der \_ \_ Enumerationstyp für den WMDM-Suchbereich definiert den Gültigkeitsbereich des Speicher Objekts.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- Device Manager der WMDM_FIND_SCOPE-Enumeration Windows Media
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
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373620"
---
# <a name="wmdm_find_scope-enumeration"></a>WMDM \_ - \_ Enumeration zum Suchen des Bereichs

Der Enumerationstyp für den **WMDM- \_ \_ Suchbereich** definiert den Gültigkeitsbereich des Speicher Objekts.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM-Such \_ \_ Bereich \_ Global**
</dt> <dd>

Suchen nach dem passenden Objekt an beliebiger Stelle auf dem Gerät.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM-Such \_ \_ Bereich \_ direkt \_ untergeordnete Elemente**
</dt> <dd>

Suchen nach dem entsprechenden Objekt innerhalb dieses Speichers und seiner untergeordneten Elemente.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





