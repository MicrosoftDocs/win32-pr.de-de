---
title: Iwmpmedia AttributeCount (Eigenschaft)
description: Die AttributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- AttributeCount-Eigenschaft, Windows-Media Player
- AttributeCount-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, AttributeCount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370313"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="61505-106">Iwmpmedia:: AttributeCount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="61505-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="61505-107">Die **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="61505-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="61505-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="61505-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61505-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="61505-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="61505-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="61505-110">Property value</span></span>

<span data-ttu-id="61505-111">Ein **System. Int32** -Wert, der die Anzahl ist.</span><span class="sxs-lookup"><span data-stu-id="61505-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="61505-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61505-112">Remarks</span></span>

<span data-ttu-id="61505-113">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="61505-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="61505-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="61505-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="61505-115">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="61505-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61505-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61505-116">Examples</span></span>

<span data-ttu-id="61505-117">Im folgenden Beispiel wird **AttributeCount** verwendet, um die Anzahl der Attribute zu bestimmen, die im aktuellen Medien Element verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="61505-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="61505-118">Der Code verwendet diesen Wert, um eine Liste von Attributnamen und Werten in einem Textfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="61505-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="61505-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="61505-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="61505-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61505-120">Requirements</span></span>



| <span data-ttu-id="61505-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61505-121">Requirement</span></span> | <span data-ttu-id="61505-122">Wert</span><span class="sxs-lookup"><span data-stu-id="61505-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61505-123">Version</span><span class="sxs-lookup"><span data-stu-id="61505-123">Version</span></span><br/>   | <span data-ttu-id="61505-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="61505-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="61505-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="61505-125">Namespace</span></span><br/> | <span data-ttu-id="61505-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="61505-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="61505-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="61505-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="61505-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="61505-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61505-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61505-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61505-130">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="61505-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





