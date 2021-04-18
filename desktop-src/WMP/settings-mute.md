---
title: Settings. stumm
description: Mit der Eigenschaft stumm wird ein Wert angegeben und abgerufen, der angibt, ob Audiodaten stumm geschaltet werden.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Einstellungen. stumm schalten von Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371086"
---
# <a name="settingsmute"></a><span data-ttu-id="7174f-104">Settings. stumm</span><span class="sxs-lookup"><span data-stu-id="7174f-104">Settings.mute</span></span>

<span data-ttu-id="7174f-105">Mit der Eigenschaft **stumm** wird ein Wert angegeben und abgerufen, der angibt, ob Audiodaten stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7174f-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="7174f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7174f-106">Syntax</span></span>

<span data-ttu-id="7174f-107">Player. Settings. stumm</span><span class="sxs-lookup"><span data-stu-id="7174f-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="7174f-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7174f-108">Possible Values</span></span>

<span data-ttu-id="7174f-109">Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7174f-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7174f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7174f-110">Value</span></span> | <span data-ttu-id="7174f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7174f-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="7174f-112">true</span><span class="sxs-lookup"><span data-stu-id="7174f-112">true</span></span>  | <span data-ttu-id="7174f-113">Audiodaten werden stumm geschaltet.</span><span class="sxs-lookup"><span data-stu-id="7174f-113">Audio is muted.</span></span>              |
| <span data-ttu-id="7174f-114">false</span><span class="sxs-lookup"><span data-stu-id="7174f-114">false</span></span> | <span data-ttu-id="7174f-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="7174f-115">Default.</span></span> <span data-ttu-id="7174f-116">Das Audioformat wird nicht stumm geschaltet.</span><span class="sxs-lookup"><span data-stu-id="7174f-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="7174f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7174f-117">Examples</span></span>

<span data-ttu-id="7174f-118">Im folgenden Beispiel wird ein HTML-Checkbox-Element erstellt, mit dem der Benutzer Audiodaten stumm schalten und die stumm Schaltung aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="7174f-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="7174f-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7174f-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="7174f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7174f-120">Requirements</span></span>



| <span data-ttu-id="7174f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7174f-121">Requirement</span></span> | <span data-ttu-id="7174f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7174f-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7174f-123">Version</span><span class="sxs-lookup"><span data-stu-id="7174f-123">Version</span></span><br/> | <span data-ttu-id="7174f-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7174f-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7174f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7174f-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7174f-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7174f-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7174f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7174f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7174f-128">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="7174f-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





