---
description: Sie erstellen ein Vertexpufferobjekt, indem Sie die IDirect3DDevice9::CreateVertexBuffer-Methode aufrufen, die fünf Parameter akzeptiert.
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Erstellen eines Vertexpuffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c12cb50d7879ef73d4c760ac61a0698651cb9ed7d334c90475bd2e8ee4148db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527674"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Erstellen eines Vertexpuffers (Direct3D 9)

Sie erstellen ein Vertexpufferobjekt, indem Sie die [**IDirect3DDevice9::CreateVertexBuffer-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) aufrufen, die fünf Parameter akzeptiert. Der erste Parameter gibt die Länge des Vertexpuffers in Bytes an. Verwenden Sie den Sizeof-Operator, um die Größe eines Scheitelpunktformats in Bytes zu bestimmen. Betrachten Sie das folgende benutzerdefinierte Scheitelpunktformat.


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



Um einen Scheitelpunktpuffer für vier CUSTOMVERTEX-Strukturen zu erstellen, geben Sie \[ 4 \* sizeof(CUSTOMVERTEX) \] für den *Length-Parameter* an.

Der zweite Parameter ist ein Satz von Verwendungssteuerelementen. Unter anderem bestimmt sein Wert, ob der Scheitelpunktpuffer Clippinginformationen in Form von Clipflags für Scheitelpunkte enthalten kann, die außerhalb des Anzeigebereichs vorhanden sind. Um einen Scheitelpunktpuffer zu erstellen, der keine Clipflags enthalten kann, schließen Sie das D3DUSAGE \_ DONOTCLIP-Flag für den *Usage-Parameter* ein. Das D3DUSAGE \_ DONOTCLIP-Flag wird nur angewendet, wenn Sie auch angeben, dass der Scheitelpunktpuffer transformierte Scheitelpunkte enthält. Das Flag D3DFVF \_ XYZRHW ist im *FVF-Parameter* enthalten. Die [**IDirect3DDevice9::CreateVertexBuffer-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignoriert das D3DUSAGE \_ DONOTCLIP-Flag, wenn Sie angeben, dass der Puffer nicht transformierte Scheitelpunkte enthält (D3DFVF \_ XYZ-Flag). Clippingflags belegen zusätzlichen Arbeitsspeicher, sodass ein clippingfähiger Scheitelpunktpuffer etwas größer als ein Scheitelpunktpuffer ist, der keine Clippingflags enthalten kann. Da diese Ressourcen beim Erstellen des Scheitelpunktpuffers zugeordnet werden, müssen Sie im Voraus einen clippingfähigen Scheitelpunktpuffer anfordern.

Der dritte Parameter, *FVF,* ist eine Kombination aus [D3DFVF,](d3dfvf.md) die das Scheitelpunktformat des Scheitelpunktpuffers beschreibt. Wenn Sie 0 für diesen Parameter angeben, ist der Scheitelpunktpuffer ein Nicht-FVF-Scheitelpunktpuffer. Weitere Informationen finden Sie unter [FVF-Vertexpuffer (Direct3D 9).](fvf-vertex-buffers.md) Der vierte Parameter beschreibt die Speicherklasse, in der der Scheitelpunktpuffer abgelegt werden soll.

Der letzte Parameter, den [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) akzeptiert, ist die Adresse einer Variablen, die mit einem Zeiger auf die neue [**IDirect3DVertexBuffer9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) des Scheitelpunktpufferobjekts gefüllt wird, wenn der Aufruf erfolgreich ist.

Sie können keine Clipflags für einen Scheitelpunktpuffer erstellen, der ohne Unterstützung für sie erstellt wurde.

Das folgende C++-Codebeispiel zeigt, wie das Erstellen eines Scheitelpunktpuffers im Code aussehen kann.


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunktpuffer](vertex-buffers.md)
</dt> </dl>

 

 
