---
title: Iwmpmedia isread onlyitem-Methode
description: Die isread onlyitem-Methode gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medien Elements bearbeitet werden können.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- isread onlyitem-Methode, Windows Media Player
- isleseronlyitem-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, isread onlyitem-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361470"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="ffadc-106">Iwmpmedia:: isread onlyitem-Methode</span><span class="sxs-lookup"><span data-stu-id="ffadc-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="ffadc-107">Die **isread onlyitem** -Methode gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medien Elements bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="ffadc-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffadc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffadc-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="ffadc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffadc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffadc-110">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffadc-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffadc-111">Ein **System. String** -Wert, der der Name des Medien Elements ist.</span><span class="sxs-lookup"><span data-stu-id="ffadc-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffadc-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffadc-112">Return value</span></span>

<span data-ttu-id="ffadc-113">Ein **System. Boolean** -Wert, der angibt, ob die Attribute schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="ffadc-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffadc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffadc-114">Remarks</span></span>

<span data-ttu-id="ffadc-115">Wenn ein Attribut schreibgeschützt ist, kann es nicht mit der **setiteminfo** -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ffadc-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="ffadc-116">Beachten Sie, dass diese Methode möglicherweise unterschiedliche Werte für ein bestimmtes Attribut zurückgibt, wenn Sie mit verschiedenen Versionen von Windows Media Player verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ffadc-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="ffadc-117">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="ffadc-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ffadc-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ffadc-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ffadc-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffadc-119">Examples</span></span>

<span data-ttu-id="ffadc-120">Im folgenden Beispiel wird **isinfoonlyitem** verwendet, um ein mehr zeitiges Textfeld mit Informationen zum aktuellen Medien Element auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="ffadc-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="ffadc-121">Im Code werden die einzelnen Attribute des aktuellen Medien Elements sowie Text angezeigt, der angibt, ob das Attribut schreibgeschützt ist oder Lese-/Schreibzugriff aufweist.</span><span class="sxs-lookup"><span data-stu-id="ffadc-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="ffadc-122">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ffadc-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="ffadc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffadc-123">Requirements</span></span>



| <span data-ttu-id="ffadc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffadc-124">Requirement</span></span> | <span data-ttu-id="ffadc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ffadc-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffadc-126">Version</span><span class="sxs-lookup"><span data-stu-id="ffadc-126">Version</span></span><br/>   | <span data-ttu-id="ffadc-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ffadc-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ffadc-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffadc-128">Namespace</span></span><br/> | <span data-ttu-id="ffadc-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ffadc-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ffadc-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="ffadc-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ffadc-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ffadc-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffadc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffadc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffadc-133">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ffadc-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ffadc-134">**Iwmpmedia. Einstellungs Verzeichnis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ffadc-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





