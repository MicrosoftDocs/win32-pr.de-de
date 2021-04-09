---
title: Das size_is-Attribut
description: Das \ size \_ is \-Attribut ist einer ganzzahligen Konstante, einem Ausdruck oder einer Variablen zugeordnet, die die Zuordnungs Größe des Arrays angibt.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858308"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="26a35-104">Die \[ Größe \_ ist " \] Attribute".</span><span class="sxs-lookup"><span data-stu-id="26a35-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="26a35-105">Die \[ [Größe \_ ist](/windows/desktop/Midl/size-is) " \] Attribute" ist einer ganzzahligen Konstante, einem Ausdruck oder einer Variablen zugeordnet, die die Zuordnungs Größe des Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="26a35-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="26a35-106">Stellen Sie sich ein Zeichen Array vor, dessen Länge durch Benutzereingaben bestimmt wird:</span><span class="sxs-lookup"><span data-stu-id="26a35-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="26a35-107">Das Sternchen ( \* ), das den Platzhalter für die Variable Array Dimension markiert, ist optional.</span><span class="sxs-lookup"><span data-stu-id="26a35-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="26a35-108">Der Serverstub muss Arbeitsspeicher auf dem Server zuweisen, der dem Arbeitsspeicher auf dem Client für diesen Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="26a35-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="26a35-109">Die Variable, die die Größe angibt, muss immer mindestens ein \[ [in](/windows/desktop/Midl/in) - \] Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="26a35-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="26a35-110">Das **\[ in \]** direktionale Attribut ist erforderlich, damit der Size-Wert beim Eintrag für den Serverstub definiert wird.</span><span class="sxs-lookup"><span data-stu-id="26a35-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="26a35-111">Dieser Größen Wert enthält Informationen, die der Serverstub benötigt, um den Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="26a35-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="26a35-112">Der Size-Parameter kann sich auch \[ in, [out](/windows/desktop/Midl/out-idl)befinden \] .</span><span class="sxs-lookup"><span data-stu-id="26a35-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="26a35-113">Dies ist beispielsweise hilfreich, wenn das vom Client gesendete Array für die Daten, die der Server speichern muss, nicht groß genug ist.</span><span class="sxs-lookup"><span data-stu-id="26a35-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="26a35-114">Sie können einen **\[ in-, out \]** -size-Parameter verwenden, um die erforderliche Größe zurück an das Client Programm zu senden.</span><span class="sxs-lookup"><span data-stu-id="26a35-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26a35-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26a35-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26a35-116">Mehrere Ebenen von Zeigern</span><span class="sxs-lookup"><span data-stu-id="26a35-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 