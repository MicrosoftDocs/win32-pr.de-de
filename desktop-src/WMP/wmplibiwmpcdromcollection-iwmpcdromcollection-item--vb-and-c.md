---
title: Iwmpcdromcollection-Element Methode
description: Die Item-Methode gibt eine iwmpcdrom-Schnittstelle am angegebenen Index zurück.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371167"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="441a8-106">Iwmpcdromcollection:: Item-Methode</span><span class="sxs-lookup"><span data-stu-id="441a8-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="441a8-107">Die **Item** -Methode gibt eine **iwmpcdrom** -Schnittstelle am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="441a8-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="441a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="441a8-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="441a8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="441a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441a8-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="441a8-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441a8-111">Ein **System. Int32** -Wert, der der Index ist.</span><span class="sxs-lookup"><span data-stu-id="441a8-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441a8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="441a8-112">Return value</span></span>

<span data-ttu-id="441a8-113">Eine **WMPLib. iwmpcdrom** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="441a8-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="441a8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="441a8-114">Remarks</span></span>

<span data-ttu-id="441a8-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="441a8-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="441a8-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="441a8-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="441a8-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="441a8-117">Examples</span></span>

<span data-ttu-id="441a8-118">Im folgenden Beispiel wird das- **Element** verwendet, um den laufwerkspezifizierer und den Wiedergabelisten Namen von allen auf dem Computer verfügbaren CD in einem Listenfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="441a8-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="441a8-119">Wenn das Laufwerk tatsächlich DVD-Inhalte enthält, ist Windows XP oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="441a8-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="441a8-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="441a8-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="441a8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="441a8-121">Requirements</span></span>



| <span data-ttu-id="441a8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="441a8-122">Requirement</span></span> | <span data-ttu-id="441a8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="441a8-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="441a8-124">Version</span><span class="sxs-lookup"><span data-stu-id="441a8-124">Version</span></span><br/>   | <span data-ttu-id="441a8-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="441a8-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="441a8-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="441a8-126">Namespace</span></span><br/> | <span data-ttu-id="441a8-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="441a8-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="441a8-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="441a8-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="441a8-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="441a8-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441a8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="441a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441a8-131">**Iwmpcdrom-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="441a8-132">**Iwmpcdromcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="441a8-133">**Iwmpcdromcollection. Count (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="441a8-134">**Iwmpcdromcollection. getbydrivespecifier (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="441a8-135">**IWMPPlaylist.Name (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="441a8-136">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="441a8-137">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="441a8-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





