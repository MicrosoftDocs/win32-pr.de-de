---
description: Die idxtalphasetter-Schnittstelle legt Eigenschaften für den Alpha Setter-Effekt fest. Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn Sie den Alpha Setter-Effekt rendert.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Idxtalphasetter-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362006"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="eec62-103">Idxtalphasetter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eec62-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="eec62-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="eec62-104">\[Deprecated.</span></span> <span data-ttu-id="eec62-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="eec62-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eec62-106">Die- `IDxtAlphaSetter` Schnittstelle legt Eigenschaften für den [Alpha Setter](alpha-setter-effect.md) -Effekt fest.</span><span class="sxs-lookup"><span data-stu-id="eec62-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="eec62-107">Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn Sie den Alpha Setter-Effekt rendert.</span><span class="sxs-lookup"><span data-stu-id="eec62-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="eec62-108">Die-Anwendungen müssen diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="eec62-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="eec62-109">Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eec62-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="eec62-110">Member</span><span class="sxs-lookup"><span data-stu-id="eec62-110">Members</span></span>

<span data-ttu-id="eec62-111">Die **idxtalphasetter** -Schnittstelle erbt von **idxeffect**.</span><span class="sxs-lookup"><span data-stu-id="eec62-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="eec62-112">**Idxtalphasetter** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eec62-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="eec62-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="eec62-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eec62-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="eec62-114">Methods</span></span>

<span data-ttu-id="eec62-115">Die **idxtalphasetter** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eec62-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="eec62-116">Methode</span><span class="sxs-lookup"><span data-stu-id="eec62-116">Method</span></span>                                                  | <span data-ttu-id="eec62-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eec62-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="eec62-118">**\_Alpha**</span><span class="sxs-lookup"><span data-stu-id="eec62-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="eec62-119">Ruft den Alpha-Wert für das gesamte Bild ab.</span><span class="sxs-lookup"><span data-stu-id="eec62-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="eec62-120">**\_alpharamp erhalten**</span><span class="sxs-lookup"><span data-stu-id="eec62-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="eec62-121">Ruft die Eigenschaft für die Alpha-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="eec62-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="eec62-122">**\_Alpha platzieren**</span><span class="sxs-lookup"><span data-stu-id="eec62-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="eec62-123">Gibt den Alpha-Wert für das gesamte Bild an.</span><span class="sxs-lookup"><span data-stu-id="eec62-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="eec62-124">**Put \_ alpharamp**</span><span class="sxs-lookup"><span data-stu-id="eec62-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="eec62-125">Gibt die Eigenschaft für die Alpha-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="eec62-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="eec62-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eec62-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eec62-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="eec62-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eec62-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="eec62-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eec62-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eec62-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eec62-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eec62-130">Requirements</span></span>



| <span data-ttu-id="eec62-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eec62-131">Requirement</span></span> | <span data-ttu-id="eec62-132">Wert</span><span class="sxs-lookup"><span data-stu-id="eec62-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec62-133">Header</span><span class="sxs-lookup"><span data-stu-id="eec62-133">Header</span></span><br/>  | <dl> <span data-ttu-id="eec62-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="eec62-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eec62-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eec62-135">Library</span></span><br/> | <dl> <span data-ttu-id="eec62-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="eec62-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




