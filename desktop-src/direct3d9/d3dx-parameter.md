---
description: Diese Flags enthalten zusätzliche Informationen zu Effect-Parametern.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 5314ae0a13f6b9f4e246cc61c33ce626f217a4d654de2f582d18027c952bd2a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607810"
---
# <a name="d3dx_parameter"></a>D3DX-PARAMETER \_

Diese Flags enthalten zusätzliche Informationen zu Effect-Parametern.

Effect-Parameterkonst constants werden von [**D3DXPARAMETER \_ DESC verwendet.**](d3dxparameter-desc.md)



| Konstante                                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**\_D3DX-PARAMETERANMERKUNG \_**</dt> </dl> | Dieser Parameter ist als Anmerkung gekennzeichnet. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effektparametern mit Anmerkungen.](using-an-effect.md)<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**\_D3DX-PARAMETERLITERAL \_**</dt> </dl>          | Dieser Parameter ist als Literalwert gekennzeichnet. Literalparameter können sich nach der Kompilierung nicht ändern, sodass der Compiler ihre Verwendung optimieren kann. Freigegebene Parameter können nicht als Literal markiert werden. Weitere [Informationen finden Sie unter Usages and Literals (Direct3D 9) (Verwendungen und Literale (Direct3D 9)).](usages-and-literals.md) <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**D3DX-PARAMETER \_ \_ FREIGEGEBEN**</dt> </dl>             | Der Wert eines Parameters wird von allen Effekten im gleichen Namespace gemeinsam genutzt. Wenn Sie den Wert in einem Effekt ändern, wird er in allen freigegebenen Effekten geändert. Weitere Informationen [finden Sie unter Freigabeparameter.](cloning-and-sharing.md) **D3DX \_ PARAMETER \_ SHARED kann** nicht mit **D3DX \_ PARAMETER LITERAL \_ oder** **D3DX \_ PARAMETER ANNOTATION kombiniert \_ werden.**<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektkonst constants](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




