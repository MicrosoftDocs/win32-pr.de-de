---
title: Union-Schlüsselwort (RPC)
description: Unions benötigen besondere Mittel Schlüssel Schlüsselwörter zur Unterstützung ihrer Verwendung mit Remote Prozedur Aufruf (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315242"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="4faa8-103">Union-Schlüsselwort (RPC)</span><span class="sxs-lookup"><span data-stu-id="4faa8-103">union keyword (RPC)</span></span>

<span data-ttu-id="4faa8-104">Einige Features der Programmiersprache C (z. b. Unions) erfordern spezielle Mittel Schlüssel Schlüsselwörter, um ihre Verwendung in Remote Prozedur aufrufen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4faa8-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="4faa8-105">Eine Union in der Programmiersprache C ist eine Variable, die Objekte mit unterschiedlichen Typen und Größen enthält.</span><span class="sxs-lookup"><span data-stu-id="4faa8-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="4faa8-106">Der Entwickler erstellt in der Regel eine Variable, um die in der Union gespeicherten Typen nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4faa8-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="4faa8-107">Um ordnungsgemäß in einer verteilten Umgebung auszuführen, muss die Variable, die den Typ der Union oder die *Diskriminante* angibt, auch für den Remote Computer verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="4faa8-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="4faa8-108">In der Mitte werden der \[ [**\_ Switchtyp**](/windows/desktop/Midl/switch-type) \] und die \[ [**Switch \_ is**](/windows/desktop/Midl/switch-is) - \] Schlüsselwörter zur Identifizierung des diskriminatentyps und des Namens angegeben</span><span class="sxs-lookup"><span data-stu-id="4faa8-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="4faa8-109">Bei der Verwendung von "Mittel l" muss die Diskriminante mit der Union auf zwei Arten übertragen werden:</span><span class="sxs-lookup"><span data-stu-id="4faa8-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="4faa8-110">Die Union und die Diskriminante müssen als Parameter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4faa8-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="4faa8-111">Die Union und die Diskriminante müssen in einer Struktur verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="4faa8-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="4faa8-112">Zwei grundlegende Typen von Unterscheidungs-Unions werden von mittlerer l bereitgestellt: [**nicht gekapselte \_ Union**](/windows/desktop/Midl/nonencapsulated-unions) und [**gekapselte \_**](/windows/desktop/Midl/encapsulated-unions)</span><span class="sxs-lookup"><span data-stu-id="4faa8-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="4faa8-113">Die Diskriminante einer nicht gekapselten Union ist ein weiterer Parameter, wenn die Union ein Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="4faa8-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="4faa8-114">Es ist ein weiteres Feld, wenn die Union ein Feld einer Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="4faa8-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="4faa8-115">Die Definition einer gekapselten Union wird in eine Struktur Definition umgewandelt, deren erstes Feld die Diskriminante ist und deren zweite und letzte Felder die Union darstellen.</span><span class="sxs-lookup"><span data-stu-id="4faa8-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="4faa8-116">Im folgenden Beispiel wird veranschaulicht, wie die Union und die Diskriminante als Parameter bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="4faa8-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="4faa8-117">Die Union im vorangehenden Beispiel kann einen einzelnen Wert enthalten: " **Short**", " **float**" oder " **char**".</span><span class="sxs-lookup"><span data-stu-id="4faa8-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="4faa8-118">Die Typdefinition für die Union enthält das Attribut "Mittelwert **Switch \_ Type** ", das den Typ des Diskriminanten angibt.</span><span class="sxs-lookup"><span data-stu-id="4faa8-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="4faa8-119">Hier \[ gibt Switch \_ Type (Short) \] an, dass der diskriminant vom Typ **Short** ist.</span><span class="sxs-lookup"><span data-stu-id="4faa8-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="4faa8-120">Der Switch muss ein ganzzahliger Typ sein.</span><span class="sxs-lookup"><span data-stu-id="4faa8-120">The switch must be an integer type.</span></span>

<span data-ttu-id="4faa8-121">Wenn die Union ein Member einer Struktur ist, muss die Diskriminante ein Member derselben Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="4faa8-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="4faa8-122">Wenn die Union ein Parameter ist, muss der diskriminant ein weiterer Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="4faa8-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="4faa8-123">Der Prototyp für die Funktion **unionparamproc** im vorangehenden Beispiel zeigt den Diskriminanten *sutype* als letzten Parameter des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="4faa8-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="4faa8-124">(Die Diskriminante kann an einer beliebigen Position im-Befehl angezeigt werden.) Der im Switch angegebene Typ des Parameters muss dem Typ entsprechen, der im **\[ Switch \_ Type \]** -Attribut angegeben **\[ \_ ist \]** .</span><span class="sxs-lookup"><span data-stu-id="4faa8-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="4faa8-125">Im folgenden Beispiel wird die Verwendung einer einzelnen-Struktur veranschaulicht, die den Diskriminanten mit der Union verpackt:</span><span class="sxs-lookup"><span data-stu-id="4faa8-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="4faa8-126">Der Microsoft RPC-Mittell-Compiler ermöglicht Union-Deklarationen außerhalb von [**typedef**](/windows/desktop/Midl/typedef) -Konstrukten.</span><span class="sxs-lookup"><span data-stu-id="4faa8-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="4faa8-127">Diese Funktion ist eine Erweiterung der DCE-IDL.</span><span class="sxs-lookup"><span data-stu-id="4faa8-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="4faa8-128">Weitere Informationen finden Sie unter [**Union**](/windows/desktop/Midl/union).</span><span class="sxs-lookup"><span data-stu-id="4faa8-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 