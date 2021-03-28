---
description: Enthält das Anwendungs Objekt des Ordners.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Folder. Application-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484038"
---
# <a name="folderapplication-property"></a><span data-ttu-id="9766a-103">Folder. Application (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9766a-103">Folder.Application property</span></span>

<span data-ttu-id="9766a-104">Enthält das Anwendungs Objekt des Ordners.</span><span class="sxs-lookup"><span data-stu-id="9766a-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="9766a-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9766a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9766a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9766a-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="9766a-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9766a-107">Property value</span></span>

<span data-ttu-id="9766a-108">Ein Objekt Verweis auf das Anwendungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="9766a-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9766a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9766a-109">Remarks</span></span>

<span data-ttu-id="9766a-110">Die **Application** -Eigenschaft gibt das Automatisierungs Objekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="9766a-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="9766a-111">Andernfalls gibt diese Eigenschaft das Automatisierungs Objekt des Webbrowser-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="9766a-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="9766a-112">Verwenden Sie diese Eigenschaft mit den Befehlen SET **und "** **Set** " oder mit dem Befehl " **GetObject** ", um eine Instanz der Internet Explorer-Anwendung zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9766a-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="9766a-113">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="9766a-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="9766a-114">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="9766a-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="9766a-115">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9766a-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9766a-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9766a-116">Requirements</span></span>



| <span data-ttu-id="9766a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9766a-117">Requirement</span></span> | <span data-ttu-id="9766a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9766a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9766a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9766a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9766a-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9766a-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="9766a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9766a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9766a-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9766a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9766a-123">Header</span><span class="sxs-lookup"><span data-stu-id="9766a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9766a-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9766a-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9766a-125">IDL</span><span class="sxs-lookup"><span data-stu-id="9766a-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9766a-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9766a-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




