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
# <a name="default-pointer-types"></a><span data-ttu-id="a6669-104">Standard Zeiger Typen</span><span class="sxs-lookup"><span data-stu-id="a6669-104">Default Pointer Types</span></span>

<span data-ttu-id="a6669-105">Es ist nicht erforderlich, dass Zeiger über eine explizite Attribut Beschreibung verfügen.</span><span class="sxs-lookup"><span data-stu-id="a6669-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="a6669-106">Wenn kein explizites Attribut bereitgestellt wird, verwendet der Mittell-Compiler ein Standard Zeiger Attribut.</span><span class="sxs-lookup"><span data-stu-id="a6669-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="a6669-107">Die Standardfälle für nicht attributierte Zeiger lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a6669-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="a6669-108">Zeiger der obersten Ebene, die in Parameterlisten angezeigt werden, werden standardmäßig als Verweis \[ [](/windows/desktop/Midl/ref) \] Zeiger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6669-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="a6669-109">Alle anderen Zeiger werden standardmäßig auf den Typ festgelegt, der vom \[ [**Zeiger \_ Standard**](/windows/desktop/Midl/pointer-default) Attribut angegeben wird \] .</span><span class="sxs-lookup"><span data-stu-id="a6669-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="a6669-110">Wenn kein \[ **Zeiger- \_ Standard** \] Attribut angegeben wird, werden diese Zeiger standardmäßig auf das Unique-Attribut fest, \[ [](/windows/desktop/Midl/unique) \] Wenn sich der mittlerer l-Compiler im Microsoft- [Erweiterungs](microsoft-rpc-binding-handle-extensions.md) Modus befindet, oder das \[ [**ptr**](/windows/desktop/Midl/ptr) \] -Attribut, wenn sich der Mittelwert Compiler im DCE-kompatiblen Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="a6669-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="a6669-111">Wenn eine Remote Prozedur einen Zeiger zurückgibt, muss der Rückgabewert ein eindeutiger \[ [](/windows/desktop/Midl/unique) \] oder vollständiger ( \[ [**ptr**](/windows/desktop/Midl/ptr) - \] ) Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="a6669-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="a6669-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6669-112">Remarks</span></span>

<span data-ttu-id="a6669-113">Verwenden Sie beim Definieren eines Zeigers immer explizite Zeiger Attribute, um ein eindeutiges Zeiger Attribut Verhalten zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="a6669-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="a6669-114">Es wird empfohlen, **\[** ptr **\]** nur dann zu verwenden, wenn ein Zeiger Aliasing erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a6669-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 