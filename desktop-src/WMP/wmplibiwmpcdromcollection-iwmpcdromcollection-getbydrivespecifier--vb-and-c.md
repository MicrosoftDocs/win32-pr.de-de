---
title: Iwmpcdromcollection getbydrivespecifier-Methode
description: Die getbydrivespecifier-Methode gibt eine iwmpcdrom-Schnittstelle zurück, die einem bestimmten Laufwerk Buchstaben zugeordnet ist.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- getbydrivespecifier-Methode, Windows Media Player
- getbydrivespecifier-Methode, Windows Media Player, iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle, Windows Media Player, getbydrivespecifier-Methode
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361975"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="5b942-106">Iwmpcdromcollection:: getbydrivespecifier-Methode</span><span class="sxs-lookup"><span data-stu-id="5b942-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="5b942-107">Die **getbydrivespecifier** -Methode gibt eine **iwmpcdrom** -Schnittstelle zurück, die einem bestimmten Laufwerk Buchstaben zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5b942-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b942-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b942-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="5b942-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b942-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b942-110">*bstraudrivespecifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b942-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b942-111">Eine **System. String** , bei der es sich um den Laufwerk Buchstaben handelt, gefolgt von einem Doppelpunkt (":").</span><span class="sxs-lookup"><span data-stu-id="5b942-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b942-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b942-112">Return value</span></span>

<span data-ttu-id="5b942-113">Eine **WMPLib. iwmpcdrom** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5b942-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b942-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b942-114">Remarks</span></span>

<span data-ttu-id="5b942-115">Laufwerk Buchstaben müssen in der Form *x*: angegeben werden, wobei *x* den Laufwerk Buchstaben darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b942-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="5b942-116">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b942-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5b942-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5b942-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5b942-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b942-118">Examples</span></span>

<span data-ttu-id="5b942-119">Im folgenden Beispiel wird **getbydrivespecifier** verwendet, um die **iwmpcdrom** -Schnittstelle zu erhalten, die einem Laufwerk Buchstaben entspricht, der vom Benutzer in einem Textfeld bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5b942-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="5b942-120">Die **iwmpcdrom. Auswerfen** -Methode wird dann aufgerufen, um das angegebene Laufwerk zu ewerfen.</span><span class="sxs-lookup"><span data-stu-id="5b942-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="5b942-121">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5b942-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="5b942-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b942-122">Requirements</span></span>



| <span data-ttu-id="5b942-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b942-123">Requirement</span></span> | <span data-ttu-id="5b942-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5b942-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b942-125">Version</span><span class="sxs-lookup"><span data-stu-id="5b942-125">Version</span></span><br/>   | <span data-ttu-id="5b942-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5b942-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5b942-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b942-127">Namespace</span></span><br/> | <span data-ttu-id="5b942-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5b942-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5b942-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="5b942-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5b942-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5b942-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b942-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b942-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b942-132">**Iwmpcdrom-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5b942-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b942-133">**Iwmpcdrom. eject (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5b942-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b942-134">**Iwmpcdromcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5b942-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b942-135">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5b942-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b942-136">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5b942-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





