---
title: Showmessageaction. MessageBody-Eigenschaft
description: Ruft bei der Skripterstellung den Nachrichtentext ab, der im Textkörper des Meldungs Felds angezeigt wird, oder legt diesen fest.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- MessageBody-Eigenschaft Taskplaner
- MessageBody-Eigenschaft Taskplaner, showmessageaction-Objekt
- Showmessageaction-Objekt Taskplaner, MessageBody-Eigenschaft
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858738"
---
# <a name="showmessageactionmessagebody-property"></a><span data-ttu-id="72bdb-106">Showmessageaction. MessageBody-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72bdb-106">ShowMessageAction.MessageBody property</span></span>

<span data-ttu-id="72bdb-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72bdb-107">\[This object is no longer supported.</span></span> <span data-ttu-id="72bdb-108">Sie können IExecAction mit der Windows Scripting [**MsgBox-Funktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Meldung in der Benutzersitzung anzuzeigen.\]</span><span class="sxs-lookup"><span data-stu-id="72bdb-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="72bdb-109">Ruft bei der Skripterstellung den Nachrichtentext ab, der im Textkörper des Meldungs Felds angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="72bdb-109">For scripting, gets or sets the message text that is displayed in the body of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="72bdb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="72bdb-110">Syntax</span></span>


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a><span data-ttu-id="72bdb-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="72bdb-111">Property value</span></span>

<span data-ttu-id="72bdb-112">Der Meldungs Text, der im Textkörper des Meldungs Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="72bdb-112">The message text that is displayed in the body of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="72bdb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72bdb-113">Remarks</span></span>

<span data-ttu-id="72bdb-114">Parametrisierte Zeichen folgen können im Nachrichtentext des Meldungs Felds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72bdb-114">Parameterized strings can be used in the message text of the message box.</span></span> <span data-ttu-id="72bdb-115">Weitere Informationen finden Sie im Abschnitt "Beispiele" in " [**EventTrigger. valuequeries**](eventtrigger-valuequeries.md)".</span><span class="sxs-lookup"><span data-stu-id="72bdb-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="72bdb-116">Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="72bdb-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="72bdb-117">Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="72bdb-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="72bdb-118">Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist.</span><span class="sxs-lookup"><span data-stu-id="72bdb-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="72bdb-119">Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .</span><span class="sxs-lookup"><span data-stu-id="72bdb-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="72bdb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72bdb-120">Requirements</span></span>



| <span data-ttu-id="72bdb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72bdb-121">Requirement</span></span> | <span data-ttu-id="72bdb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="72bdb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72bdb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72bdb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="72bdb-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72bdb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="72bdb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72bdb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="72bdb-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72bdb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72bdb-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="72bdb-127">End of client support</span></span><br/>    | <span data-ttu-id="72bdb-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="72bdb-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="72bdb-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="72bdb-129">End of server support</span></span><br/>    | <span data-ttu-id="72bdb-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72bdb-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="72bdb-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="72bdb-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="72bdb-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72bdb-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72bdb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="72bdb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72bdb-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72bdb-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72bdb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72bdb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72bdb-136">**Showmessageaction**</span><span class="sxs-lookup"><span data-stu-id="72bdb-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

