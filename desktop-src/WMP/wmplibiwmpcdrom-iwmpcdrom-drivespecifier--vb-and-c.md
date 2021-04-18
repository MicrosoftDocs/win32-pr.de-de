---
title: Iwmpcdrom-drivespecifier (Eigenschaft)
description: Mit der drivespecifier-Eigenschaft wird der CD-oder DVD-Laufwerk Buchstabe abgerufen.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- drivespecifier-Eigenschaften Fenster Media Player
- drivespecifier-Eigenschaft, Windows Media Player, iwmpcdrom-Schnittstelle
- Iwmpcdrom-Schnittstelle, Windows Media Player, drivespecifier (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360898"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="faf4d-106">Iwmpcdrom::d rivespecifier (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="faf4d-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="faf4d-107">Mit der **drivespecifier** -Eigenschaft wird der CD-oder DVD-Laufwerk Buchstabe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="faf4d-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf4d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf4d-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="faf4d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="faf4d-109">Property value</span></span>

<span data-ttu-id="faf4d-110">Ein **System. String** -Wert, der der Laufwerk Buchstabe ist.</span><span class="sxs-lookup"><span data-stu-id="faf4d-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="faf4d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faf4d-111">Remarks</span></span>

<span data-ttu-id="faf4d-112">In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.</span><span class="sxs-lookup"><span data-stu-id="faf4d-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="faf4d-113">Diese Eigenschaft ruft einen Laufwerk Buchstaben für einen NULL basierten Laufwerks Index innerhalb des Bereichs ab, der mithilfe von **iwmpcdromcollection. count** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="faf4d-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="faf4d-114">Der abgerufene Wert hat die Form *x*:, wobei *X* den Laufwerk Buchstaben darstellt.</span><span class="sxs-lookup"><span data-stu-id="faf4d-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="faf4d-115">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="faf4d-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="faf4d-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="faf4d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="faf4d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faf4d-117">Examples</span></span>

<span data-ttu-id="faf4d-118">Im folgenden Beispiel wird **drivespecifier** verwendet, um eine Zeichenfolge zu erstellen, die eine Liste der verfügbaren CD-und DVD-Laufwerke enthält und diese Zeichenfolge in einem Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="faf4d-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="faf4d-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="faf4d-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="faf4d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faf4d-120">Requirements</span></span>



| <span data-ttu-id="faf4d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faf4d-121">Requirement</span></span> | <span data-ttu-id="faf4d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="faf4d-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf4d-123">Version</span><span class="sxs-lookup"><span data-stu-id="faf4d-123">Version</span></span><br/>   | <span data-ttu-id="faf4d-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="faf4d-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="faf4d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="faf4d-125">Namespace</span></span><br/> | <span data-ttu-id="faf4d-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="faf4d-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="faf4d-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="faf4d-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="faf4d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="faf4d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf4d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faf4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf4d-130">**Iwmpcdrom-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="faf4d-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="faf4d-131">**Iwmpcdromcollection. Count (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="faf4d-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="faf4d-132">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="faf4d-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="faf4d-133">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="faf4d-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





