---
description: Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Parameter Attribute für Methoden und Ereignisse eines Geräte Dienstanbieter.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Parameter Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363209"
---
# <a name="parameter-attributes"></a><span data-ttu-id="93b9a-103">Parameterattribute</span><span class="sxs-lookup"><span data-stu-id="93b9a-103">Parameter Attributes</span></span>

<span data-ttu-id="93b9a-104">Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Parameter Attribute für Methoden und Ereignisse eines Geräte Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="93b9a-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="93b9a-105">Diese Attribute werden von den folgenden Methoden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="93b9a-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="93b9a-106">**Iportabletoviceservicecapabili:: getmethodparameterattribute**</span><span class="sxs-lookup"><span data-stu-id="93b9a-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="93b9a-107">**Iportabletoviceservicecapabili:: geteventparameterattribute**</span><span class="sxs-lookup"><span data-stu-id="93b9a-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="93b9a-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="93b9a-108">Attribute</span></span>                                            | <span data-ttu-id="93b9a-109">VarType</span><span class="sxs-lookup"><span data-stu-id="93b9a-109">VarType</span></span>         | <span data-ttu-id="93b9a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93b9a-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b9a-111">**Standardwert des WPD- \_ Parameter \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="93b9a-112">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="93b9a-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="93b9a-113">Der Standardwert des Parameters.</span><span class="sxs-lookup"><span data-stu-id="93b9a-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="93b9a-114">**\_ \_ \_ Enumerationselemente für WPD-Parameter Attribute \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="93b9a-115">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="93b9a-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="93b9a-116">Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle, die die Enumerationswerte für den Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="93b9a-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="93b9a-117">**WPD- \_ Parameter- \_ Attribut \_ Formular**</span><span class="sxs-lookup"><span data-stu-id="93b9a-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="93b9a-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="93b9a-118">**VT\_UI4**</span></span>     | <span data-ttu-id="93b9a-119">Die Form gültiger zulässiger Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="93b9a-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="93b9a-120">**maximale Größe des WPD- \_ Parameter \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="93b9a-121">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="93b9a-121">**VT\_UI8**</span></span>     | <span data-ttu-id="93b9a-122">Die maximale Größe des Parameters in Byte.</span><span class="sxs-lookup"><span data-stu-id="93b9a-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="93b9a-123">**Name des WPD- \_ Parameter \_ Attributs \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="93b9a-124">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="93b9a-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="93b9a-125">Eine Zeichenfolge, die den Skript freundlichen Namen eines Ereignisses oder Methoden Parameters angibt.</span><span class="sxs-lookup"><span data-stu-id="93b9a-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="93b9a-126">Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="93b9a-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="93b9a-127">**Reihenfolge der WPD- \_ Parameter \_ Attribute \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="93b9a-128">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="93b9a-128">**VT\_UI4**</span></span>     | <span data-ttu-id="93b9a-129">Der null basierte Index für die Parameterreihenfolge, sodass der Auftragswert 0 dem ersten Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="93b9a-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="93b9a-130">**Bereich des WPD- \_ Parameter \_ \_ Bereichs \_ Min.**</span><span class="sxs-lookup"><span data-stu-id="93b9a-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="93b9a-131">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="93b9a-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="93b9a-132">Der maximale Wert für einen Parameter im Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93b9a-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="93b9a-133">**Bereich des WPD- \_ Parameter \_ Attributs \_ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="93b9a-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="93b9a-134">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="93b9a-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="93b9a-135">Der minimale Wert für einen Parameter im Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93b9a-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="93b9a-136">**Bereich für \_ den \_ Attribut \_ Bereich \_ für WPD-Parameter**</span><span class="sxs-lookup"><span data-stu-id="93b9a-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="93b9a-137">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="93b9a-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="93b9a-138">Der Schrittwert für einen Parameter im Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93b9a-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="93b9a-139">**regulärer Ausdruck des WPD- \_ Parameter \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="93b9a-140">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="93b9a-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="93b9a-141">Ein regulärer Ausdruck, der akzeptable Werte für die Parameter der Form eines regulären Ausdrucks der Form des WPD- \_ Parameter \_ Attributs angibt \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93b9a-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="93b9a-142">**Benutzertyp des WPD- \_ Parameter \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93b9a-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="93b9a-143">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="93b9a-143">**VT\_UI4**</span></span>     | <span data-ttu-id="93b9a-144">Eine ganze Zahl, die die Verwendung eines Methoden Parameters angibt, z. b. in/out. Gültige Werte sind der Enumerationstyp für die [**Verwendung von WPD- \_ Parametern \_ \_**](wpd-parameter-usage-types.md) .</span><span class="sxs-lookup"><span data-stu-id="93b9a-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="93b9a-145">**WPD- \_ Parameter \_ Attribut \_ VarType**</span><span class="sxs-lookup"><span data-stu-id="93b9a-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="93b9a-146">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="93b9a-146">**VT\_UI4**</span></span>     | <span data-ttu-id="93b9a-147">Der VarType-Parameter.</span><span class="sxs-lookup"><span data-stu-id="93b9a-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="93b9a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93b9a-148">Requirements</span></span>



| <span data-ttu-id="93b9a-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93b9a-149">Requirement</span></span> | <span data-ttu-id="93b9a-150">Wert</span><span class="sxs-lookup"><span data-stu-id="93b9a-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b9a-151">Header</span><span class="sxs-lookup"><span data-stu-id="93b9a-151">Header</span></span><br/> | <dl> <span data-ttu-id="93b9a-152"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="93b9a-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b9a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93b9a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b9a-154">**Eigenschaften und Attribute**</span><span class="sxs-lookup"><span data-stu-id="93b9a-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




