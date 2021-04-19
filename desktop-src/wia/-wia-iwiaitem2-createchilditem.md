---
description: Erstellen Sie ein neues untergeordnetes Element. Fügt der IWiaItem2-Struktur eines Geräts IWiaItem2-Objekte hinzu.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2:: kreatechilditem-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349869"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="d04e8-104">IWiaItem2:: kreatechilditem-Methode</span><span class="sxs-lookup"><span data-stu-id="d04e8-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="d04e8-105">Erstellen Sie ein neues untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="d04e8-105">Create a new child item.</span></span> <span data-ttu-id="d04e8-106">Fügt der **IWiaItem2** -Struktur eines Geräts [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte hinzu.</span><span class="sxs-lookup"><span data-stu-id="d04e8-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="d04e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d04e8-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="d04e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d04e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d04e8-109">*litemflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d04e8-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d04e8-110">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="d04e8-110">Type: **LONG**</span></span>

<span data-ttu-id="d04e8-111">Gibt den WIA-2,0-Elementtyp an.</span><span class="sxs-lookup"><span data-stu-id="d04e8-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="d04e8-112">Siehe [**WIA-Elementtyp-Flags**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d04e8-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d04e8-113">*lkreationflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d04e8-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d04e8-114">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="d04e8-114">Type: **LONG**</span></span>

<span data-ttu-id="d04e8-115">Gibt an, wie das neue Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d04e8-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="d04e8-116"><span id="0"></span>**0** (0)</span><span class="sxs-lookup"><span data-stu-id="d04e8-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d04e8-117">Legen Sie die Standardwerte für die Eigenschaften des untergeordneten Elements fest.</span><span class="sxs-lookup"><span data-stu-id="d04e8-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="d04e8-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Kopieren \_ Übergeordnete \_ Eigenschafts \_ Werte** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="d04e8-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="d04e8-119">Kopieren Sie die Werte aller Lese-/Schreibeigenschaften von der übergeordneten.</span><span class="sxs-lookup"><span data-stu-id="d04e8-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d04e8-120">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d04e8-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d04e8-121">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d04e8-121">Type: **BSTR**</span></span>

<span data-ttu-id="d04e8-122">Gibt den Elementnamen an.</span><span class="sxs-lookup"><span data-stu-id="d04e8-122">Specifies the item name.</span></span> <span data-ttu-id="d04e8-123">Dieser Name wird an das Ende des Namens des übergeordneten Elements angehängt, um den vollständigen Elementnamen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d04e8-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="d04e8-124">*ppIWiaItem2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d04e8-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d04e8-125">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d04e8-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="d04e8-126">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle, mit der die **IWiaItem2:: featechilditem** -Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d04e8-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d04e8-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d04e8-127">Return value</span></span>

<span data-ttu-id="d04e8-128">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d04e8-128">Type: **HRESULT**</span></span>

<span data-ttu-id="d04e8-129">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d04e8-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d04e8-130">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d04e8-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d04e8-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d04e8-131">Remarks</span></span>

<span data-ttu-id="d04e8-132">Einige WIA 2,0-Hardware Geräte ermöglichen es Anwendungen, neue Elemente in der [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur zu erstellen, die das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="d04e8-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="d04e8-133">Anwendungen müssen die Geräte testen, um festzustellen, ob Sie diese Funktion unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d04e8-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="d04e8-134">Verwenden Sie die ienumwia \_ dev \_ Caps-Oberfläche, um die Funktionen des aktuellen Geräts aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="d04e8-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="d04e8-135">Wenn das Gerät das Erstellen neuer Elemente in der [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur zulässt, wird durch Aufrufen von **IWiaItem2:: auflistungschilditem** ein neues **IWiaItem2** -Objekt erstellt, das dem aktuellen Knoten untergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d04e8-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="d04e8-136">Es übergibt einen Zeiger auf den neuen Knoten über den *ppIWiaItem2* -Parameter an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d04e8-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="d04e8-137">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="d04e8-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="d04e8-138">Wenn *lkreationflags* den Wert von über \_ geordneten \_ Eigenschafts \_ Werten kopieren und *litemflags* 0 (null) ist, gibt die Funktion E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="d04e8-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04e8-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d04e8-139">Requirements</span></span>



| <span data-ttu-id="d04e8-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d04e8-140">Requirement</span></span> | <span data-ttu-id="d04e8-141">Wert</span><span class="sxs-lookup"><span data-stu-id="d04e8-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d04e8-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d04e8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d04e8-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d04e8-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d04e8-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d04e8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d04e8-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d04e8-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d04e8-146">Header</span><span class="sxs-lookup"><span data-stu-id="d04e8-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d04e8-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d04e8-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d04e8-148">IDL</span><span class="sxs-lookup"><span data-stu-id="d04e8-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d04e8-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d04e8-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
