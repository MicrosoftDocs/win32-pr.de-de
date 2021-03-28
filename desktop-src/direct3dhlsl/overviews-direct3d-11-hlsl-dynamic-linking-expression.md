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
# <a name="interface-usage-restrictions"></a>Einschränkungen der Schnittstellen Verwendung

Die aktuelle GPU-Hardware unterstützt keine unterschiedlichen Slot-Informationen zur Shader-Laufzeit. Folglich können Schnittstellen Verweise nicht innerhalb eines bedingten Ausdrucks, z. b. einer if-oder Switch-Anweisung, geändert werden.

Der folgende Shader-Code veranschaulicht, wann diese Einschränkung stattfindet und einen möglichen alternativen Ansatz.

Unter Berücksichtigung der folgenden Schnittstellen Deklarationen:


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



Die folgenden Klassen Deklarationen werden angegeben:


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



Ein Schnittstellen Verweis kann nicht innerhalb des bedingten Ausdrucks (einer if-Anweisung) geändert werden:


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



Mit derselben Schnittstelle und denselben Klassen Deklarationen können Sie einen Index verwenden, um die gleiche Funktionalität bereitzustellen und die erzwungene Schleife zu vermeiden.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamisches Verknüpfen](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




