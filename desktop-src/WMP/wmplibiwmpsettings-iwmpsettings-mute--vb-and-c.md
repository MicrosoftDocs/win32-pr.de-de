---
title: Iwmpsettings-Eigenschaft stumm schalten
description: Mit der Eigenschaft stumm wird ein Wert abgerufen oder festgelegt, der angibt, ob Audiodaten stumm sind
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- Eigenschaften Fenster Media Player stumm schalten
- stumm Eigenschaften Fenster Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, Eigenschaft stumm schalten
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374039"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="1f3e5-106">Iwmpsettings:: stumm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f3e5-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="1f3e5-107">Mit der Eigenschaft **stumm** wird ein Wert abgerufen oder festgelegt, der angibt, ob Audiodaten stumm sind</span><span class="sxs-lookup"><span data-stu-id="1f3e5-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f3e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f3e5-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="1f3e5-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1f3e5-109">Property value</span></span>

<span data-ttu-id="1f3e5-110">Ein **System. Boolean** -Wert, der angibt, ob Audiodaten stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="1f3e5-111">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="1f3e5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f3e5-112">Examples</span></span>

<span data-ttu-id="1f3e5-113">Im folgenden Beispiel wird ein Kontrollkästchen erstellt, und die **stumm** Eigenschaft wird zum stumm schalten und Aufheben der stumm Schaltung gewechselt, wenn der aktivierte Zustand des Felds geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="1f3e5-114">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1f3e5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f3e5-115">Requirements</span></span>



| <span data-ttu-id="1f3e5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f3e5-116">Requirement</span></span> | <span data-ttu-id="1f3e5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1f3e5-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3e5-118">Version</span><span class="sxs-lookup"><span data-stu-id="1f3e5-118">Version</span></span><br/>   | <span data-ttu-id="1f3e5-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="1f3e5-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1f3e5-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f3e5-120">Namespace</span></span><br/> | <span data-ttu-id="1f3e5-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1f3e5-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1f3e5-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="1f3e5-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1f3e5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1f3e5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f3e5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f3e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3e5-125">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1f3e5-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1f3e5-126">**Iwmpsettings. Rate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1f3e5-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





