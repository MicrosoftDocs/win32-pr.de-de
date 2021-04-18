---
description: Gibt den Wert an, den eine Eigenschaft zu einem bestimmten Zeitpunkt annimmt.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: DEXTER_PARAM Struktur ("qedit. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371594"
---
# <a name="dexter_param-structure"></a>Dexter- \_ param-Struktur

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Gibt den Wert an, den eine Eigenschaft zu einem bestimmten Zeitpunkt annimmt.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Der Name der Eigenschaft.

</dd> <dt>

**dispID**
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

**nwerte**
</dt> <dd>

Anzahl der Werte, die von der-Eigenschaft angenommen werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das-Objekt muss die **IDispatch** -Schnittstelle unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipropertysetter**](ipropertysetter.md)
</dt> <dt>

[**Wert von Dexter \_**](dexter-value.md)
</dt> </dl>

 

 




