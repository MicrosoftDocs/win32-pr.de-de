---
description: Die getitemsfromui-Methode des Item-Objekts zeigt ein Dialogfeld an, in dem ein Benutzer Bilder und Audiodaten auswählen kann, die von einem Gerät übertragen werden sollen.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. getitemsfromui-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130020"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="a05dc-103">Item. getitemsfromui-Methode</span><span class="sxs-lookup"><span data-stu-id="a05dc-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="a05dc-104">Die **getitemsfromui** -Methode des [**Item**](-wia-item.md) -Objekts zeigt ein Dialogfeld an, in dem ein Benutzer Bilder und Audiodaten auswählen kann, die von einem Gerät übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a05dc-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a05dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a05dc-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="a05dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a05dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05dc-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a05dc-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05dc-108">Typ: **[ **wiaflag**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="a05dc-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="a05dc-109"> (0)</span><span class="sxs-lookup"><span data-stu-id="a05dc-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a05dc-110">Standard.</span><span class="sxs-lookup"><span data-stu-id="a05dc-110">Default.</span></span> <span data-ttu-id="a05dc-111">\[in \] gibt das Dialogfeld Verhalten an.</span><span class="sxs-lookup"><span data-stu-id="a05dc-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="a05dc-112">Die gültigen Werte für diesen Parameter sind identisch mit denen für den *lFlags* -Parameter der [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a05dc-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a05dc-113">*Absicht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a05dc-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05dc-114">Typ: **wiaintent**</span><span class="sxs-lookup"><span data-stu-id="a05dc-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="a05dc-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="a05dc-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a05dc-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="a05dc-116">Default.</span></span> <span data-ttu-id="a05dc-117">\[in \] gibt an, welche Art von Daten das Image darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="a05dc-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="a05dc-118">Eine Liste der Abbild Intent-Werte finden Sie unter [**Bild beabsichtigte Konstanten**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="a05dc-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05dc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a05dc-119">Return value</span></span>

<span data-ttu-id="a05dc-120">Typ: **ICollection**</span><span class="sxs-lookup"><span data-stu-id="a05dc-120">Type: **ICollection**</span></span>

<span data-ttu-id="a05dc-121">Diese Methode gibt eine Auflistung von [**Element**](-wia-item.md) Objekten zurück, die die vom Benutzer ausgewählten Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="a05dc-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="a05dc-122">Wenn keine Elemente ausgewählt sind, ist die Auflistung leer.</span><span class="sxs-lookup"><span data-stu-id="a05dc-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05dc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a05dc-123">Remarks</span></span>

<span data-ttu-id="a05dc-124">Fügen Sie für Microsoft Visual Basic-Anwendungen einen Verweis auf die Typbibliothek "Windows-Abbild Erfassung 1,01" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a05dc-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="a05dc-125">Diese Methode gilt nur für Geräte (Stamm Elemente).</span><span class="sxs-lookup"><span data-stu-id="a05dc-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="a05dc-126">Die-Methode gibt eine Auflistung von [**Element**](-wia-item.md) Objekten zurück, die die vom Benutzer ausgewählten Bilder oder Audioclips darstellen.</span><span class="sxs-lookup"><span data-stu-id="a05dc-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="a05dc-127">Wenn vom Benutzer keine Elemente ausgewählt werden, gibt die Methode eine leere Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="a05dc-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="a05dc-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a05dc-128">Examples</span></span>

<span data-ttu-id="a05dc-129">Das folgende Beispiel veranschaulicht die Verwendung der **getitemsfromui** -Methode, um Benutzern das Auswählen von Bildern aus einem Dialogfeld zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a05dc-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="a05dc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a05dc-130">Requirements</span></span>



| <span data-ttu-id="a05dc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a05dc-131">Requirement</span></span> | <span data-ttu-id="a05dc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a05dc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a05dc-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a05dc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a05dc-134">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a05dc-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a05dc-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a05dc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a05dc-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a05dc-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a05dc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a05dc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a05dc-138"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a05dc-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




