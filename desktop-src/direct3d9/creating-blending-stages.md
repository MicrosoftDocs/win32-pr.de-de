---
description: Eine Mischungs Stufe ist ein Satz von Textur Vorgängen und ihren Argumenten, die definieren, wie Texturen gemischt werden.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Erstellen von Mischungs Stufen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126881"
---
# <a name="creating-blending-stages-direct3d-9"></a>Erstellen von Mischungs Stufen (Direct3D 9)

Eine Mischungs Stufe ist ein Satz von Textur Vorgängen und ihren Argumenten, die definieren, wie Texturen gemischt werden. Beim Erstellen einer Mischungs Phase rufen C++-Anwendungen die [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) -Methode auf. Der erste-Befehl gibt den Vorgang an, der ausgeführt wird. Zwei weitere Aufrufe definieren die Argumente, auf die der Vorgang angewendet wird. Im folgenden Codebeispiel wird die Erstellung einer Mischungs Stufe veranschaulicht.


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



Texel-Daten in Texturen enthalten Farb-und Alpha Werte. Anwendungen können separate Vorgänge für Farb-und Alpha Werte in einer einzelnen Mischungs Stufe definieren. Jeder Vorgang, jede Farbe und jedes Alpha hat seine eigenen Argumente. Weitere Informationen finden Sie unter [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

Obwohl Sie nicht Teil der Direct3D-API sind, können Sie die folgenden Makros in Ihre Anwendung einfügen, um den Code abzukürzen, der zum Erstellen von Textur Mischungs Stufen erforderlich ist.


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Mischung](texture-blending.md)
</dt> </dl>

 

 
