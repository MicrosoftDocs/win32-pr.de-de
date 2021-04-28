---
description: 'Shell.Application-Eigenschaft: Enthält das Application-Objekt des Objekts.'
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Shell.Application-Eigenschaft (Shldisp.h)
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
ms.openlocfilehash: 5a90b3953ed54b8a3652d6c9c26533d433ffb600
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083858"
---
# <a name="shellapplication-property"></a><span data-ttu-id="f3e41-103">Shell.Application-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3e41-103">Shell.Application property</span></span>

<span data-ttu-id="f3e41-104">Enthält das Application-Objekt des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f3e41-104">Contains the object's Application object.</span></span>

<span data-ttu-id="f3e41-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f3e41-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e41-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3e41-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="f3e41-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f3e41-107">Property value</span></span>

<span data-ttu-id="f3e41-108">Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das Anwendungsobjekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="f3e41-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e41-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3e41-109">Remarks</span></span>

<span data-ttu-id="f3e41-110">Die **Application-Eigenschaft** gibt das Automatisierungsobjekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält, wenn auf dieses Objekt zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3e41-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="f3e41-111">Andernfalls gibt diese Eigenschaft das Automatisierungsobjekt des WebBrowser-Steuerelements zurück.</span><span class="sxs-lookup"><span data-stu-id="f3e41-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="f3e41-112">Verwenden Sie diese Eigenschaft mit den **Befehlen Set** und **CreateObject** oder mit dem **Befehl GetObject,** um eine Instanz der Windows Internet Explorer zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3e41-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e41-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3e41-113">Requirements</span></span>



| <span data-ttu-id="f3e41-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3e41-114">Requirement</span></span> | <span data-ttu-id="f3e41-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f3e41-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e41-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3e41-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e41-117">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3e41-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3e41-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3e41-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e41-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3e41-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f3e41-120">Header</span><span class="sxs-lookup"><span data-stu-id="f3e41-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e41-121"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e41-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f3e41-122">Idl</span><span class="sxs-lookup"><span data-stu-id="f3e41-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3e41-123"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3e41-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f3e41-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f3e41-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3e41-125"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="f3e41-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
