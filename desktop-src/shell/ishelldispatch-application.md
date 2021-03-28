---
description: Enthält ein-Objekt, das eine Anwendung darstellt.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Ishelldispatch. Application-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527356"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="e0c36-103">Ishelldispatch. Application (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0c36-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="e0c36-104">Enthält ein-Objekt, das eine Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0c36-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="e0c36-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e0c36-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c36-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0c36-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="e0c36-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e0c36-107">Property value</span></span>

<span data-ttu-id="e0c36-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das Anwendungs Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="e0c36-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c36-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0c36-109">Remarks</span></span>

<span data-ttu-id="e0c36-110">Diese Eigenschaft wird implementiert, und der Zugriff erfolgt über die [**Shell. ejectpc**](shell-ejectpc.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e0c36-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="e0c36-111">Die **Application** -Eigenschaft gibt das Automatisierungs Objekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="e0c36-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="e0c36-112">Andernfalls gibt diese Eigenschaft das Automatisierungs Objekt des Webbrowser-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="e0c36-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="e0c36-113">Verwenden Sie diese Eigenschaft mit den Befehlen SET **und "** **Set** " oder mit dem Befehl " **GetObject** ", um eine Instanz der Windows Internet Explorer-Anwendung zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e0c36-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c36-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e0c36-114">Requirements</span></span>



| <span data-ttu-id="e0c36-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0c36-115">Requirement</span></span> | <span data-ttu-id="e0c36-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e0c36-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c36-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0c36-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c36-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0c36-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e0c36-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0c36-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c36-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0c36-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0c36-121">Header</span><span class="sxs-lookup"><span data-stu-id="e0c36-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c36-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c36-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e0c36-123">IDL</span><span class="sxs-lookup"><span data-stu-id="e0c36-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0c36-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0c36-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e0c36-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e0c36-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0c36-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="e0c36-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
