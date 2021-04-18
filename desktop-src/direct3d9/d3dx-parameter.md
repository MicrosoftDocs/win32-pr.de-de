---
description: Diese Flags bieten zusätzliche Informationen zu Effekt Parametern.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
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
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371923"
---
# <a name="d3dx_parameter"></a>D3DX- \_ Parameter

Diese Flags bieten zusätzliche Informationen zu Effekt Parametern.

Effektparameter Konstanten werden von [**D3DXPARAMETER- \_**](d3dxparameter-desc.md)Elementen verwendet.



| Konstante                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**D3DX- \_ Parameter \_ Anmerkung**</dt> </dl> | Dieser Parameter ist als Anmerkung gekennzeichnet. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit Anmerkungen](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**D3DX \_ \_ Parameterliterale**</dt> </dl>          | Dieser Parameter ist als Literalwert gekennzeichnet. Literalparameter können nach der Kompilierung nicht geändert werden, sodass der Compiler seine Verwendung optimieren kann. Freigegebene Parameter können nicht als Literale gekennzeichnet werden. Weitere Informationen finden Sie unter [Verwendungen und Literale (Direct3D 9)](usages-and-literals.md). <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**D3DX- \_ Parameter frei \_ gegeben**</dt> </dl>             | Der Wert eines Parameters wird von allen Effekten im gleichen Namespace gemeinsam genutzt. Wenn Sie den Wert in einem Effekt ändern, wird er in allen gemeinsam genutzten Effekten geändert. Siehe [Freigabe Parameter](cloning-and-sharing.md). **D3DX \_ Der frei \_ gegebene Parameter** kann nicht mit der **D3DX- \_ Parameter \_ Literale** oder der **D3DX- \_ Parameter \_ Anmerkung** kombiniert werden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Konstanten](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




