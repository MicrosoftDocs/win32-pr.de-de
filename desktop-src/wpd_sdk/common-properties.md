---
description: Windows Portable Devices (WPD) unterstützt die folgenden Eigenschaften von Befehlsparametern.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Befehlsparameter (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371221"
---
# <a name="command-parameters"></a><span data-ttu-id="8d928-103">Befehlsparameter</span><span class="sxs-lookup"><span data-stu-id="8d928-103">Command Parameters</span></span>

<span data-ttu-id="8d928-104">Windows Portable Devices (WPD) unterstützt die folgenden Eigenschaften von Befehlsparametern.</span><span class="sxs-lookup"><span data-stu-id="8d928-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="8d928-105">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8d928-105">**Property**</span></span>                                            | <span data-ttu-id="8d928-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="8d928-106">**VarType**</span></span>     | <span data-ttu-id="8d928-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d928-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d928-108">**\_ \_ allgemeine \_ Client \_ Informationen für WPD-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="8d928-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="8d928-109">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="8d928-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="8d928-110">Eine [**iportableendvicevalues**](iportabledevicevalues.md) -Schnittstelle, die der Treiber verwendet, um den Client zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8d928-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="8d928-111">**WPD- \_ Eigenschaft allgemeiner \_ \_ Client \_ Informations \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="8d928-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="8d928-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8d928-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="8d928-113">Ein vom Treiber angegebener Kontext, der einen Client für alle nachfolgenden Vorgänge identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8d928-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="8d928-114">**\_ \_ allgemeine \_ Befehls \_ Kategorie der WPD-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8d928-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="8d928-115">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="8d928-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="8d928-116">Der **GUID** -Teil des **PropertyKey** -Werts des Befehls.</span><span class="sxs-lookup"><span data-stu-id="8d928-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="8d928-117">**\_ \_ allgemeine \_ Befehls- \_ ID für WPD-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8d928-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="8d928-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8d928-118">**VT\_UI4**</span></span>     | <span data-ttu-id="8d928-119">Der persistente eindeutige ID-Teil (PID) des **PropertyKey** -Werts des Befehls.</span><span class="sxs-lookup"><span data-stu-id="8d928-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="8d928-120">**Allgemeine WPD- \_ Eigenschaft ( \_ \_ Befehls \_ Ziel)**</span><span class="sxs-lookup"><span data-stu-id="8d928-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="8d928-121">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8d928-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="8d928-122">Der Zielobjekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="8d928-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="8d928-123">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="8d928-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="8d928-124">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8d928-124">**VT\_UI4**</span></span>     | <span data-ttu-id="8d928-125">Ein Treiber spezifischer Fehlercode, der von einem WPD-Treiber zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d928-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="8d928-126">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d928-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="8d928-127">**VT- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="8d928-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="8d928-128">Der **HRESULT** -Wert, der von einem WPD-Treiber für einen bestimmten Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d928-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="8d928-129">**\_ \_ allgemeine \_ Objekt- \_ IDs der WPD-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8d928-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="8d928-130">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="8d928-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="8d928-131">Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle vom Variant-Typ **VT \_ LPWSTR** , die eine Liste von Objekt bezeichgern enthält.</span><span class="sxs-lookup"><span data-stu-id="8d928-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="8d928-132">**WPD- \_ Eigenschaft \_ allgemeine \_ persistente \_ eindeutige \_ IDs**</span><span class="sxs-lookup"><span data-stu-id="8d928-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="8d928-133">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="8d928-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="8d928-134">Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle vom Variant-Typ **VT \_ LPWSTR** , die eine Liste von PIDs enthält.</span><span class="sxs-lookup"><span data-stu-id="8d928-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="8d928-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d928-135">Requirements</span></span>



| <span data-ttu-id="8d928-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d928-136">Requirement</span></span> | <span data-ttu-id="8d928-137">Wert</span><span class="sxs-lookup"><span data-stu-id="8d928-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d928-138">Header</span><span class="sxs-lookup"><span data-stu-id="8d928-138">Header</span></span><br/> | <dl> <span data-ttu-id="8d928-139"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d928-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d928-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d928-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d928-141">**Eigenschaften und Attribute**</span><span class="sxs-lookup"><span data-stu-id="8d928-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




