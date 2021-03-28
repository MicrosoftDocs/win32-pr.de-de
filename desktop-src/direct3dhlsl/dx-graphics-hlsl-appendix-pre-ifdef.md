---
title: " ifdef-und ifndef-Direktiven"
description: Präprozessordirektiven, die bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef-und ifndef-Direktiven HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037990"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="4991d-104">\#ifdef-und \# ifndef-Direktiven</span><span class="sxs-lookup"><span data-stu-id="4991d-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="4991d-105">Präprozessordirektiven, die bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4991d-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="4991d-106">\#ifdef- *Bezeichner* ...</span><span class="sxs-lookup"><span data-stu-id="4991d-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="4991d-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="4991d-107">\#endif</span></span>                   |
| <span data-ttu-id="4991d-108">\#ifndef- *Bezeichner* ...</span><span class="sxs-lookup"><span data-stu-id="4991d-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="4991d-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="4991d-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="4991d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4991d-110">Parameters</span></span>



| <span data-ttu-id="4991d-111">Element</span><span class="sxs-lookup"><span data-stu-id="4991d-111">Item</span></span>                                                                              | <span data-ttu-id="4991d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4991d-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4991d-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*</span><span class="sxs-lookup"><span data-stu-id="4991d-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="4991d-114">Der Bezeichner der zu überprüfen Konstanten oder Makros.</span><span class="sxs-lookup"><span data-stu-id="4991d-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4991d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4991d-115">Remarks</span></span>

<span data-ttu-id="4991d-116">Sie können die \# ifdef-und \# ifndef-Direktiven überall [ \# ](dx-graphics-hlsl-appendix-pre-if.md) dort verwenden, wo verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4991d-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="4991d-117">Die \# ifdef-Anweisung entspricht der-Direktive.</span><span class="sxs-lookup"><span data-stu-id="4991d-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="4991d-118">Diese Direktiven überprüfen nur das vorhanden sein oder Fehlen von [ \# bezeichlen](dx-graphics-hlsl-appendix-pre-define.md) , die mithilfe der define-Direktive definiert wurden, nicht für Bezeichner, die im C-oder C++-Quellcode deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="4991d-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="4991d-119">Diese Anweisungen werden nur bereitgestellt, um die Kompatibilität mit früheren Versionen der Sprache zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="4991d-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="4991d-120">Die Verwendung des [definierten](dx-graphics-hlsl-appendix-pre-if.md) Operators mit der \# if-Direktive wird bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="4991d-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="4991d-121">Die \# ifndef-Direktive prüft das Gegenteil der von \# ifdef geprüften Bedingung.</span><span class="sxs-lookup"><span data-stu-id="4991d-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="4991d-122">Wenn der Bezeichner nicht definiert ist, ist die Bedingung "true" (ungleich 0); Andernfalls ist die Bedingung "false" (null).</span><span class="sxs-lookup"><span data-stu-id="4991d-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="4991d-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4991d-123">Examples</span></span>

<span data-ttu-id="4991d-124">Der Bezeichner kann von der Befehlszeile mithilfe der Option /D- übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4991d-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="4991d-125">Bis zu 30 Makros können mit /D angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4991d-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="4991d-126">Dies ist hilfreich, wenn überprüft werden soll, ob eine Definition vorhanden ist, da diese von der Befehlszeile übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4991d-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="4991d-127">Im folgenden Beispiel wird dieses Verhalten verwendet, um zu bestimmen, ob eine Anwendung im Testmodus ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4991d-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="4991d-128">Bei der Kompilierung mit dem folgenden Befehl wird "PROG. cpp" im Testmodus kompiliert. Andernfalls wird es im abschließenden Modus kompiliert.</span><span class="sxs-lookup"><span data-stu-id="4991d-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="4991d-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4991d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4991d-130">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4991d-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="4991d-131">\#Wenn,)</span><span class="sxs-lookup"><span data-stu-id="4991d-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





