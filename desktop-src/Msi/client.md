---
description: Das Client-Objekt stellt eine Beziehung zwischen einer Komponente und einem Client Produkt dar.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Clientobjekt.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361933"
---
# <a name="client-object"></a><span data-ttu-id="5d0ba-103">Clientobjekt.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-103">Client object</span></span>

<span data-ttu-id="5d0ba-104">Das Client-Objekt stellt eine Beziehung zwischen einer Komponente und einem Client Produkt dar.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="5d0ba-105">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="5d0ba-106">Dieses Objekt ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="5d0ba-107">Member</span><span class="sxs-lookup"><span data-stu-id="5d0ba-107">Members</span></span>

<span data-ttu-id="5d0ba-108">Das **Client** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5d0ba-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="5d0ba-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d0ba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d0ba-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d0ba-110">Properties</span></span>

<span data-ttu-id="5d0ba-111">Das **Client** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="5d0ba-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5d0ba-112">Property</span></span>                                                 | <span data-ttu-id="5d0ba-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d0ba-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="5d0ba-114">**Componentcode**</span><span class="sxs-lookup"><span data-stu-id="5d0ba-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="5d0ba-115">Der Komponenten Code der betreffenden Komponente.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="5d0ba-116">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="5d0ba-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="5d0ba-117">Der Kontext des Produkts.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="5d0ba-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="5d0ba-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="5d0ba-119">Das Client Produkt der betreffenden Komponente.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="5d0ba-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="5d0ba-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="5d0ba-121">Die Benutzer-SID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="5d0ba-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d0ba-122">Requirements</span></span>



| <span data-ttu-id="5d0ba-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d0ba-123">Requirement</span></span> | <span data-ttu-id="5d0ba-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5d0ba-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0ba-125">Version</span><span class="sxs-lookup"><span data-stu-id="5d0ba-125">Version</span></span><br/> | <span data-ttu-id="5d0ba-126">Windows Installer 5,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5d0ba-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="5d0ba-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5d0ba-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d0ba-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d0ba-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d0ba-129">IID</span><span class="sxs-lookup"><span data-stu-id="5d0ba-129">IID</span></span><br/>     | <span data-ttu-id="5d0ba-130">IID \_ IClient ist definiert als 000c1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d0ba-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5d0ba-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d0ba-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0ba-132">Verwenden der Automatisierungsschnittstelle</span><span class="sxs-lookup"><span data-stu-id="5d0ba-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="5d0ba-133">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5d0ba-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




