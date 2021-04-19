---
title: Iwmpcdromcollection-Anzahl (Eigenschaft)
description: Die Count-Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- Anzahl der Eigenschaften Fenster Media Player
- Count-Eigenschaft, Windows Media Player, iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle, Windows Media Player, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354652"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="e45c5-106">Iwmpcdromcollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e45c5-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="e45c5-107">Die **count** -Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.</span><span class="sxs-lookup"><span data-stu-id="e45c5-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e45c5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e45c5-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e45c5-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e45c5-109">Property value</span></span>

<span data-ttu-id="e45c5-110">Ein **System. Int32** -Wert, der die Anzahl der verfügbaren Laufwerke ist.</span><span class="sxs-lookup"><span data-stu-id="e45c5-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="e45c5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e45c5-111">Remarks</span></span>

<span data-ttu-id="e45c5-112">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e45c5-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="e45c5-113">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e45c5-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e45c5-114">DVD-Laufwerke werden genau wie CD-Laufwerke gezählt.</span><span class="sxs-lookup"><span data-stu-id="e45c5-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="e45c5-115">Das Windows Media Player ActiveX-Steuerelement unterstützt jedoch nur DVD-Funktionen für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="e45c5-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="e45c5-116">In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.</span><span class="sxs-lookup"><span data-stu-id="e45c5-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="e45c5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e45c5-117">Examples</span></span>

<span data-ttu-id="e45c5-118">Im folgenden Beispiel wird count verwendet, um die Anzahl der verfügbaren CD-und DVD-Laufwerke in einem Meldungs Feld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e45c5-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="e45c5-119">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e45c5-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="e45c5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e45c5-120">Requirements</span></span>



| <span data-ttu-id="e45c5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e45c5-121">Requirement</span></span> | <span data-ttu-id="e45c5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e45c5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e45c5-123">Version</span><span class="sxs-lookup"><span data-stu-id="e45c5-123">Version</span></span><br/>   | <span data-ttu-id="e45c5-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e45c5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e45c5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e45c5-125">Namespace</span></span><br/> | <span data-ttu-id="e45c5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e45c5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e45c5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="e45c5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e45c5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e45c5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e45c5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e45c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e45c5-130">**Iwmpcdromcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e45c5-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e45c5-131">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e45c5-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e45c5-132">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e45c5-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





