---
description: Die LoadXml-Methode lädt Eigenschafts Daten, die in Extensible Markup Language (XML) ausgedrückt werden.
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Ipropertysetter:: LoadXml-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368318"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="5d76a-103">Ipropertysetter:: LoadXml-Methode</span><span class="sxs-lookup"><span data-stu-id="5d76a-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="5d76a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5d76a-104">\[Deprecated.</span></span> <span data-ttu-id="5d76a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5d76a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d76a-106">Die- `LoadXML` Methode lädt Eigenschafts Daten, die in Extensible Markup Language (XML) ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="5d76a-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d76a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d76a-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="5d76a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d76a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d76a-109">*pxml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d76a-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d76a-110">Ein Zeiger auf die **IUnknown** -Schnittstelle eines vom Microsoft XML-Parser erstellten XML-Elements.</span><span class="sxs-lookup"><span data-stu-id="5d76a-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d76a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d76a-111">Return value</span></span>

<span data-ttu-id="5d76a-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5d76a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5d76a-113">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="5d76a-113">Possible values include the following.</span></span>



| <span data-ttu-id="5d76a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5d76a-114">Return code</span></span>                                                                                                  | <span data-ttu-id="5d76a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d76a-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="5d76a-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5d76a-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="5d76a-117">Keine Eigenschafts Daten.</span><span class="sxs-lookup"><span data-stu-id="5d76a-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="5d76a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d76a-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="5d76a-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5d76a-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="5d76a-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="5d76a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="5d76a-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5d76a-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="5d76a-122"><dt>**VFW \_ E \_ ungültiges \_ Datei \_ Format.**</dt></span><span class="sxs-lookup"><span data-stu-id="5d76a-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="5d76a-123">Ungültiges Format.</span><span class="sxs-lookup"><span data-stu-id="5d76a-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="5d76a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d76a-124">Remarks</span></span>

<span data-ttu-id="5d76a-125">In der Regel müssen Anwendungen diese Methode nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d76a-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="5d76a-126">Von des wird es intern verwendet, um Eigenschaften aus XTL-Dateien zu laden.</span><span class="sxs-lookup"><span data-stu-id="5d76a-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="5d76a-127">Um diese Methode zu verwenden, erstellen Sie ein **IXMLDocument** -Objekt, und verwenden Sie es zum Analysieren einer XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="5d76a-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="5d76a-128">Verwenden Sie dann das **IXMLDocument** -Objekt, um **IXmlElement** -Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d76a-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="5d76a-129">Wenn das Objekt über Eigenschaften verfügt, können Sie den **IXmlElement** -Zeiger an die **LoadXml** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="5d76a-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="5d76a-130">Die-Methode lädt die Eigenschaften in den Eigenschaften Setter.</span><span class="sxs-lookup"><span data-stu-id="5d76a-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="5d76a-131">Die **IXMLDocument** -Schnittstelle und die **IXmlElement** -Schnittstelle sind in Microsoft XML Core Services (MSXML) Version 1,0 implementiert, aber in neueren Versionen von MSXML nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5d76a-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d76a-132">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5d76a-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d76a-133">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5d76a-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5d76a-134">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d76a-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d76a-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d76a-135">Requirements</span></span>



| <span data-ttu-id="5d76a-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d76a-136">Requirement</span></span> | <span data-ttu-id="5d76a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5d76a-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d76a-138">Header</span><span class="sxs-lookup"><span data-stu-id="5d76a-138">Header</span></span><br/>  | <dl> <span data-ttu-id="5d76a-139"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5d76a-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d76a-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d76a-140">Library</span></span><br/> | <dl> <span data-ttu-id="5d76a-141"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5d76a-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d76a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d76a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d76a-143">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d76a-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="5d76a-144">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5d76a-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




