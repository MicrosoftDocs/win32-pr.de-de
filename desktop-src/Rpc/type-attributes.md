---
title: Typattribute
description: Remote Prozedur Aufruf (RPC) und die Attribute des Mittelwert Typs, die auf Typdeklarationen angewendet werden können.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858268"
---
# <a name="type-attributes"></a><span data-ttu-id="f3a1a-103">Typattribute</span><span class="sxs-lookup"><span data-stu-id="f3a1a-103">Type Attributes</span></span>

<span data-ttu-id="f3a1a-104">Typattribute sind die Mittelwert Attribute, die auf Typdeklarationen angewendet werden können:</span><span class="sxs-lookup"><span data-stu-id="f3a1a-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="f3a1a-105">**\[**[**bewältigen**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="f3a1a-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="f3a1a-106">**\[**[**Kontext \_ handle**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="f3a1a-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="f3a1a-107">**\[**[**\_Switchtyp**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="f3a1a-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="f3a1a-108">Zeiger-Typattribute</span><span class="sxs-lookup"><span data-stu-id="f3a1a-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="f3a1a-109">Das **\[ \_ SwitchType \]** -Attribut gibt den Typ eines Union-Diskriminators an.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="f3a1a-110">Dieses Attribut gilt nur für eine nicht gekapselte Union.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="f3a1a-111">Ein Kontext Handle ist ein Zeiger mit einem **\[ Kontext \_ handle \]** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="f3a1a-112">Das **\[ Kontext \_ handle \]** -Attribut ermöglicht es Ihnen, Prozeduren zu schreiben, die Zustandsinformationen zwischen Remote Prozedur aufrufen erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="f3a1a-113">Ein Kontext Handle mit einem Wert, der nicht NULL ist, stellt gespeicherten Kontext dar und dient zwei Zwecken:</span><span class="sxs-lookup"><span data-stu-id="f3a1a-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="f3a1a-114">Auf der Clientseite enthält Sie die Informationen, die von der RPC-Lauf Zeit Bibliothek benötigt werden, um den Aufruf an den Server weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="f3a1a-115">Auf der Serverseite dient sie als Handle für den aktiven Kontext.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="f3a1a-116">Das **\[** [**handle**](/windows/desktop/Midl/handle) - **\]** Attribut gibt an, dass ein Typ als benutzerdefiniertes (generisches) handle auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="f3a1a-117">Diese Funktion ermöglicht das Design von Handles, die für die Anwendung von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="f3a1a-118">Der Benutzer muss Bindungs-und unbindungs Routinen bereitstellen, um zwischen dem benutzerdefinierten Handlertyp und dem primitiven RPC-Handle-Handle **\_ t** zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="f3a1a-119">Ein Primitives Handle enthält Ziel Informationen, die für die RPC-Laufzeitbibliotheken von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="f3a1a-120">Ein benutzerdefiniertes Handle kann nur in einer Typdeklaration definiert werden, nicht in einer Funktionsdeklaration.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="f3a1a-121">Ein Parameter mit dem **\[ handle \]** -Attribut hat einen doppelten Zweck.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="f3a1a-122">Sie wird verwendet, um die Bindung für den Aufruf zu bestimmen, und Sie wird als normaler Daten Parameter an die aufgerufene Prozedur übertragen.</span><span class="sxs-lookup"><span data-stu-id="f3a1a-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 