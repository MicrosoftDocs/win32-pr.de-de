---
title: Einschränkungen der Schnittstellenverwendung
description: Die aktuelle GPU-Hardware unterstützt zur Shaderlaufzeit keine unterschiedlichen Slotinformationen. Folglich können Schnittstellenverweise nicht innerhalb eines bedingten Ausdrucks wie einer if- oder switch-Anweisung geändert werden.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae44bbdb93ab2b3ffa0d09385c56b463192cc68c17e0454f9edd3326f722d29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672560"
---
# <a name="interface-usage-restrictions"></a>Einschränkungen der Schnittstellenverwendung

Die aktuelle GPU-Hardware unterstützt zur Shaderlaufzeit keine unterschiedlichen Slotinformationen. Folglich können Schnittstellenverweise nicht innerhalb eines bedingten Ausdrucks wie einer if- oder switch-Anweisung geändert werden.

Der folgende Shadercode veranschaulicht, wann diese Einschränkung auftritt und ein möglicher alternativer Ansatz.

Mit den folgenden Schnittstellendeklarationen:


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



Mit den folgenden Klassendeklarationen:


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



Ein Schnittstellenverweis kann nicht innerhalb des bedingten Ausdrucks geändert werden (eine if-Anweisung):


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



Angesichts der gleichen Schnittstellen- und Klassendeklarationen können Sie einen Index verwenden, um die gleiche Funktionalität zur Verfügung zu stellen und die erzwungene Schleifenaufrollung zu vermeiden.


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

[Dynamische Verknüpfung](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




