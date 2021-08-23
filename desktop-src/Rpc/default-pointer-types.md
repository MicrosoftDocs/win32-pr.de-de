---
title: Standardzeigertypen
description: Zeiger müssen keine explizite Attributbeschreibung aufweisen. Wenn kein explizites Attribut angegeben wird, verwendet der MIDL-Compiler ein Standardzeigerattribut.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3020f17af6e24778c0fa5090009650f3c0832df528ba148e0a6a91928dd1dc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930977"
---
# <a name="default-pointer-types"></a>Standardzeigertypen

Zeiger müssen keine explizite Attributbeschreibung aufweisen. Wenn kein explizites Attribut angegeben wird, verwendet der MIDL-Compiler ein Standardzeigerattribut.

Die Standardfälle für nicht attributierte Zeiger sind die folgenden:

-   Zeiger der obersten Ebene, die in Parameterlisten angezeigt werden, werden standardmäßig auf \[ [](/windows/desktop/Midl/ref) \] verweiszeigert.
-   Alle anderen Zeiger werden standardmäßig auf den Vom \[ [**\_ Zeigerstandardattribut**](/windows/desktop/Midl/pointer-default) angegebenen Typ \] festgelegt. Wenn kein \[ **\_ Zeigerstandardattribut** angegeben wird, verwenden \] diese Zeiger standardmäßig das \[ [**eindeutige**](/windows/desktop/Midl/unique) \] Attribut, wenn sich der MIDL-Compiler im [Microsoft-Erweiterungsmodus](microsoft-rpc-binding-handle-extensions.md) befindet, oder das \[ [**ptr-Attribut,**](/windows/desktop/Midl/ptr) \] wenn sich der MIDL-Compiler im DCE-kompatiblen Modus befindet.

Wenn eine Remoteprozedur einen Zeiger zurückgibt, muss der Rückgabewert ein \[ [**eindeutiger**](/windows/desktop/Midl/unique) \] oder vollständiger Zeiger \[ [**(ptr)**](/windows/desktop/Midl/ptr) \] sein.

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

### <a name="remarks"></a>Hinweise

Um ein eindeutiges Zeigerattributverhalten sicherzustellen, verwenden Sie beim Definieren eines Zeigers immer explizite Zeigerattribute.

Es wird empfohlen, **\[** ptr **\]** nur zu verwenden, wenn Zeigeraliasing erforderlich ist.

 

 