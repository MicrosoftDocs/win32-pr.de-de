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
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="88dfc-103">Packen von Regeln für konstante Variablen</span><span class="sxs-lookup"><span data-stu-id="88dfc-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="88dfc-104">Verpackungs Regeln legen fest, wie eng Daten beim Speichern angeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="88dfc-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="88dfc-105">HLSL implementiert Verpackungs Regeln für vs-Ausgabedaten, GS-Eingabe-und-Ausgabedaten und PS-Eingabe-und-Ausgabedaten.</span><span class="sxs-lookup"><span data-stu-id="88dfc-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="88dfc-106">(Die Daten werden für vs-Eingaben nicht gepackt, da die IA-Phase keine Daten entpacken kann.)</span><span class="sxs-lookup"><span data-stu-id="88dfc-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="88dfc-107">HLSL-Verpackungs Regeln ähneln dem Ausführen eines **\# Pragma Pack 4** mit Visual Studio, das Daten in 4-Byte-Grenzen packt.</span><span class="sxs-lookup"><span data-stu-id="88dfc-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="88dfc-108">Außerdem packt HLSL Daten so, dass Sie keine 16-Byte-Grenze überschreiten.</span><span class="sxs-lookup"><span data-stu-id="88dfc-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="88dfc-109">Variablen werden in einem angegebenen vier-Komponenten-Vektor verpackt, bis die Variable eine Begrenzung von vier Vektoren überschreitet. die nächsten Variablen werden zum nächsten vier-Komponenten Vektor gerhütet.</span><span class="sxs-lookup"><span data-stu-id="88dfc-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="88dfc-110">Jede-Struktur zwingt, dass die nächste Variable beim nächsten vier-Komponenten-Vektor gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="88dfc-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="88dfc-111">Dadurch wird manchmal Auffüllung für Struktur Arrays generiert.</span><span class="sxs-lookup"><span data-stu-id="88dfc-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="88dfc-112">Die sich ergebende Größe einer beliebigen Struktur ist immer durch **sizeof**(*vier-Komponenten Vektor*) gleichmäßig teilbar.</span><span class="sxs-lookup"><span data-stu-id="88dfc-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="88dfc-113">Arrays werden standardmäßig nicht in HLSL gepackt.</span><span class="sxs-lookup"><span data-stu-id="88dfc-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="88dfc-114">Um zu vermeiden, dass der Shader den Alu-Overhead für Offset Berechnungen übernimmt, wird jedes Element in einem Array in einem Vektor mit vier Komponenten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="88dfc-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="88dfc-115">Beachten Sie, dass Sie das Packen von Arrays (und die Adressierungs Berechnungen) mithilfe von Umwandlungen erreichen können.</span><span class="sxs-lookup"><span data-stu-id="88dfc-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="88dfc-116">Im folgenden finden Sie Beispiele für Strukturen und ihre entsprechenden verpackten Größen (wenn ein **float1** 4 Bytes belegt):</span><span class="sxs-lookup"><span data-stu-id="88dfc-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


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



## <a name="more-aggressive-packing"></a><span data-ttu-id="88dfc-117">Aggressivere Verpackung</span><span class="sxs-lookup"><span data-stu-id="88dfc-117">More Aggressive Packing</span></span>

<span data-ttu-id="88dfc-118">Sie könnten ein Array aggressiver verpacken.</span><span class="sxs-lookup"><span data-stu-id="88dfc-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="88dfc-119">Beispielsweise ein Array von float-Variablen:</span><span class="sxs-lookup"><span data-stu-id="88dfc-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="88dfc-120">Sie können diese Option ohne Leerzeichen im Array wie folgt Verpacken:</span><span class="sxs-lookup"><span data-stu-id="88dfc-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="88dfc-121">Die strengere Verpackung ist ein Kompromiss und der Bedarf an zusätzlichen shaderanweisungen für die Adress Berechnung.</span><span class="sxs-lookup"><span data-stu-id="88dfc-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88dfc-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88dfc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88dfc-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="88dfc-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




