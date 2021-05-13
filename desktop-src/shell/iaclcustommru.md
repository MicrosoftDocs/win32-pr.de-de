---
description: Macht Methoden verfügbar, die verwendet werden, um eine LISTE der zuletzt verwendeten (MRU) für ein AutoVervollständigen-Objekt zu initialisieren.
title: IACLCustomMRU-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: f47a9df320da5c710c21ddbab83ca87b49c28e12
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842011"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="c12ab-103">IACLCustomMRU-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c12ab-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="c12ab-104">Macht Methoden verfügbar, die verwendet werden, um eine LISTE der zuletzt verwendeten (MRU) für ein AutoVervollständigen-Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c12ab-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="c12ab-105">Member</span><span class="sxs-lookup"><span data-stu-id="c12ab-105">Members</span></span>

<span data-ttu-id="c12ab-106">Die **IACLCustomMRU-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="c12ab-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c12ab-107">**IACLCustomMRU** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="c12ab-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="c12ab-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="c12ab-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c12ab-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="c12ab-109">Methods</span></span>

<span data-ttu-id="c12ab-110">Die **IACLCustomMRU-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c12ab-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="c12ab-111">Methode</span><span class="sxs-lookup"><span data-stu-id="c12ab-111">Method</span></span>                                             | <span data-ttu-id="c12ab-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c12ab-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="c12ab-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="c12ab-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="c12ab-114">Fügt der MRU-Liste einen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="c12ab-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="c12ab-115">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="c12ab-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="c12ab-116">Lädt eine Liste von Zeichenfolgen aus der Registrierung in die MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="c12ab-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c12ab-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c12ab-117">Requirements</span></span>



| <span data-ttu-id="c12ab-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c12ab-118">Requirement</span></span> | <span data-ttu-id="c12ab-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c12ab-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c12ab-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c12ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c12ab-121">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c12ab-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c12ab-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c12ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c12ab-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c12ab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
