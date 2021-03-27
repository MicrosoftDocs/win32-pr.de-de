---
title: Packen von Regeln für konstante Variablen
description: Verpackungs Regeln legen fest, wie eng Daten beim Speichern angeordnet werden können.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2020
ms.locfileid: "103724368"
---
# <a name="packing-rules-for-constant-variables"></a>Packen von Regeln für konstante Variablen

Verpackungs Regeln legen fest, wie eng Daten beim Speichern angeordnet werden können. HLSL implementiert Verpackungs Regeln für vs-Ausgabedaten, GS-Eingabe-und-Ausgabedaten und PS-Eingabe-und-Ausgabedaten. (Die Daten werden für vs-Eingaben nicht gepackt, da die IA-Phase keine Daten entpacken kann.)

HLSL-Verpackungs Regeln ähneln dem Ausführen eines **\# Pragma Pack 4** mit Visual Studio, das Daten in 4-Byte-Grenzen packt. Außerdem packt HLSL Daten so, dass Sie keine 16-Byte-Grenze überschreiten. Variablen werden in einem angegebenen vier-Komponenten-Vektor verpackt, bis die Variable eine Begrenzung von vier Vektoren überschreitet. die nächsten Variablen werden zum nächsten vier-Komponenten Vektor gerhütet.

Jede-Struktur zwingt, dass die nächste Variable beim nächsten vier-Komponenten-Vektor gestartet wird. Dadurch wird manchmal Auffüllung für Struktur Arrays generiert. Die sich ergebende Größe einer beliebigen Struktur ist immer durch **sizeof**(*vier-Komponenten Vektor*) gleichmäßig teilbar.

Arrays werden standardmäßig nicht in HLSL gepackt. Um zu vermeiden, dass der Shader den Alu-Overhead für Offset Berechnungen übernimmt, wird jedes Element in einem Array in einem Vektor mit vier Komponenten gespeichert. Beachten Sie, dass Sie das Packen von Arrays (und die Adressierungs Berechnungen) mithilfe von Umwandlungen erreichen können.

Im folgenden finden Sie Beispiele für Strukturen und ihre entsprechenden verpackten Größen (wenn ein **float1** 4 Bytes belegt):


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



## <a name="more-aggressive-packing"></a>Aggressivere Verpackung

Sie könnten ein Array aggressiver verpacken. Beispielsweise ein Array von float-Variablen:


```
float4 array[16];
```



Sie können diese Option ohne Leerzeichen im Array wie folgt Verpacken:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



Die strengere Verpackung ist ein Kompromiss und der Bedarf an zusätzlichen shaderanweisungen für die Adress Berechnung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




