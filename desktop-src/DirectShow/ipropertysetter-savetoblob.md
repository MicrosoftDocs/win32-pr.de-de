---
description: Die savetoblob-Methode speichert die Eigenschaften Daten in einem Persistenzformat.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Ipropertysetter:: savedeblob-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365499"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="be505-103">Ipropertysetter:: savedeblob-Methode</span><span class="sxs-lookup"><span data-stu-id="be505-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="be505-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="be505-104">\[Deprecated.</span></span> <span data-ttu-id="be505-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="be505-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be505-106">Die- `SaveToBlob` Methode speichert die Eigenschaften Daten in einem Persistenzformat.</span><span class="sxs-lookup"><span data-stu-id="be505-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="be505-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be505-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="be505-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be505-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be505-109">*pcsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be505-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be505-110">Empfängt die Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="be505-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="be505-111">*ppb* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be505-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be505-112">Empfängt einen Zeiger auf ein Bytearray, das die Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="be505-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be505-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be505-113">Return value</span></span>

<span data-ttu-id="be505-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="be505-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be505-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be505-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be505-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be505-116">Remarks</span></span>

<span data-ttu-id="be505-117">Die-Methode ordnet Speicher für das Bytearray zu.</span><span class="sxs-lookup"><span data-stu-id="be505-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="be505-118">Der Aufrufer muss ihn mithilfe der **CoTaskMemFree** -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="be505-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="be505-119">Alle Eigenschaftsnamen und-Werte werden auf eine Länge von 40 Zeichen gekürzt.</span><span class="sxs-lookup"><span data-stu-id="be505-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="be505-120">Aus diesem Grund ist XML das bevorzugte Persistenzformat.</span><span class="sxs-lookup"><span data-stu-id="be505-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="be505-121">Siehe [**IXml2Dex-Schnittstelle**](ixml2dex.md).</span><span class="sxs-lookup"><span data-stu-id="be505-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="be505-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="be505-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="be505-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="be505-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="be505-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be505-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be505-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be505-125">Requirements</span></span>



| <span data-ttu-id="be505-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be505-126">Requirement</span></span> | <span data-ttu-id="be505-127">Wert</span><span class="sxs-lookup"><span data-stu-id="be505-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be505-128">Header</span><span class="sxs-lookup"><span data-stu-id="be505-128">Header</span></span><br/>  | <dl> <span data-ttu-id="be505-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="be505-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="be505-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be505-130">Library</span></span><br/> | <dl> <span data-ttu-id="be505-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="be505-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be505-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be505-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be505-133">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="be505-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="be505-134">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="be505-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




