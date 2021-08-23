---
title: Komprimierungsregeln für konstante Variablen
description: Komprimierungsregeln bestimmen, wie eng Daten angeordnet werden können, wenn sie gespeichert werden.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49b10f6383344821c7659ac40b367a77e0421d33be68a374c59920a62d37697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120084"
---
# <a name="packing-rules-for-constant-variables"></a>Komprimierungsregeln für konstante Variablen

Komprimierungsregeln bestimmen, wie eng Daten angeordnet werden können, wenn sie gespeichert werden. HLSL implementiert Komprimierungsregeln für VS-Ausgabedaten, GS-Eingabe- und -Ausgabedaten sowie PS-Ein- und -Ausgabedaten. (Daten werden nicht für VS-Eingaben gepackt, da die IA-Phase keine Daten entpacken kann.)

HLSL-Komprimierungsregeln ähneln der Durchführung eines **\# Pragma packs 4** mit Visual Studio, das Daten in 4-Byte-Grenzen packt. Darüber hinaus packt HLSL Daten, sodass sie keine 16-Byte-Grenze überschreiten. Variablen werden in einen angegebenen Vektor mit vier Komponenten gepackt, bis die Variable eine Vier-Vektor-Grenze umgeht. die nächsten Variablen werden auf den nächsten Vektor mit vier Komponenten verschoben.

Jede Struktur erzwingt, dass die nächste Variable mit dem nächsten Vektor mit vier Komponenten beginnt. Dies generiert manchmal Auffüllung für Arrays von Strukturen. Die resultierende Größe einer beliebigen Struktur ist immer gleichmäßig durch **sizeof***(Vierkomponentenvektor)* teilbar.

Arrays sind standardmäßig nicht in HLSL gepackt. Um zu vermeiden, dass der Shader ALU-Mehraufwand für Offsetberechnungen übernimmt, wird jedes Element in einem Array in einem Vektor mit vier Komponenten gespeichert. Beachten Sie, dass Sie das Packen für Arrays erreichen können (und die Adressierungsberechnungen verursachen), indem Sie die Umwandlung verwenden.

Im Folgenden sind Beispiele für Strukturen und deren entsprechende gepackte Größen aufgeführt (mit der Angegebenen: **float1** belegt 4 Bytes):


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a>Aggressivere Komprimierung

Sie könnten ein Array aggressiver packen. Bei einem Array von float-Variablen:


```
float4 array[16];
```



Sie können es wie folgt packen, ohne Leerzeichen im Array zu verwenden:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



Die strengere Komprimierung ist ein Trade off im Vergleich zur Notwendigkeit zusätzlicher Shaderanweisungen für die Adressberechnung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




