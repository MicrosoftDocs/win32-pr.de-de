---
description: Ein FVF-Code beschreibt den Inhalt von Scheitelpunkten, die in einem einzelnen Datenstrom überlappend gespeichert sind.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: FVF-Codes der Funktion korrigiert (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4fb691192fcc4dbd7dc42c4d6c00829c209f87f68ec32ea42f6c26ff4663c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069190"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>FVF-Codes der Funktion korrigiert (Direct3D 9)

Ein FVF-Code beschreibt den Inhalt von Scheitelpunkten, die in einem einzelnen Datenstrom überlappend gespeichert sind. Im Allgemeinen werden Daten angegeben, die von der Verarbeitungspipeline für feste Funktionsvertex verarbeitet werden sollen. Dies ist eine Vertexdeklaration im älteren Stil. Informationen zum aktuellen Vertexdeklarationsstil finden Sie unter [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

Direct3D-Anwendungen können Modellvertices auf verschiedene Weise definieren. Die Unterstützung für flexible Scheitelpunktdefinitionen, auch als flexible Vertexformate oder flexible Vertexformatcodes bezeichnet, ermöglicht es Ihrer Anwendung, nur die benötigten Scheitelpunktkomponenten zu verwenden, sodass die nicht verwendeten Komponenten wegfallen. Wenn Sie nur die erforderlichen Scheitelpunktkomponenten verwenden, kann Ihre Anwendung Arbeitsspeicher sparen und die Verarbeitungsbandbreite minimieren, die zum Rendern von Modellen erforderlich ist. Sie beschreiben, wie Ihre Scheitelpunkte formatiert werden, indem Sie eine Kombination aus [D3DFVF-Codes](d3dfvf.md) verwenden.

Die FVF-Spezifikation enthält Formate für die Punktgröße, die von D3DFVF PSIZE angegeben \_ werden. Diese Größe wird in Kameraraumeinheiten für nicht transformierte und helle Scheitelpunkte (TL) und in Geräteraumeinheiten für TL-Scheitelpunkte ausgedrückt.

Die Renderingmethoden der [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) stellen C++-Anwendungen Methoden bereit, die eine Kombination dieser Flags akzeptieren, und verwenden sie, um zu bestimmen, wie Primitive gerendert werden. Im Grunde teilen diese Flags dem System mit, welche Vertexkomponenten – Position, Vertexmischungsgewichtungen, Normal, Farben und Anzahl und Format der Texturkoordinaten – ihre Anwendung verwendet und indirekt, welche Teile der Renderingpipeline Direct3D auf sie anwenden soll. Darüber hinaus kommuniziert das Vorhandensein oder Fehlen eines bestimmten Vertexformatflags mit dem System, welche Vertexkomponentenfelder im Arbeitsspeicher vorhanden sind und die Sie ausgelassen haben.

Um Geräteeinschränkungen zu ermitteln, können Sie ein Gerät nach den Werten von D3DFVFCAPS \_ DONOTSTRIPELEMENTS und D3DFVFCAPS \_ TEXCOORDCOUNTMASK im FVFCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)abfragen.

Texturkoordinaten können in verschiedenen Formaten deklariert werden, sodass Texturen mit nur einer Koordinate oder bis zu vier Texturkoordinaten (für 2D-projizierte Texturkoordinaten) adressiert werden können. Weitere Informationen finden Sie unter [Texturkoordinatenformate (Direct3D 9).](texture-coordinate-formats.md) Verwenden Sie den [**D3DFVF \_ TEXCOORDSIZEN-Makrosatz,**](d3dfvf-texcoordsizen.md) um Bitmuster zu erstellen, die die Texturkoordinatenformate identifizieren, die im Scheitelpunktformat verwendet werden.

Keine Anwendung verwendet jede Komponente. Die reziprozitäten homogenen Felder W (RHW) und Vertex normal schließen sich gegenseitig aus. Die meisten Anwendungen versuchen auch nicht, alle acht Sätze von Texturkoordinaten zu verwenden, aber Direct3D verfügt über diese Kapazität. Es gibt mehrere Einschränkungen für die Flags, die Sie mit anderen Flags verwenden können. Beispielsweise können Sie die Flags D3DFVF \_ XYZ und D3DFVF \_ XYZRHW nicht zusammen verwenden, da dies darauf hindeutet, dass Ihre Anwendung die Position eines Scheitelpunkts mit nicht transformierten und transformierten Scheitelpunkten beschreibt.

Um die indizierte Vertexmischung zu verwenden, sollte das UBYTE4-Flag D3DFVF \_ LASTBETA \_ am Ende der FVF-Deklaration angezeigt werden. Das Vorhandensein dieses Flags gibt an, dass die fünfte Mischungsgewichtung als DWORD anstelle von float behandelt wird. Weitere Informationen finden Sie unter [Indexed Vertex Blending (Direct3D 9) .](indexed-vertex-blending.md)

Die folgenden Codebeispiele zeigen den Unterschied zwischen einem FVF-Code, der das UBYTE4-Flag D3DFVF \_ LASTBETA \_ verwendet, und einem, der nicht verwendet wird. Das Flag D3DFVF \_ XYZB3 ist vorhanden, wenn vier Blendingindizes verwendet werden, da Sie immer die Summe der ersten drei Indizes von der Zahl 1 subtrahieren, um den vierten zu erhalten (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



Die unten definierte FVF verwendet das Flag D3DFVF \_ LAST \_ UBYTE4.


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexdeklaration](vertex-declaration.md)
</dt> </dl>

 

 
