---
description: Entfernt das aktuelle IWiaItem2-Objekt aus der Objektstruktur des Geräts.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2::D eleteitem-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368096"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="6ccad-103">IWiaItem2::D eleteitem-Methode</span><span class="sxs-lookup"><span data-stu-id="6ccad-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="6ccad-104">Entfernt das aktuelle [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt aus der Objektstruktur des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6ccad-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ccad-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6ccad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ccad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccad-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ccad-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ccad-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="6ccad-108">Type: **LONG**</span></span>

<span data-ttu-id="6ccad-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ccad-109">Currently unused.</span></span> <span data-ttu-id="6ccad-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6ccad-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ccad-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ccad-111">Return value</span></span>

<span data-ttu-id="6ccad-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ccad-112">Type: **HRESULT**</span></span>

<span data-ttu-id="6ccad-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6ccad-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ccad-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ccad-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ccad-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ccad-115">Remarks</span></span>

<span data-ttu-id="6ccad-116">Das Windows Image Acquisition (WIA) 2,0-Laufzeitsystem stellt jedes WIA 2,0-Hardware Gerät dar, das mit dem Computer des Benutzers verbunden ist, als hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="6ccad-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="6ccad-117">Ein bestimmtes WIA 2,0-Gerät lässt möglicherweise zu, dass Anwendungen **IWiaItem2** -Objekte aus der Struktur löschen.</span><span class="sxs-lookup"><span data-stu-id="6ccad-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="6ccad-118">Elemente mit untergeordneten Elementen können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6ccad-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="6ccad-119">Die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle muss verwendet werden, um das Gerät für das Löschen von Elementen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6ccad-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="6ccad-120">Wenn das Gerät das Löschen von Elementen in seiner [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur unterstützt, müssen Sie die **IWiaItem2::D eleteitem** -Methode zum Entfernen des **IWiaItem2** -Objekts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ccad-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="6ccad-121">Beachten Sie, dass diese Methode nur ein Objekt löscht, nachdem alle Verweise auf das Objekt freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="6ccad-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="6ccad-122">Wenn beim Löschen eines Elements ein Fehler aufgetreten ist, \_ wird "E DeleteItem" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ccad-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="6ccad-123">Der numerische Wert für diesen Fehler ist noch nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6ccad-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccad-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ccad-124">Requirements</span></span>



| <span data-ttu-id="6ccad-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ccad-125">Requirement</span></span> | <span data-ttu-id="6ccad-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6ccad-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccad-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ccad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccad-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ccad-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ccad-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ccad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccad-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ccad-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ccad-131">Header</span><span class="sxs-lookup"><span data-stu-id="6ccad-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccad-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ccad-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ccad-133">IDL</span><span class="sxs-lookup"><span data-stu-id="6ccad-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ccad-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ccad-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




