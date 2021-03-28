---
description: Enthält das Anwendungs Objekt der Auflistung der Ordner Elemente.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Folderitems. Application-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127840"
---
# <a name="folderitemsapplication-property"></a><span data-ttu-id="7e5fc-103">Folderitems. Application (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e5fc-103">FolderItems.Application property</span></span>

<span data-ttu-id="7e5fc-104">Enthält das **Anwendungs** Objekt der Auflistung der Ordner Elemente.</span><span class="sxs-lookup"><span data-stu-id="7e5fc-104">Contains the **Application** object of the folder items collection.</span></span>

<span data-ttu-id="7e5fc-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7e5fc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5fc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e5fc-106">Syntax</span></span>


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a><span data-ttu-id="7e5fc-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e5fc-107">Property value</span></span>

<span data-ttu-id="7e5fc-108">Ein Objekt Verweis auf das Anwendungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="7e5fc-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e5fc-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e5fc-109">Remarks</span></span>

<span data-ttu-id="7e5fc-110">Die **Application** -Eigenschaft gibt das Automatisierungs Objekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="7e5fc-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="7e5fc-111">Andernfalls gibt diese Eigenschaft das Automatisierungs Objekt des Webbrowser-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="7e5fc-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="7e5fc-112">Verwenden Sie diese Eigenschaft mit den Befehlen SET **und "** **Set** " oder mit dem Befehl " **GetObject** ", um eine Instanz der Windows Internet Explorer-Anwendung zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7e5fc-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e5fc-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7e5fc-113">Requirements</span></span>



| <span data-ttu-id="7e5fc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e5fc-114">Requirement</span></span> | <span data-ttu-id="7e5fc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7e5fc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e5fc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e5fc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7e5fc-117">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e5fc-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7e5fc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e5fc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7e5fc-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e5fc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e5fc-120">Header</span><span class="sxs-lookup"><span data-stu-id="7e5fc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e5fc-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e5fc-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7e5fc-122">IDL</span><span class="sxs-lookup"><span data-stu-id="7e5fc-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e5fc-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e5fc-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7e5fc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7e5fc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e5fc-125"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7e5fc-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




