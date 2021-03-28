---
title: Einschränkungen der Schnittstellen Verwendung
description: Die aktuelle GPU-Hardware unterstützt keine unterschiedlichen Slot-Informationen zur Shader-Laufzeit. Folglich können Schnittstellen Verweise nicht innerhalb eines bedingten Ausdrucks, z. b. einer if-oder Switch-Anweisung, geändert werden.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8825d192dcb874ce8b148c4ade5c579a55857311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309723"
---
# <a name="interface-usage-restrictions"></a><span data-ttu-id="4a3c5-104">Einschränkungen der Schnittstellen Verwendung</span><span class="sxs-lookup"><span data-stu-id="4a3c5-104">Interface Usage Restrictions</span></span>

<span data-ttu-id="4a3c5-105">Die aktuelle GPU-Hardware unterstützt keine unterschiedlichen Slot-Informationen zur Shader-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="4a3c5-105">Current GPU hardware does not support varying slot information at shader runtime.</span></span> <span data-ttu-id="4a3c5-106">Folglich können Schnittstellen Verweise nicht innerhalb eines bedingten Ausdrucks, z. b. einer if-oder Switch-Anweisung, geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4a3c5-106">As a consequence interface references cannot be modified within a conditional expression such as an if or switch statement.</span></span>

<span data-ttu-id="4a3c5-107">Der folgende Shader-Code veranschaulicht, wann diese Einschränkung stattfindet und einen möglichen alternativen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="4a3c5-107">The following shader code illustrates when this restriction will occur and a possible alternate approach.</span></span>

<span data-ttu-id="4a3c5-108">Unter Berücksichtigung der folgenden Schnittstellen Deklarationen:</span><span class="sxs-lookup"><span data-stu-id="4a3c5-108">Given the following interface declarations:</span></span>


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



<span data-ttu-id="4a3c5-109">Die folgenden Klassen Deklarationen werden angegeben:</span><span class="sxs-lookup"><span data-stu-id="4a3c5-109">Given the following class declarations:</span></span>


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



<span data-ttu-id="4a3c5-110">Ein Schnittstellen Verweis kann nicht innerhalb des bedingten Ausdrucks (einer if-Anweisung) geändert werden:</span><span class="sxs-lookup"><span data-stu-id="4a3c5-110">An interface reference cannot be modified within the conditional expression (an if statement):</span></span>


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



<span data-ttu-id="4a3c5-111">Mit derselben Schnittstelle und denselben Klassen Deklarationen können Sie einen Index verwenden, um die gleiche Funktionalität bereitzustellen und die erzwungene Schleife zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4a3c5-111">Given the same interface and class declarations, you could use an index to provide the same functionality and avoid the forced loop unroll.</span></span>


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a><span data-ttu-id="4a3c5-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a3c5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3c5-113">Dynamisches Verknüpfen</span><span class="sxs-lookup"><span data-stu-id="4a3c5-113">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




