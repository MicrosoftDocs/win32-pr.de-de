---
title: Iwmpsettings defaultframe (Eigenschaft)
description: Mit der defaultframe-Eigenschaft wird der Name des Frames abgerufen oder festgelegt, der zum Anzeigen einer URL verwendet wird, die in einem AxWindowsMediaPlayer \_ wmpocxevents \_ scriptcommandevent-Ereignis empfangen wird.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- defaultframe-Eigenschaften Fenster Media Player
- defaultframe-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, defaultframe (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364860"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="a232b-106">Iwmpsettings::d efaultframe-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a232b-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="a232b-107">Mit der **defaultframe** -Eigenschaft wird der Name des Frames abgerufen oder festgelegt, der zum Anzeigen einer URL verwendet wird, die in einem **AxWindowsMediaPlayer \_ wmpocxevents \_ scriptcommandevent** -Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="a232b-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a232b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a232b-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="a232b-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a232b-109">Property value</span></span>

<span data-ttu-id="a232b-110">Ein **System. String** -Wert, der dem Wert des Name-Attributs des Ziel **Frame** Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="a232b-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a232b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a232b-111">Remarks</span></span>

<span data-ttu-id="a232b-112">Wenn im **\_ wmpocxevents \_ scriptcommandevent** -Ereignis ein Zielframe angegeben ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a232b-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="a232b-113">Diese Eigenschaft wird ignoriert, wenn das Applet "Netscape Navigator Java" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a232b-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="a232b-114">Im Netscape Navigator zeigt jeder empfangene URL-Skript Befehl die URL in einem neuen Browserfenster an, unabhängig vom Wert von **defaultframe**.</span><span class="sxs-lookup"><span data-stu-id="a232b-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a232b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a232b-115">Requirements</span></span>



| <span data-ttu-id="a232b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a232b-116">Requirement</span></span> | <span data-ttu-id="a232b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a232b-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a232b-118">Version</span><span class="sxs-lookup"><span data-stu-id="a232b-118">Version</span></span><br/>   | <span data-ttu-id="a232b-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a232b-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a232b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a232b-120">Namespace</span></span><br/> | <span data-ttu-id="a232b-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a232b-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a232b-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a232b-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a232b-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a232b-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a232b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a232b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a232b-125">**AxWindowsMediaPlayer. ScriptCommand-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a232b-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="a232b-126">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a232b-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





