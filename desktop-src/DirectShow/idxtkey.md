---
description: Die idxtkey-Schnittstelle legt Eigenschaften für den Schlüssel Übergang fest. Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten verwendet, wenn der Schlüssel Übergang gerendert wird.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Idxtkey-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364732"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="cbda6-103">Idxtkey-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cbda6-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="cbda6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cbda6-104">\[Deprecated.</span></span> <span data-ttu-id="cbda6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cbda6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cbda6-106">Die- `IDxtKey` Schnittstelle legt Eigenschaften für den [Schlüssel](key-transition.md) Übergang fest.</span><span class="sxs-lookup"><span data-stu-id="cbda6-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="cbda6-107">Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten verwendet, wenn der Schlüssel Übergang gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="cbda6-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="cbda6-108">Die-Anwendungen müssen diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbda6-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="cbda6-109">Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cbda6-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="cbda6-110">Member</span><span class="sxs-lookup"><span data-stu-id="cbda6-110">Members</span></span>

<span data-ttu-id="cbda6-111">Die **idxtkey** -Schnittstelle erbt von **idxeffect**.</span><span class="sxs-lookup"><span data-stu-id="cbda6-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="cbda6-112">**Idxtkey** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cbda6-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="cbda6-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="cbda6-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cbda6-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="cbda6-114">Methods</span></span>

<span data-ttu-id="cbda6-115">Die **idxtkey** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cbda6-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="cbda6-116">Methode</span><span class="sxs-lookup"><span data-stu-id="cbda6-116">Method</span></span>                                            | <span data-ttu-id="cbda6-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbda6-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbda6-118">**\_Farbton erhalten**</span><span class="sxs-lookup"><span data-stu-id="cbda6-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="cbda6-119">Ruft den Hue-Wert ab, für den der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbda6-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="cbda6-120">**\_Invertieren**</span><span class="sxs-lookup"><span data-stu-id="cbda6-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="cbda6-121">Ruft einen booleschen Wert ab, der angibt, ob der Schlüssel Vorgang invertiert wird.</span><span class="sxs-lookup"><span data-stu-id="cbda6-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="cbda6-122">**\_KeyType erhalten**</span><span class="sxs-lookup"><span data-stu-id="cbda6-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="cbda6-123">Ruft den Typ des Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="cbda6-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="cbda6-124">**\_Beleuchtung erhalten**</span><span class="sxs-lookup"><span data-stu-id="cbda6-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="cbda6-125">Ruft den Wert der Leuchtkraft ab, für den der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbda6-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="cbda6-126">**\_RGB erhalten**</span><span class="sxs-lookup"><span data-stu-id="cbda6-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="cbda6-127">Ruft die RGB-Farbe ab, für die der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbda6-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="cbda6-128">**\_Ähnlichkeit erhalten**</span><span class="sxs-lookup"><span data-stu-id="cbda6-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="cbda6-129">Ruft den Bereich der Farbdaten ab, der transparent wird.</span><span class="sxs-lookup"><span data-stu-id="cbda6-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="cbda6-130">**\_Farbton ablegen**</span><span class="sxs-lookup"><span data-stu-id="cbda6-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="cbda6-131">Gibt den Farbton Wert an, auf den der Schlüssel festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cbda6-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="cbda6-132">**\_Invert einfügen**</span><span class="sxs-lookup"><span data-stu-id="cbda6-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="cbda6-133">Gibt an, ob der Schlüssel Vorgang invertiert wird.</span><span class="sxs-lookup"><span data-stu-id="cbda6-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="cbda6-134">**\_KeyType platzieren**</span><span class="sxs-lookup"><span data-stu-id="cbda6-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="cbda6-135">Gibt den Typ des Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="cbda6-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="cbda6-136">**\_Leuchtkraft einfügen**</span><span class="sxs-lookup"><span data-stu-id="cbda6-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="cbda6-137">Gibt den Wert der Leuchtkraft an, auf den der Schlüssel festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="cbda6-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="cbda6-138">**\_RGB einfügen**</span><span class="sxs-lookup"><span data-stu-id="cbda6-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="cbda6-139">Gibt die RGB-Farbe für den Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="cbda6-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="cbda6-140">**\_Ähnlichkeit**</span><span class="sxs-lookup"><span data-stu-id="cbda6-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="cbda6-141">Gibt den Bereich der Farbdaten an, der transparent wird.</span><span class="sxs-lookup"><span data-stu-id="cbda6-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="cbda6-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbda6-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbda6-143">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cbda6-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cbda6-144">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cbda6-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cbda6-145">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cbda6-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cbda6-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbda6-146">Requirements</span></span>



| <span data-ttu-id="cbda6-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbda6-147">Requirement</span></span> | <span data-ttu-id="cbda6-148">Wert</span><span class="sxs-lookup"><span data-stu-id="cbda6-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbda6-149">Header</span><span class="sxs-lookup"><span data-stu-id="cbda6-149">Header</span></span><br/>  | <dl> <span data-ttu-id="cbda6-150"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cbda6-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cbda6-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cbda6-151">Library</span></span><br/> | <dl> <span data-ttu-id="cbda6-152"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cbda6-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




