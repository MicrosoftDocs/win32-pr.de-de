---
description: Macht Methoden verfügbar, die zum Initialisieren einer zuletzt verwendeten (MRU-) Liste für ein Objekt für die automatische Vervollständigung verwendet werden.
title: Iaclcustommru-Schnittstelle
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
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994623"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="06a12-103">Iaclcustommru-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="06a12-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="06a12-104">Macht Methoden verfügbar, die zum Initialisieren einer zuletzt verwendeten (MRU-) Liste für ein Objekt für die automatische Vervollständigung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06a12-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="06a12-105">Member</span><span class="sxs-lookup"><span data-stu-id="06a12-105">Members</span></span>

<span data-ttu-id="06a12-106">Die **iaclcustommru** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="06a12-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="06a12-107">**Iaclcustommru** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06a12-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="06a12-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="06a12-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="06a12-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="06a12-109">Methods</span></span>

<span data-ttu-id="06a12-110">Die **iaclcustommru** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="06a12-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="06a12-111">Methode</span><span class="sxs-lookup"><span data-stu-id="06a12-111">Method</span></span>                                             | <span data-ttu-id="06a12-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06a12-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="06a12-113">**Addmrustring**</span><span class="sxs-lookup"><span data-stu-id="06a12-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="06a12-114">Fügt der MRU-Liste einen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="06a12-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="06a12-115">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="06a12-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="06a12-116">Lädt eine Liste von Zeichen folgen aus der Registrierung in die MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="06a12-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06a12-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="06a12-117">Requirements</span></span>



| <span data-ttu-id="06a12-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06a12-118">Requirement</span></span> | <span data-ttu-id="06a12-119">Wert</span><span class="sxs-lookup"><span data-stu-id="06a12-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06a12-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06a12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06a12-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06a12-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="06a12-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06a12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06a12-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06a12-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
