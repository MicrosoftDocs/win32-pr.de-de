---
title: Das user_marshal-Attribut
description: Das \ User \_ Marshal \-Attribut ist ein Attribut vom Typ "ACF", das in der Syntax "\" \_ als \ darstellt.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Remote Prozedur Aufruf RPC, Attribute, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473805"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="69740-105">Das Mars-Attribut des Benutzers \_</span><span class="sxs-lookup"><span data-stu-id="69740-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="69740-106">Das \[ Attribut für den [Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal) \] ist ein Attribut vom Typ "ACF", das in der Syntax ähnlich ist \[ [ \_ als](/windows/desktop/Midl/represent-as) \] .</span><span class="sxs-lookup"><span data-stu-id="69740-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="69740-107">Wie beim IDL-Attribut bietet \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] eine effizientere Möglichkeit zum Mars Hallen von Daten in einem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="69740-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="69740-108">Als ACF-Attribut können Sie mithilfe von **\[ User \_ Marshal \]** benutzerdefinierte Datentypen Mars Hallen, die in der mittleren l unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="69740-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="69740-109">Jeder anwendungsspezifische Typ verfügt über einen entsprechenden transaktionablen Typ, der die Wire-Darstellung definiert.</span><span class="sxs-lookup"><span data-stu-id="69740-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="69740-110">Der anwendungsspezifische Typ kann ein einfacher, zusammengesetzter oder Zeigertyp sein.</span><span class="sxs-lookup"><span data-stu-id="69740-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="69740-111">Die Haupteinschränkung besteht darin, dass die Typinstanz eine festgelegte, klar definierte Speichergröße aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="69740-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="69740-112">Wenn die Größe Ihrer Typinstanz geändert werden muss, verwenden Sie ein Zeiger Feld anstelle eines konformen Arrays.</span><span class="sxs-lookup"><span data-stu-id="69740-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="69740-113">Alternativ können Sie einen Zeiger auf den änderbaren Typ definieren.</span><span class="sxs-lookup"><span data-stu-id="69740-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="69740-114">Wie beim Wire Marshal-Attribut stellen Sie Routinen für die Größenanpassung, das **\[ \_ Marshalling \]** , das Marshalling und das Freigeben von Durchläufen bereit.</span><span class="sxs-lookup"><span data-stu-id="69740-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="69740-115">In der folgenden Tabelle werden die vier vom Benutzer bereitgestellten Routine Namen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69740-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="69740-116">Der <type> ist der userm-*Typ* , der in der Typdefinition für den **\[ Benutzer- \_ Marshal \]** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="69740-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="69740-117">-Routine zurückgegebener Wert</span><span class="sxs-lookup"><span data-stu-id="69740-117">Routine</span></span>                                                            | <span data-ttu-id="69740-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69740-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="69740-119"><type>\_Usersize</span><span class="sxs-lookup"><span data-stu-id="69740-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="69740-120">Gibt die Größe des RPC-Daten Puffers vor dem Mars Hallen auf Client-oder Serverseite an.</span><span class="sxs-lookup"><span data-stu-id="69740-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="69740-121"><type>\_Usermarshal</span><span class="sxs-lookup"><span data-stu-id="69740-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="69740-122">Marshalls der Daten auf Client-oder Serverseite.</span><span class="sxs-lookup"><span data-stu-id="69740-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="69740-123"><type>\_Userunmarshal</span><span class="sxs-lookup"><span data-stu-id="69740-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="69740-124">Gibt die Daten auf der Client-oder Serverseite aus.</span><span class="sxs-lookup"><span data-stu-id="69740-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="69740-125"><type>\_Benutzer frei</span><span class="sxs-lookup"><span data-stu-id="69740-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="69740-126">Gibt die Daten auf der Serverseite frei.</span><span class="sxs-lookup"><span data-stu-id="69740-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="69740-127">Diese vom Benutzer bereitgestellten Routinen werden entweder von der Client-oder der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="69740-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="69740-128">Wenn der-Parameter \[ nur [in](/windows/desktop/Midl/in) ist \] , überträgt der Client an den Server.</span><span class="sxs-lookup"><span data-stu-id="69740-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="69740-129">Der Client benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ".</span><span class="sxs-lookup"><span data-stu-id="69740-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="69740-130">Der Server benötigt die Funktionen **<type> \_ userunmarshal** und **<type> \_ userfree** .</span><span class="sxs-lookup"><span data-stu-id="69740-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="69740-131">Bei einem reinen \[ [out](/windows/desktop/Midl/out-idl) \] -Parameter überträgt der Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="69740-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="69740-132">Der Server benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ", während der Client die **<type> \_ usermarshal** -Funktion benötigt.</span><span class="sxs-lookup"><span data-stu-id="69740-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69740-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69740-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69740-134">Das Wire \_ Marshal-Attribut</span><span class="sxs-lookup"><span data-stu-id="69740-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="69740-135">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_</span><span class="sxs-lookup"><span data-stu-id="69740-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="69740-136">Benutzer \_ Mars Hall</span><span class="sxs-lookup"><span data-stu-id="69740-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="69740-137">Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="69740-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="69740-138">**Ndrgetusermarshalinfo**</span><span class="sxs-lookup"><span data-stu-id="69740-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 