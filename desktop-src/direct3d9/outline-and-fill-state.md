---
description: Primitive, die keine Texturen aufweisen, werden mit der durch ihr Material angegebenen Farbe oder ggf. mit den für die Scheitelpunkte angegebenen Farben gerendert.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Kontur- und Füllzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db18c38b7511d6fd7954ffdbf18b9e5681cb884414373fd7a22dba2ade3bebf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068940"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Kontur- und Füllzustand (Direct3D 9)

Primitive, die keine Texturen aufweisen, werden mit der durch ihr Material angegebenen Farbe oder ggf. mit den für die Scheitelpunkte angegebenen Farben gerendert. Sie können die Methode auswählen, um sie zu füllen, indem Sie einen Wert angeben, der durch den [**D3DFILLMODE-Enumerationstyp**](./d3dfillmode.md) für den D3DRS \_ FILLMODE-Renderzustand definiert wird.

Um das Dithering zu aktivieren, muss Ihre Anwendung den D3DRS \_ DITHERENABLE-Enumerationswert als ersten Parameter an [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)übergeben. Der zweite Parameter muss auf **TRUE** festgelegt werden, um das Dithering zu aktivieren, und **FALSE,** um ihn zu deaktivieren.

Manchmal kann das Zeichnen des letzten Pixels in einer Linie dazu führen, dass sich unaufdehnlich mit den umgebenden Primitiven überschneidet. Sie können dies mithilfe des \_ aufzählten D3DRS LASTPIXEL-Werts steuern. Ändern Sie diese Einstellung jedoch nicht ohne eine gewisse Vorgabe. Unter bestimmten Umständen kann das Unterdrücken des Renderings des letzten Pixels zu ungenauen Lücken zwischen Primitiven führen.

Objektgliederungen können gezeichnet werden, indem das entsprechende Strichzeichnungsmuster festgelegt wird. Der Standardzustand für das Zeichnen von Linien ist das Zeichnen von durchgezogenen Linien. Weitere Informationen finden Sie unter [Unterstützung von Strichzeichnungen im Renderzustand von D3DX (Direct3D 9).](line-drawing-support-in-d3dx.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 
