---
title: IDCompositionVisual SetClip-Methoden (Dcomp.h)
description: Legt die Clip-Eigenschaft dieses Visuals auf den angegebenen rechteckigen Bereich oder clip-Objekt fest.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip-Methoden DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 1cc1d0f24c30e6ec11ecaa40b0317109eddaf432ee311a5b9545f34f7afa8582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043058"
---
# <a name="idcompositionvisualsetclip-methods"></a>IDCompositionVisual::SetClip-Methoden

Legt die Clip-Eigenschaft dieses Visuals auf den angegebenen rechteckigen Bereich oder clip-Objekt fest. Die Clip-Eigenschaft schränkt das Rendering der visuellen Teilstruktur, die an diesem Visual gerootet ist, auf einen rechteckigen Bereich ein.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                | Beschreibung                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SetClip(const D2D \_ RECT \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | Legt die Clip-Eigenschaft auf den angegebenen rechteckigen Bereich fest.<br/> |
| [**SetClip(IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | Legt die Clip-Eigenschaft auf das angegebene Clipobjekt fest.<br/>        |



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

[Freistellen](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
