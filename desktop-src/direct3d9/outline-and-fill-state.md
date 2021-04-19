---
description: Primitive, die keine Texturen aufweisen, werden mit der Farbe gerendert, die durch Ihr Material angegeben wird, oder mit den Farben, die für die Scheitel Punkte angegeben sind, falls vorhanden.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Umriss und Füll Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342545"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Umriss und Füll Zustand (Direct3D 9)

Primitive, die keine Texturen aufweisen, werden mit der Farbe gerendert, die durch Ihr Material angegeben wird, oder mit den Farben, die für die Scheitel Punkte angegeben sind, falls vorhanden. Sie können die Methode auswählen, um Sie auszufüllen, indem Sie einen Wert angeben, der vom [**D3DFILLMODE**](./d3dfillmode.md) -Enumerationstyp für den D3DRS \_ FillMode-renderzustand definiert wird.

Um das Dithering zu aktivieren, muss die Anwendung den D3DRS \_ ditherenable-Enumerationswert als ersten Parameter an [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)übergeben. Der zweite Parameter muss auf **true** festgelegt werden, um das Dithering zu aktivieren, und **false** , um es zu deaktivieren.

Manchmal kann das Zeichnen des letzten Pixels in einer Zeile zu einer unschönen Überschneidung mit umgebenden primitiven führen. Dies können Sie mit dem \_ Enumerationswert D3DRS lastpixel steuern. Ändern Sie diese Einstellung jedoch nicht, ohne dass dies der Fall ist. Unter bestimmten Bedingungen kann das Unterdrücken des Renderings des letzten Pixels zu unansehnlichen Lücken zwischen primitiven führen.

Objekt umrissen können durch Festlegen des entsprechenden Linien Zeichnungs Musters gezeichnet werden. Der Standardzeilen Zeichnungs Zustand ist das Zeichnen von vollziehen. Weitere Informationen finden Sie [unter Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) Rendering State.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 
