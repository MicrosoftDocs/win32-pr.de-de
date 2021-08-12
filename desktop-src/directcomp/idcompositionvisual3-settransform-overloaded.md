---
title: IDCompositionVisual3 SetTransform-Methoden (Dcomp.h)
description: Legt die Transform-Eigenschaft dieses Visuals fest. Die Transform-Eigenschaft gibt eine 3D-Transformation an, mit der das Koordinatensystem dieses Visuals geändert wird. Die -Eigenschaft kann entweder eine 4-mal-4-Transformationsmatrix oder ein Transformationsobjekt angeben.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- SetTransform-Methoden DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 08b243704c3eabae528d475c92b924f6aecfba92f923b7190c085e3e89bd1f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281237"
---
# <a name="idcompositionvisual3settransform-methods"></a>IDCompositionVisual3::SetTransform-Methoden

Legt die Transform-Eigenschaft dieses Visuals fest. Die Transform-Eigenschaft gibt eine 3D-Transformation an, mit der das Koordinatensystem dieses Visuals geändert wird. Die -Eigenschaft kann entweder eine 4-mal-4-Transformationsmatrix oder ein Transformationsobjekt angeben.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                  | Beschreibung                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform(D2D \_ MATRIX \_ 4X4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | Legt die Transform-Eigenschaft auf die angegebene Transformationsmatrix fest.<br/>      |
| [**SetTransform(IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | Legt die Transform-Eigenschaft auf das angegebene Transformationsobjekt fest.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 8 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2012-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Dcomp.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Dcomp.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDCompositionVisual3**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**IDCompositionSkewTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**IDCompositionTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**IDCompositionVisual::SetOffsetX**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**IDCompositionVisual::SetOffsetY**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
