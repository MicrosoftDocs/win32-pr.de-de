---
title: AxWindowsMediaPlayer. VERSIONINFO-Eigenschaft
description: Die VERSIONINFO-Eigenschaft ruft einen Wert ab, der die Version des Windows-Media Player angibt.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- VERSIONINFO-Eigenschaften Fenster Media Player
- VERSIONINFO-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, VERSIONINFO-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372184"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="13fe9-106">AxWindowsMediaPlayer. VERSIONINFO-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="13fe9-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="13fe9-107">Die VERSIONINFO-Eigenschaft ruft einen Wert ab, der die Version des Windows-Media Player angibt.</span><span class="sxs-lookup"><span data-stu-id="13fe9-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="13fe9-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="13fe9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fe9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="13fe9-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="13fe9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="13fe9-110">Property value</span></span>

<span data-ttu-id="13fe9-111">Ein System. String-Wert, der die Versionsinformationen im folgenden Format ist: "*X*. 0,0. *Yyyy*"Where *X* steht für die Hauptversionsnummer und *yyyy* für die Buildnummer.</span><span class="sxs-lookup"><span data-stu-id="13fe9-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="13fe9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13fe9-112">Examples</span></span>

<span data-ttu-id="13fe9-113">Im folgenden Beispiel wird eine Schaltfläche erstellt, die beim Klicken ein Meldungs Feld mit den Versionsinformationen für Windows Media Player anzeigt.</span><span class="sxs-lookup"><span data-stu-id="13fe9-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="13fe9-114">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="13fe9-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="13fe9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13fe9-115">Requirements</span></span>



| <span data-ttu-id="13fe9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13fe9-116">Requirement</span></span> | <span data-ttu-id="13fe9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13fe9-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fe9-118">Version</span><span class="sxs-lookup"><span data-stu-id="13fe9-118">Version</span></span><br/>   | <span data-ttu-id="13fe9-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="13fe9-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="13fe9-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="13fe9-120">Namespace</span></span><br/> | <span data-ttu-id="13fe9-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="13fe9-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="13fe9-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="13fe9-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="13fe9-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="13fe9-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13fe9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13fe9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fe9-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="13fe9-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





