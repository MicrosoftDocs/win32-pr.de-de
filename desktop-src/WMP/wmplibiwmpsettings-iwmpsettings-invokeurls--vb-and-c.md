---
title: Iwmpsettings invokeurls (Eigenschaft)
description: Die invokeurls-Eigenschaft ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- invokeurls-Eigenschaft, Windows-Media Player
- invokeurls-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings Interface, Windows Media Player, invokeurls (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371575"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="2b916-106">Iwmpsettings:: invokeurls (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2b916-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="2b916-107">Die **invokeurls** -Eigenschaft ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="2b916-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b916-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b916-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="2b916-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2b916-109">Property value</span></span>

<span data-ttu-id="2b916-110">Ein **System. Boolean** -Wert, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen.</span><span class="sxs-lookup"><span data-stu-id="2b916-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="2b916-111">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="2b916-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b916-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b916-112">Remarks</span></span>

<span data-ttu-id="2b916-113">Digitale Mediendateien und Streams können URL-Skript Befehle enthalten.</span><span class="sxs-lookup"><span data-stu-id="2b916-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="2b916-114">Wenn ein URL-Skript Befehl an das Windows Media Player-Steuerelement gesendet wird, wird er unabhängig von dem von **invokeurls** abgerufenen Wert zuerst an den **AxWindowsMediaPlayer-Ereignishandler " \_ \_ scriptcommandevent** " übergeben.</span><span class="sxs-lookup"><span data-stu-id="2b916-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="2b916-115">Nachdem **\_ wmpocxevents \_ scriptcommandevent** beendet wurde, überprüft Windows Media Player **invokeurls** , um zu bestimmen, ob der Standard Webbrowser mit der URL gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b916-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="2b916-116">Sie können URLs selektiv anzeigen, indem Sie Sie in **\_ wmpocxevents \_ scriptcommandevent** überprüfen und **invokeurls** wie gewünscht festlegen.</span><span class="sxs-lookup"><span data-stu-id="2b916-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b916-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b916-117">Requirements</span></span>



| <span data-ttu-id="2b916-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b916-118">Requirement</span></span> | <span data-ttu-id="2b916-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2b916-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b916-120">Version</span><span class="sxs-lookup"><span data-stu-id="2b916-120">Version</span></span><br/>   | <span data-ttu-id="2b916-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2b916-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b916-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b916-122">Namespace</span></span><br/> | <span data-ttu-id="2b916-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2b916-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b916-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="2b916-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b916-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b916-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b916-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b916-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b916-127">**AxWindowsMediaPlayer. ScriptCommand-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b916-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="2b916-128">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b916-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





