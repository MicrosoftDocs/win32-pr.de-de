---
description: Gibt eine Eigenschaft an, die für einen Übergang oder einen Effekt festgelegt werden soll, zusammen mit der Anzahl der unterschiedlichen Werte, die die Eigenschaft über die Dauer des Übergangs oder Effekts annimmt.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: DEXTER_VALUE Struktur ("qedit. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371593"
---
# <a name="dexter_value-structure"></a>Struktur von Dexter- \_ Werten

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Gibt eine Eigenschaft an, die für einen Übergang oder einen Effekt festgelegt werden soll, zusammen mit der Anzahl der unterschiedlichen Werte, die die Eigenschaft über die Dauer des Übergangs oder Effekts annimmt.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>Member

<dl> <dt>

**Ramelow**
</dt> <dd>

Der Wert der Eigenschaft.

</dd> <dt>

**imposante**
</dt> <dd>

Der Zeitpunkt, zu dem die Eigenschaft den Wert annimmt, relativ zum Anfang des Übergangs oder Effekts.

</dd> <dt>

**dwinterp**
</dt> <dd>

Flag, das angibt, wie die-Eigenschaft vom vorherigen Wert zu diesem Wert verläuft. Dies muss eine der folgenden Ressourcen sein:



| Wert                                                                                                                                                                           | Bedeutung                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**dexterf \_ springen**</dt> </dl>                      | Die Eigenschaft springt zum angegebenen Zeitpunkt sofort in den neuen Wert.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**dexterf- \_ Interpolate**</dt> </dl> | Die-Eigenschaft wird linear aus dem vorherigen Wert interpoliert.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipropertysetter**](ipropertysetter.md)
</dt> <dt>

[**Dexter \_ -Parameter**](dexter-param.md)
</dt> </dl>

 

 




