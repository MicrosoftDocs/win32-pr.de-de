---
description: Ein f-Code-Code beschreibt den Inhalt von Vertices, die in einem einzelnen Datenstrom verschachtelt werden.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Code der Fixed-Funktion (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346177"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Code der Fixed-Funktion (Direct3D 9)

Ein f-Code-Code beschreibt den Inhalt von Vertices, die in einem einzelnen Datenstrom verschachtelt werden. Im Allgemeinen werden die Daten angegeben, die von der Pipeline für die Verarbeitung fester Funktionen verarbeitet werden sollen. Dies ist eine Scheitelpunkt Deklaration im älteren Stil. um den aktuellen Scheitelpunkt Deklarations Stil anzuzeigen, finden Sie weitere Informationen unter [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Direct3D-Anwendungen können Modell Vertices auf verschiedene Weise definieren. Die Unterstützung von flexiblen Scheitelpunkt Definitionen, auch als flexible Scheitelpunkt Formate oder flexible Scheitelpunkt Formate bezeichnet, ermöglicht es der Anwendung, nur die zu verwendenden Scheitelpunkt Komponenten zu verwenden, sodass die Komponenten, die nicht verwendet werden, ausgeschlossen werden. Wenn Sie nur die erforderlichen Scheitelpunkt Komponenten verwenden, kann Ihre Anwendung Arbeitsspeicher einsparen und die Verarbeitungs Bandbreite minimieren, die zum Rendering von Modellen erforderlich ist. Sie beschreiben, wie die Vertices formatiert werden, indem Sie eine Kombination aus [D3DFVF](d3dfvf.md) Codes verwenden.

Die Spezifikation "f VF" umfasst Formate für die Punktgröße, die durch D3DFVF \_ Psize angegeben werden. Diese Größe wird in Kamera Raumeinheiten für nicht transformierte und beleuchtete Scheitel Punkte (TL) und in Einheiten für die Speichereinheiten für TL-Scheitel Punkte ausgedrückt.

Die Renderingmethoden der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle stellen C++-Anwendungen Methoden bereit, die eine Kombination dieser Flags akzeptieren, und verwenden Sie, um zu bestimmen, wie primitive gerendert werden. Im Grunde weisen diese Flags das System an, welche Scheitelpunkt Komponenten Positions-, Vertex-Mischungs Gewichtungen, normal, Farben und die Anzahl und das Format von Texturkoordinaten verwenden. Ihre Anwendung verwendet und, indirekt, welche Teile der Renderingpipeline, auf die Direct3D angewendet werden soll. Außerdem kommuniziert das vorhanden sein oder Fehlen eines bestimmten Scheitelpunkt Formatflags mit dem System, welche vertexkomponentenfelder im Arbeitsspeicher vorhanden sind und welche ausgelassen wurden.

Um die Geräte Einschränkungen zu ermitteln, können Sie ein Gerät nach den Werten von D3DFVFCAPS \_ donotstripelements und D3DFVFCAPS \_ texcoordrattmask im fvfcaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)Abfragen.

Texturkoordinaten können in unterschiedlichen Formaten deklariert werden, sodass Texturen mit nur einer Koordinate oder bis zu vier Texturkoordinaten (bei 2D-projizierten Texturkoordinaten) adressiert werden können. Weitere Informationen finden Sie unter [Texturkoordinaten Formate (Direct3D 9)](texture-coordinate-formats.md). Verwenden Sie den [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) -Satz von Makros, um Bitmuster zu erstellen, mit denen die Texturkoordinaten Formate identifiziert werden, die im Vertex-Format verwendet werden.

Jede-Komponente wird von keiner Anwendung verwendet. Die normalen Felder "gegenseitige homogene W" und "Scheitelpunkt" schließen sich gegenseitig aus. Die meisten Anwendungen versuchen auch, alle acht Sätze von Texturkoordinaten zu verwenden, aber Direct3D hat diese Kapazität. Es gibt mehrere Einschränkungen hinsichtlich der Flags, die Sie mit anderen Flags verwenden können. Beispielsweise können Sie die \_ Flags D3DFVF XYZ und D3DFVF \_ xyzrhw nicht gleichzeitig verwenden, da dies darauf hindeuten würde, dass Ihre Anwendung die Position eines Scheitel Punkts mit nicht transformierten und transformierten Vertices beschreibt.

Um indizierte vertexmischungs Zeichen zu verwenden, sollte das D3DFVF \_ lastbeta \_ UBYTE4-Flag am Ende der FVF-Deklaration angezeigt werden. Das vorhanden sein dieses Flags gibt an, dass das fünfte Mischungs Gewicht als DWORD und nicht als float behandelt wird. Weitere Informationen finden Sie unter [indiziertes Vertex-Blending (Direct3D 9)](indexed-vertex-blending.md).

Die folgenden Codebeispiele zeigen den Unterschied zwischen einem f-Code, der das D3DFVF \_ lastbeta \_ UBYTE4-Flag verwendet, und einem, das nicht ist. Das Flag D3DFVF \_ XYZB3 ist vorhanden, wenn vier Mischungs Indizes verwendet werden, weil Sie immer die Summe der ersten drei Werte von der Zahl 1 subtrahieren, um die vierte zu erhalten (Blend ₄ = 1-(Blend ₁ + Blend-Taste + Blend ₃)).


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



Die unten definierte "f VF" verwendet das Flag "D3DFVF \_ Last \_ UBYTE4".


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

[Vertex-Deklaration](vertex-declaration.md)
</dt> </dl>

 

 
