---
title: Das Wire_marshal-Attribut
description: Das Attribut \ Wire \_ Marshal \ ist ein Attribut vom Typ IDL, das der Syntax in \ Übertragung \_ als \ ähnelt, bietet jedoch eine effizientere Möglichkeit zum Mars Hallen von Daten über ein Netzwerk.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- Remote Prozedur Aufruf RPC, Attribute, Wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390712"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="6617b-105">Das Wire \_ Marshal-Attribut</span><span class="sxs-lookup"><span data-stu-id="6617b-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="6617b-106">Das \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] -Attribut ist ein Attribut vom Typ IDL, das in der Syntax für die über \[ [Tragung \_ als](/windows/desktop/Midl/transmit-as)ähnlich ist \] , aber eine effizientere Möglichkeit zum Mars Hallen von Daten in einem Netzwerk bietet.</span><span class="sxs-lookup"><span data-stu-id="6617b-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="6617b-107">Sie verwenden das \[ **Wire \_ Marshal** - \] Attribut, um einen Datentyp anzugeben, der anstelle des anwendungsspezifischen Datentyps übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="6617b-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="6617b-108">Jeder anwendungsspezifische Typ verfügt über einen entsprechenden transaktionablen Typ, der die Wire-Darstellung definiert (die im Netzwerk verwendete Darstellung). Der anwendungsspezifische Typ muss nicht transaktierbar sein, aber es muss sich um einen Typ handeln, der von der Mittell erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6617b-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="6617b-109">Verwenden Sie zum Mars Hallen eines Typs, der in der mittleren l unbekannt ist, das ACF-Attribut \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="6617b-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="6617b-110">Der anwendungsspezifische Typ kann ein einfacher, zusammengesetzter oder Zeigertyp sein.</span><span class="sxs-lookup"><span data-stu-id="6617b-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="6617b-111">Die Haupteinschränkung besteht darin, dass die Typinstanz eine festgelegte, klar definierte Speichergröße aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="6617b-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="6617b-112">Wenn die Größe Ihrer Typinstanz geändert werden muss, verwenden Sie ein Zeiger Feld anstelle eines konformen Arrays.</span><span class="sxs-lookup"><span data-stu-id="6617b-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="6617b-113">Alternativ können Sie einen Zeiger auf den änderbaren Typ definieren.</span><span class="sxs-lookup"><span data-stu-id="6617b-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="6617b-114">Sie müssen die Routinen für die Größenanpassung, das Marshalling und das Marshalling der Daten sowie das Freigeben des zugeordneten Speichers bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6617b-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="6617b-115">In der folgenden Tabelle werden die vier vom Benutzer bereitgestellten Routine Namen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6617b-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="6617b-116">Der <type> ist der in der \[ Typdefinition des **Wire \_ Marshal** angegebene userm-Typ \] .</span><span class="sxs-lookup"><span data-stu-id="6617b-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="6617b-117">-Routine zurückgegebener Wert</span><span class="sxs-lookup"><span data-stu-id="6617b-117">Routine</span></span>                                                            | <span data-ttu-id="6617b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6617b-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="6617b-119"><type>\_Usersize</span><span class="sxs-lookup"><span data-stu-id="6617b-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="6617b-120">Gibt die Größe des RPC-Daten Puffers vor dem Mars Hallen auf Client-oder Serverseite an.</span><span class="sxs-lookup"><span data-stu-id="6617b-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="6617b-121"><type>\_Usermarshal</span><span class="sxs-lookup"><span data-stu-id="6617b-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="6617b-122">Marshalls der Daten auf Client-oder Serverseite.</span><span class="sxs-lookup"><span data-stu-id="6617b-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="6617b-123"><type>\_Userunmarshal</span><span class="sxs-lookup"><span data-stu-id="6617b-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="6617b-124">Gibt die Daten auf der Client-oder Serverseite aus.</span><span class="sxs-lookup"><span data-stu-id="6617b-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="6617b-125"><type>\_Benutzer frei</span><span class="sxs-lookup"><span data-stu-id="6617b-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="6617b-126">Gibt die Daten auf der Serverseite frei.</span><span class="sxs-lookup"><span data-stu-id="6617b-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="6617b-127">Diese vom Programmierer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6617b-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="6617b-128">Wenn der-Parameter \[ nur [in](/windows/desktop/Midl/in) ist \] , überträgt der Client an den Server.</span><span class="sxs-lookup"><span data-stu-id="6617b-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="6617b-129">Der Client benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ".</span><span class="sxs-lookup"><span data-stu-id="6617b-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="6617b-130">Der Server benötigt die **<type> \_ userunmarshal**-und **<type> \_ userfree** -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6617b-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="6617b-131">Bei einem reinen \[ [out](/windows/desktop/Midl/out-idl) \] -Parameter überträgt der Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="6617b-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="6617b-132">Der Server benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ", während der Client die **<type> \_ usermarshal** -Funktion benötigt.</span><span class="sxs-lookup"><span data-stu-id="6617b-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6617b-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6617b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6617b-134">Das Mars-Attribut des Benutzers \_</span><span class="sxs-lookup"><span data-stu-id="6617b-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="6617b-135">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="6617b-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="6617b-136">Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="6617b-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="6617b-137">Benutzer \_ Mars Hall</span><span class="sxs-lookup"><span data-stu-id="6617b-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="6617b-138">**Ndrgetusermarshalinfo**</span><span class="sxs-lookup"><span data-stu-id="6617b-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 