---
description: Definiert Bitmuster, die benutzerdefinierte Clippingebenen ermöglichen. Diese Makros sind beim Festlegen von Werten für den D3DRS clipplaneenable-Rendering als benutzerfreundlicher Definition definiert \_ .
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: D3DCLIPPLANEn-Makro (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394086"
---
# <a name="d3dclipplanen-macro"></a>D3DCLIPPLANEn-Makro

Definiert Bitmuster, die benutzerdefinierte Clippingebenen ermöglichen. Diese Makros sind beim Festlegen von Werten für den D3DRS clipplaneenable-Rendering als benutzerfreundlicher Definition definiert \_ .

## <a name="syntax"></a>Syntax


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Benutzerdefinierte Clippingebenen werden aktiviert, wenn der im D3DRS \_ clipplaneenable-renderzustand festgelegte Wert mindestens ein Set Bits enthält (d. h. ist nicht 0). Der Wert des "Rendering-State" ist nicht wichtig. der Wert wird vom System nicht als Zahl interpretiert. Stattdessen aktiviert der Wert die Clipping-Ebene, deren entsprechendes Bit festgelegt ist. Mit Bit 0 wird der Zustand der ersten Clippingebene (bei Index 0), Bit 1 der zweiten Ebene usw. gesteuert.

Die von diesen Makros erstellten Bitmuster können mithilfe eines logischen OR-Vorgangs kombiniert werden, um mehrere Clippingebenen gleichzeitig zu aktivieren. Wenn Sie eines dieser Makros aus der Kombination weglassen, wird die Clippingebene an diesem Index deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




