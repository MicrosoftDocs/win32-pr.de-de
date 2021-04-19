---
description: Die setbuffervalue-Methode fügt einen neuen \* Bytewert (Type VT \_ Vector \| VT \_ UI1) hinzu oder überschreibt eine vorhandene.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'Iportabledevicevalues:: setbuffervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359670"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="9b299-103">Iportabledevicevalues:: setbuffervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="9b299-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="9b299-104">Die **setbuffervalue** -Methode fügt einen neuen  \* Bytewert (Type VT \_ Vector \| VT \_ UI1) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="9b299-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b299-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b299-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="9b299-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b299-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b299-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b299-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b299-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="9b299-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b299-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b299-110">Ein **Byte \*** , das die Daten enthält, die in das Element geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b299-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="9b299-111">Die gesendeten Puffer Daten werden in die-Schnittstelle kopiert, sodass der Aufrufer diesen Puffer nach dem Aufruf freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="9b299-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="9b299-112">*cbValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b299-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b299-113">Die Größe des Werts, auf den *pValue* zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="9b299-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b299-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b299-114">Return value</span></span>

<span data-ttu-id="9b299-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="9b299-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9b299-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9b299-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9b299-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9b299-117">Return code</span></span>                                                                          | <span data-ttu-id="9b299-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b299-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9b299-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b299-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9b299-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b299-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b299-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b299-121">Remarks</span></span>

<span data-ttu-id="9b299-122">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b299-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="9b299-123">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="9b299-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="9b299-124">Das Festlegen eines Puffers, der **null oder NULL** ist, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b299-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b299-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b299-125">Requirements</span></span>



| <span data-ttu-id="9b299-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b299-126">Requirement</span></span> | <span data-ttu-id="9b299-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9b299-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b299-128">Header</span><span class="sxs-lookup"><span data-stu-id="9b299-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9b299-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b299-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b299-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b299-130">Library</span></span><br/> | <dl> <span data-ttu-id="9b299-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b299-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b299-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b299-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b299-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9b299-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="9b299-134">**Iportablede vicevalues:: getbuffervalue**</span><span class="sxs-lookup"><span data-stu-id="9b299-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




