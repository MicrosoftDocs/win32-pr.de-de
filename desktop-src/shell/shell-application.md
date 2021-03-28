---
description: Enthält das Anwendungs Objekt des-Objekts.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Shell. Application-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a9f9bd7fa28d2b277adfd8038c10c97efe16f51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868688"
---
# <a name="shellapplication-property"></a><span data-ttu-id="b0f18-103">Shell. Application (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b0f18-103">Shell.Application property</span></span>

<span data-ttu-id="b0f18-104">Enthält das Anwendungs Objekt des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0f18-104">Contains the object's Application object.</span></span>

<span data-ttu-id="b0f18-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b0f18-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f18-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0f18-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="b0f18-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b0f18-107">Property value</span></span>

<span data-ttu-id="b0f18-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das Anwendungs Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="b0f18-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f18-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0f18-109">Remarks</span></span>

<span data-ttu-id="b0f18-110">Die **Application** -Eigenschaft gibt das Automatisierungs Objekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="b0f18-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="b0f18-111">Andernfalls gibt diese Eigenschaft das Automatisierungs Objekt des Webbrowser-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="b0f18-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="b0f18-112">Verwenden Sie diese Eigenschaft mit den Befehlen SET **und "** **Set** " oder mit dem Befehl " **GetObject** ", um eine Instanz der Windows Internet Explorer-Anwendung zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b0f18-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f18-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b0f18-113">Requirements</span></span>



| <span data-ttu-id="b0f18-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0f18-114">Requirement</span></span> | <span data-ttu-id="b0f18-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b0f18-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f18-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0f18-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f18-117">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0f18-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0f18-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0f18-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f18-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0f18-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b0f18-120">Header</span><span class="sxs-lookup"><span data-stu-id="b0f18-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0f18-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f18-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b0f18-122">IDL</span><span class="sxs-lookup"><span data-stu-id="b0f18-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0f18-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0f18-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b0f18-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b0f18-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0f18-125"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b0f18-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
