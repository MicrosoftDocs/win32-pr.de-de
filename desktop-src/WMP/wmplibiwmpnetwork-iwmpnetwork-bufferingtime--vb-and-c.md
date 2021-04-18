---
title: Iwmpnetwork BufferingTime (Eigenschaft)
description: Die BufferingTime-Eigenschaft ruft die Zeitspanne in Millisekunden ab, die zum Puffern eingehender Daten vor Beginn der Wiedergabe reserviert wird, oder legt Sie fest.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- BufferingTime-Eigenschaft, Windows-Media Player
- BufferingTime-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, BufferingTime (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352828"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="0ffee-106">Iwmpnetwork:: BufferingTime (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0ffee-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="0ffee-107">Die **BufferingTime** -Eigenschaft ruft die Zeitspanne in Millisekunden ab, die zum Puffern eingehender Daten vor Beginn der Wiedergabe reserviert wird, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0ffee-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ffee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ffee-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0ffee-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0ffee-109">Property value</span></span>

<span data-ttu-id="0ffee-110">Ein **System. Int32** -Wert, der die Pufferzeit in Millisekunden angibt, die zwischen 0 und 60.000 und dem Standardwert 5.000 liegt.</span><span class="sxs-lookup"><span data-stu-id="0ffee-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="0ffee-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ffee-111">Examples</span></span>

<span data-ttu-id="0ffee-112">Im folgenden Codebeispiel wird **BufferingTime** verwendet, um die Anzahl der Sekunden anzugeben, die für die Pufferung eingehender Daten reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="0ffee-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="0ffee-113">Ein Textfeld ermöglicht dem Benutzer, einen neuen Wert für **BufferingTime** einzugeben, und die-Eigenschaft wird als Reaktion auf das Click-Ereignis einer Schaltfläche aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0ffee-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="0ffee-114">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0ffee-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0ffee-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ffee-115">Requirements</span></span>



| <span data-ttu-id="0ffee-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ffee-116">Requirement</span></span> | <span data-ttu-id="0ffee-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0ffee-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ffee-118">Version</span><span class="sxs-lookup"><span data-stu-id="0ffee-118">Version</span></span><br/>   | <span data-ttu-id="0ffee-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0ffee-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0ffee-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ffee-120">Namespace</span></span><br/> | <span data-ttu-id="0ffee-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ffee-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ffee-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="0ffee-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ffee-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ffee-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ffee-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ffee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ffee-125">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0ffee-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





