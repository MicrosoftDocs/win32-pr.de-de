---
description: 'Sie erstellen ein Vertex-Puffer Objekt, indem Sie die IDirect3DDevice9:: createvertexbuffer-Methode aufrufen, die fünf Parameter akzeptiert.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Erstellen eines Scheitelpunkt Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343194"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Erstellen eines Scheitelpunkt Puffers (Direct3D 9)

Sie erstellen ein Vertex-Puffer Objekt, indem Sie die [**IDirect3DDevice9:: createvertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) -Methode aufrufen, die fünf Parameter akzeptiert. Der erste Parameter gibt die Vertex-Pufferlänge in Bytes an. Verwenden Sie den sizeof-Operator, um die Größe eines Scheitelpunkt Formats in Bytes zu bestimmen. Beachten Sie das folgende benutzerdefinierte Scheitelpunkt Format.


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



Um einen Vertex-Puffer zum Speichern von vier CustomVertex-Strukturen zu erstellen, geben Sie \[ 4 \* sizeof (CustomVertex) \] für den *length* -Parameter an.

Der zweite Parameter ist ein Satz von Verwendungs Steuerelementen. Unter anderem bestimmt der Wert, ob der Vertex-Puffer clippinginformationen in Form von Clip-Flags enthalten kann, die außerhalb des Anzeige Bereichs vorhanden sind. Zum Erstellen eines Scheitelpunkt Puffers, der keine Clip-Flags enthalten kann, schließen Sie das D3DUSAGE \_ DoNotClip-Flag für den *Usage* -Parameter ein. Das \_ Flag D3DUSAGE DoNotClip wird nur angewendet, wenn Sie auch angeben, dass der Vertexpuffer transformierte Scheitel Punkte enthalten soll \_ . das Flag D3DFVF xyzrhw ist im Parameter " *f* ..." enthalten. Die [**IDirect3DDevice9:: samatevertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) -Methode ignoriert das \_ Flag D3DUSAGE DoNotClip, wenn Sie angeben, dass der Puffer untransformierte Scheitel Punkte (das D3DFVF \_ XYZ-Flag) enthalten soll. Clippingflags belegen zusätzlichen Arbeitsspeicher, sodass ein Clipping-fähiger Vertex-Puffer etwas größer als ein Scheitelpunkt Puffer ist, der keine clippingflags enthalten kann. Da diese Ressourcen zugewiesen werden, wenn der Scheitelpunkt Puffer erstellt wird, müssen Sie im Voraus einen Clipping-fähigen Vertex-Puffer anfordern.

Der dritte Parameter, " *f VF*", ist eine Kombination aus [D3DFVF](d3dfvf.md) , die das Scheitelpunkt Format des Scheitelpunkt Puffers beschreibt. Wenn Sie für diesen Parameter den Wert 0 angeben, ist der Vertex-Puffer ein nicht-f-b-Puffer. Weitere Informationen finden Sie unter [f-Server-Vertex-Puffer (Direct3D 9)](fvf-vertex-buffers.md). Der vierte Parameter beschreibt die Speicher Klasse, in die der Scheitelpunkt Puffer platziert werden soll.

Der letzte Parameter, den [**IDirect3DDevice9:: anatevertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) akzeptiert, ist die Adresse einer Variablen, die mit einem Zeiger auf die neue [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) -Schnittstelle des Vertex-Puffer Objekts gefüllt wird, wenn der-Befehl erfolgreich ausgeführt wird.

Sie können keine Clip Flags für einen Vertex-Puffer erstellen, der ohne Unterstützung für Sie erstellt wurde.

Im folgenden C++-Codebeispiel wird gezeigt, wie das Erstellen eines Scheitelpunkt Puffers im Code aussehen könnte.


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

[Vertex-Puffer](vertex-buffers.md)
</dt> </dl>

 

 
