---
title: Schnittstellen Header Attribute
description: Fügen Sie diese Attribute in den Schnittstellen Header ein, um Informationen über die gesamte-Schnittstelle zu übermitteln.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL-Mittell, Attribute, Schnittstellen Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036768"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="e0d0c-104">Schnittstellen Header Attribute</span><span class="sxs-lookup"><span data-stu-id="e0d0c-104">Interface Header Attributes</span></span>

<span data-ttu-id="e0d0c-105">Fügen Sie diese Attribute in den Schnittstellen Header ein, um Informationen über die gesamte-Schnittstelle zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="e0d0c-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0d0c-106">Attribute</span></span>                                   | <span data-ttu-id="e0d0c-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e0d0c-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0d0c-108">**Async- \_ UUID**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="e0d0c-109">Weist den Mittel l-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="e0d0c-110">**UUID**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="e0d0c-111">Legt einen 128-Bit-Wert fest, der eine bestimmte Schnittstelle von allen anderen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="e0d0c-112">Der tatsächliche Wert kann eine GUID, eine CLSID oder eine IID darstellen.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="e0d0c-113">**nah**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-113">**local**</span></span>](local.md)                      | <span data-ttu-id="e0d0c-114">Weist den Mittel l-Compiler an, nur Header Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="e0d0c-115">Eine Schnittstelle muss entweder ein [**UUID**](uuid.md) -oder ein [**Lokales**](local.md) Attribut haben.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="e0d0c-116">**MS- \_ Union**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="e0d0c-117">Steuert die NDR-Ausrichtung von nicht gekapselten Unions.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="e0d0c-118">Verwenden Sie aus Gründen der Abwärtskompatibilität mit Schnittstellen, die auf mittlerer l 1,0 oder 2,0 basieren.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="e0d0c-119">**Objekt (object)**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-119">**object**</span></span>](object.md)                    | <span data-ttu-id="e0d0c-120">Identifiziert die-Schnittstelle als COM-Schnittstelle und leitet den Mittelwert Compiler an die Generierung von Proxy-/Stubcode anstelle von RPC-Client-und Serverstubs weiter.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="e0d0c-121">**version**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-121">**version**</span></span>](version.md)                  | <span data-ttu-id="e0d0c-122">Identifiziert eine bestimmte Version einer Schnittstelle in Fällen, in denen mehrere Versionen der Schnittstelle vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="e0d0c-123">Da com-Schnittstellen unveränderlich sind, können Sie das [**Versions**](version.md) Attribut nicht in einer [**Objekt**](object.md) Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="e0d0c-124">**Zeiger \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="e0d0c-125">Gibt den Standard Zeigertyp für alle Zeiger außer den in Parameterlisten enthaltenen Zeigern an.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="e0d0c-126">Der Standardtyp kann [**eindeutig**](unique.md), [**ref**](ref.md)oder [**ptr**](ptr.md)sein.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="e0d0c-127">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="e0d0c-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="e0d0c-128">Gibt einen statischen (bekannten) Endpunkt an, auf dem eine Serveranwendung auf Remote Prozedur Aufrufe lauschen soll.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="e0d0c-129">Siehe [Typbibliotheks Attribute](type-library-attributes.md) für Schnittstellen Attribute, z. b. [**Dual**](dual.md) und [**oleautomation**](oleautomation.md), die spezifisch für Schnittstellen sind, die in einer Bibliotheks Anweisung definiert sind oder auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e0d0c-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 




