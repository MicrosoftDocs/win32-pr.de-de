---
title: IDCompositionVisual SetTransform-Methoden (Dcomp.h)
description: Legt die Transform-Eigenschaft dieses Visuals fest. Die Transform-Eigenschaft gibt eine 2D-Transformation an, die verwendet wird, um das Koordinatensystem dieses Visuals zu ändern. Die -Eigenschaft kann entweder eine 3:2-Transformationsmatrix oder ein Transformationsobjekt angeben.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: b38c2e8fce2f0687b78b65574858a38bba681c6bc1174cab13dfa254e3b186c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281247"
---
# <a name="idcompositionvisualsettransform-methods"></a>IDCompositionVisual::SetTransform-Methoden

Legt die Transform-Eigenschaft dieses Visuals fest. Die Transform-Eigenschaft gibt eine 2D-Transformation an, die verwendet wird, um das Koordinatensystem dieses Visuals zu ändern. Die -Eigenschaft kann entweder eine 3:2-Transformationsmatrix oder ein Transformationsobjekt angeben.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                    | Beschreibung                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform(D2D \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | Legt die Transform-Eigenschaft auf die angegebene Transformationsmatrix fest.<br/>      |
| [**SetTransform(IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | Legt die Transform-Eigenschaft auf das angegebene Transformationsobjekt fest.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2012-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Dcomp.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Dcomp.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

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
