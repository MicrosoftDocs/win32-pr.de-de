---
description: 'IPortableDeviceValues::GetCount-Methode: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.'
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: IPortableDeviceValues::GetCount-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086238"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="da6d9-103">IPortableDeviceValues::GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="da6d9-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="da6d9-104">Die **GetCount-Methode** ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="da6d9-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="da6d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da6d9-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="da6d9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da6d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da6d9-107">*pcelt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="da6d9-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6d9-108">Zeiger auf ein **DWORD,** das die Anzahl der Elemente in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="da6d9-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da6d9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da6d9-109">Return value</span></span>

<span data-ttu-id="da6d9-110">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="da6d9-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="da6d9-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da6d9-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="da6d9-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="da6d9-112">Return code</span></span>                                                                          | <span data-ttu-id="da6d9-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da6d9-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="da6d9-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="da6d9-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="da6d9-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da6d9-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="da6d9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da6d9-116">Requirements</span></span>



| <span data-ttu-id="da6d9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da6d9-117">Requirement</span></span> | <span data-ttu-id="da6d9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="da6d9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da6d9-119">Header</span><span class="sxs-lookup"><span data-stu-id="da6d9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="da6d9-120"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="da6d9-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="da6d9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da6d9-121">Library</span></span><br/> | <dl> <span data-ttu-id="da6d9-122"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="da6d9-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da6d9-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da6d9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da6d9-124">**IPortableDeviceValues-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="da6d9-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




