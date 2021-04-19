---
description: Die seterrorvalue-Methode fügt einen neuen HRESULT-Wert (Type VT \_ Error) hinzu oder überschreibt eine vorhandene.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Iportabledevicevalues:: Server-Wert-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362015"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="92263-103">Iportabledevicevalues:: Server terrorvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="92263-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="92263-104">Die **seterrorvalue** -Methode fügt einen neuen **HRESULT** -Wert (Type VT \_ Error) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="92263-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="92263-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92263-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="92263-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92263-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92263-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92263-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="92263-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="92263-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92263-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92263-110">Ein **HRESULT** , das den neuen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="92263-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92263-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92263-111">Return value</span></span>

<span data-ttu-id="92263-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="92263-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="92263-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="92263-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="92263-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="92263-114">Return code</span></span>                                                                          | <span data-ttu-id="92263-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92263-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="92263-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92263-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="92263-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92263-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92263-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92263-118">Remarks</span></span>

<span data-ttu-id="92263-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="92263-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="92263-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92263-120">Requirements</span></span>



| <span data-ttu-id="92263-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92263-121">Requirement</span></span> | <span data-ttu-id="92263-122">Wert</span><span class="sxs-lookup"><span data-stu-id="92263-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92263-123">Header</span><span class="sxs-lookup"><span data-stu-id="92263-123">Header</span></span><br/>  | <dl> <span data-ttu-id="92263-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="92263-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="92263-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92263-125">Library</span></span><br/> | <dl> <span data-ttu-id="92263-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92263-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92263-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92263-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92263-128">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="92263-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="92263-129">**Iportablede vicevalues:: geterrorvalue**</span><span class="sxs-lookup"><span data-stu-id="92263-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




