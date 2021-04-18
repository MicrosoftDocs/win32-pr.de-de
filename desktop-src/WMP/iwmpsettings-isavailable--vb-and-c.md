---
title: Iwmpsettings. IsAvailable (VB und C)
description: Die IsAvailable-Eigenschaft (die get \_ IsAvailable-Methode in C \) Ruft einen Wert ab, der angibt, ob eine angegebene Aktion ausgeführt werden kann.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- Iwmpsettings. IsAvailable (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351208"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="e4984-104">Iwmpsettings. IsAvailable (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="e4984-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="e4984-105">Mit der **IsAvailable** -Eigenschaft (der **get \_ IsAvailable** -Methode in c#) wird ein Wert abgerufen, der angibt, ob eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4984-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="e4984-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4984-106">Parameters</span></span>

<span data-ttu-id="e4984-107">*bstritem*</span><span class="sxs-lookup"><span data-stu-id="e4984-107">*bstrItem*</span></span>

<span data-ttu-id="e4984-108">Ein **System. String** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4984-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="e4984-109">Wert</span><span class="sxs-lookup"><span data-stu-id="e4984-109">Value</span></span>              | <span data-ttu-id="e4984-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4984-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4984-111">AutoStart</span><span class="sxs-lookup"><span data-stu-id="e4984-111">AutoStart</span></span>          | <span data-ttu-id="e4984-112">Ermittelt, ob die Autostart-Eigenschaft festgelegt werden kann, um anzugeben, dass Windows Media Player die Wiedergabe automatisch startet.</span><span class="sxs-lookup"><span data-stu-id="e4984-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="e4984-113">Balance</span><span class="sxs-lookup"><span data-stu-id="e4984-113">Balance</span></span>            | <span data-ttu-id="e4984-114">Ermittelt, ob die Balance-Eigenschaft verwendet werden kann, um den Stereo Saldo festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e4984-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="e4984-115">Basis</span><span class="sxs-lookup"><span data-stu-id="e4984-115">BaseURL</span></span>            | <span data-ttu-id="e4984-116">Ermittelt, ob die baseurl-Eigenschaft festgelegt werden kann, um eine Basis-URL anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4984-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="e4984-117">Defaultframe</span><span class="sxs-lookup"><span data-stu-id="e4984-117">DefaultFrame</span></span>       | <span data-ttu-id="e4984-118">Ermittelt, ob die defaultframe-Eigenschaft festgelegt werden kann, um den Standard Frame anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4984-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="e4984-119">Enableerrordialogfelder</span><span class="sxs-lookup"><span data-stu-id="e4984-119">EnableErrorDialogs</span></span> | <span data-ttu-id="e4984-120">Ermittelt, ob die enableerrordialogs-Eigenschaft festgelegt werden kann, um das Anzeigen von Fehler Dialogfeldern zu aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e4984-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="e4984-121">GetMode</span><span class="sxs-lookup"><span data-stu-id="e4984-121">GetMode</span></span>            | <span data-ttu-id="e4984-122">Ermittelt, ob die getMode-Methode verwendet werden kann, um die aktuelle Schleife oder den Streamingmodus abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4984-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="e4984-123">Invokeurls</span><span class="sxs-lookup"><span data-stu-id="e4984-123">InvokeURLs</span></span>         | <span data-ttu-id="e4984-124">Ermittelt, ob die invokeurls-Eigenschaft festgelegt werden kann, um anzugeben, ob URL-Ereignisse einen Webbrowser starten sollen.</span><span class="sxs-lookup"><span data-stu-id="e4984-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="e4984-125">Mute</span><span class="sxs-lookup"><span data-stu-id="e4984-125">Mute</span></span>               | <span data-ttu-id="e4984-126">Ermittelt, ob die stumm Eigenschaft festgelegt werden kann, um anzugeben, ob die Audioausgabe ein-oder ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="e4984-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="e4984-127">Playcount</span><span class="sxs-lookup"><span data-stu-id="e4984-127">PlayCount</span></span>          | <span data-ttu-id="e4984-128">Ermittelt, ob die playcount-Eigenschaft festgelegt werden kann, um anzugeben, wie oft ein Medien Element abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4984-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="e4984-129">Rate</span><span class="sxs-lookup"><span data-stu-id="e4984-129">Rate</span></span>               | <span data-ttu-id="e4984-130">Ermittelt, ob die Raten Eigenschaft festgelegt werden kann, um die Wiedergabe Rate zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e4984-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="e4984-131">SetMode</span><span class="sxs-lookup"><span data-stu-id="e4984-131">SetMode</span></span>            | <span data-ttu-id="e4984-132">Ermittelt, ob die setmode-Methode verwendet werden kann, um die aktuelle Schleife oder den Shuffle-Modus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4984-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="e4984-133">Lautstärke</span><span class="sxs-lookup"><span data-stu-id="e4984-133">Volume</span></span>             | <span data-ttu-id="e4984-134">Ermittelt, ob die Volumeeigenschaft festgelegt werden kann, um das audiovolume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4984-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="e4984-135">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e4984-135">Property Value</span></span>

<span data-ttu-id="e4984-136">Ein **System. Boolean** -Wert, der angibt, ob die angegebene Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4984-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4984-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4984-137">Remarks</span></span>

<span data-ttu-id="e4984-138">**Iwmpsettings. isidentical** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="e4984-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="e4984-139">In c# wird dies als **iwmpsettings. get \_ isidentical** -Methode bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e4984-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="e4984-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4984-140">Examples</span></span>

<span data-ttu-id="e4984-141">Im folgenden Beispiel wird jede der **iwmpsettings** -Eigenschaften mithilfe der **IsAvailable** -Eigenschaft getestet (die **get \_ IsAvailable** -Methode in c#).</span><span class="sxs-lookup"><span data-stu-id="e4984-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="e4984-142">Der Eigenschaftsname und das Ergebnis jedes Tests werden in einem mehrzeiligen Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4984-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="e4984-143">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e4984-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="e4984-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4984-144">Requirements</span></span>



| <span data-ttu-id="e4984-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4984-145">Requirement</span></span> | <span data-ttu-id="e4984-146">Wert</span><span class="sxs-lookup"><span data-stu-id="e4984-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4984-147">Version</span><span class="sxs-lookup"><span data-stu-id="e4984-147">Version</span></span><br/>   | <span data-ttu-id="e4984-148">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e4984-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e4984-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4984-149">Namespace</span></span><br/> | <span data-ttu-id="e4984-150">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e4984-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e4984-151">Assembly</span><span class="sxs-lookup"><span data-stu-id="e4984-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e4984-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e4984-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4984-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4984-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4984-154">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-155">**Iwmpsettings. Autostart (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-156">**Iwmpsettings. Balance (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-157">**Iwmpsettings. baseurl (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-158">**Iwmpsettings. defaultframe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-159">**Iwmpsettings. enableerrordialogs (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-160">**Iwmpsettings. getMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-161">**Iwmpsettings. invokeurls (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-162">**Iwmpsettings. stumm (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-163">**Iwmpsettings. playcount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-164">**Iwmpsettings. Rate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-165">**Iwmpsettings. SetMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4984-166">**Iwmpsettings. Volume (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e4984-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





