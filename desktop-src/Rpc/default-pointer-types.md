---
title: Standard Zeiger Typen
description: Es ist nicht erforderlich, dass Zeiger über eine explizite Attribut Beschreibung verfügen. Wenn kein explizites Attribut bereitgestellt wird, verwendet der Mittell-Compiler ein Standard Zeiger Attribut.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039305"
---
# <a name="default-pointer-types"></a>Standard Zeiger Typen

Es ist nicht erforderlich, dass Zeiger über eine explizite Attribut Beschreibung verfügen. Wenn kein explizites Attribut bereitgestellt wird, verwendet der Mittell-Compiler ein Standard Zeiger Attribut.

Die Standardfälle für nicht attributierte Zeiger lauten wie folgt:

-   Zeiger der obersten Ebene, die in Parameterlisten angezeigt werden, werden standardmäßig als Verweis \[ [](/windows/desktop/Midl/ref) \] Zeiger angezeigt.
-   Alle anderen Zeiger werden standardmäßig auf den Typ festgelegt, der vom \[ [**Zeiger \_ Standard**](/windows/desktop/Midl/pointer-default) Attribut angegeben wird \] . Wenn kein \[ **Zeiger- \_ Standard** \] Attribut angegeben wird, werden diese Zeiger standardmäßig auf das Unique-Attribut fest, \[ [](/windows/desktop/Midl/unique) \] Wenn sich der mittlerer l-Compiler im Microsoft- [Erweiterungs](microsoft-rpc-binding-handle-extensions.md) Modus befindet, oder das \[ [**ptr**](/windows/desktop/Midl/ptr) \] -Attribut, wenn sich der Mittelwert Compiler im DCE-kompatiblen Modus befindet.

Wenn eine Remote Prozedur einen Zeiger zurückgibt, muss der Rückgabewert ein eindeutiger \[ [](/windows/desktop/Midl/unique) \] oder vollständiger ( \[ [**ptr**](/windows/desktop/Midl/ptr) - \] ) Zeiger sein.

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a>Bemerkungen

Verwenden Sie beim Definieren eines Zeigers immer explizite Zeiger Attribute, um ein eindeutiges Zeiger Attribut Verhalten zu gewährleisten.

Es wird empfohlen, **\[** ptr **\]** nur dann zu verwenden, wenn ein Zeiger Aliasing erforderlich ist.

 

 