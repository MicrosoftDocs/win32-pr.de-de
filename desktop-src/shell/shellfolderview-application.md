---
description: Enthält das Anwendungs Objekt des-Objekts.
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Shellfolderview. Application-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ba57c407183179f580b5b616ad039c22e6fea66c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980432"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="8ca56-103">Shellfolderview. Application (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8ca56-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="8ca56-104">Enthält das Anwendungs Objekt des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8ca56-104">Contains the object's Application object.</span></span>

<span data-ttu-id="8ca56-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8ca56-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca56-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ca56-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="8ca56-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8ca56-107">Property value</span></span>

<span data-ttu-id="8ca56-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das Anwendungs Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="8ca56-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca56-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ca56-109">Remarks</span></span>

<span data-ttu-id="8ca56-110">Die **Application** -Eigenschaft gibt das Automatisierungs Objekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="8ca56-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="8ca56-111">Andernfalls gibt diese Eigenschaft das Automatisierungs Objekt des Webbrowser-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="8ca56-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="8ca56-112">Verwenden Sie diese Eigenschaft mit den Befehlen SET **und "** **Set** " oder mit dem Befehl " **GetObject** ", um eine Instanz der Windows Internet Explorer-Anwendung zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8ca56-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca56-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8ca56-113">Requirements</span></span>



| <span data-ttu-id="8ca56-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ca56-114">Requirement</span></span> | <span data-ttu-id="8ca56-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8ca56-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca56-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ca56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca56-117">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ca56-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ca56-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ca56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca56-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ca56-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ca56-120">Header</span><span class="sxs-lookup"><span data-stu-id="8ca56-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca56-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca56-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8ca56-122">IDL</span><span class="sxs-lookup"><span data-stu-id="8ca56-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ca56-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ca56-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8ca56-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca56-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ca56-125"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8ca56-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
