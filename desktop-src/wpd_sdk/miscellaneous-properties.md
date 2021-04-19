---
description: Tragbare Windows-Geräte unterstützen die folgenden verschiedenen Eigenschaften.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Sonstige Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354091"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="8270b-103">Sonstige Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8270b-103">Miscellaneous Properties</span></span>

<span data-ttu-id="8270b-104">Tragbare Windows-Geräte unterstützen die folgenden verschiedenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8270b-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="8270b-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8270b-105">Property</span></span>                                       | <span data-ttu-id="8270b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="8270b-106">VarType</span></span>         | <span data-ttu-id="8270b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8270b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8270b-108">**WPD- \_ API- \_ Option \_ use \_ Clear \_ Data \_ Stream**</span><span class="sxs-lookup"><span data-stu-id="8270b-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="8270b-109">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="8270b-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="8270b-110">Ein boolescher Wert, der angibt, ob der Datenstrom, der für die Datenübertragung erstellt wurde, eindeutig ist, d. h., DRM ist nicht beteiligt. Clients können diese Option festlegen, indem Sie Sie den Objekteigenschaften hinzufügen, die an [**iportabledevicecontent:: deateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8270b-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="8270b-111">**WPD- \_ Dienst \_ Version**</span><span class="sxs-lookup"><span data-stu-id="8270b-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="8270b-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8270b-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="8270b-113">Eine Zeichenfolge, die die Implementierungs Version eines bestimmten Geräte Dienstanbieter angibt.</span><span class="sxs-lookup"><span data-stu-id="8270b-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8270b-114">**Inhaltstypen für WPD- \_ Ordner sind \_ \_ \_ zulässig.**</span><span class="sxs-lookup"><span data-stu-id="8270b-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="8270b-115">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="8270b-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="8270b-116">Ein-Wert, der die Objekttypen angibt, die direkt untergeordnete Elemente dieses Ordners sein können.</span><span class="sxs-lookup"><span data-stu-id="8270b-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="8270b-117">Untergeordnete Ordner können über unterschiedliche Funktionen verfügen. Diese Eigenschaft ist eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) \_ , die VT CLSID-Werte enthält, die zulässige Objekttypen angeben.</span><span class="sxs-lookup"><span data-stu-id="8270b-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="8270b-118">Eine Liste der Objekttypen, die von tragbaren Windows-Geräten definiert werden, finden Sie unter [Anforderungen für Objekte](requirements-for-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8270b-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="8270b-119">**WPD- \_ Funktions \_ Objekt \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="8270b-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="8270b-120">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="8270b-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="8270b-121">Ein-Wert, der die Funktions Kategorie des-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="8270b-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8270b-122">**WPD- \_ RENDERING- \_ Informations \_ profile**</span><span class="sxs-lookup"><span data-stu-id="8270b-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="8270b-123">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="8270b-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="8270b-124">Eine [**iportabledevicevaluescollection**](iportabledevicevaluescollection.md) , die mehrere [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstellen enthält, von denen jede die Eigenschafts Einstellungen für ein Profil enthält, das vom-Objekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8270b-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="8270b-125">**\_ \_ \_ \_ Anzeige \_ Name des WPD-Objekt Hinweis Speicher Orts**</span><span class="sxs-lookup"><span data-stu-id="8270b-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="8270b-126">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8270b-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="8270b-127">Wenn ein Objekt ein Hinweis Speicherort ist, gibt diese Eigenschaft den Hinweis spezifischen Namen an, der dem Benutzer anstelle des Objekt namens angezeigt werden soll. Treiber können Positions Hinweise für verschiedene Objekttypen angeben.</span><span class="sxs-lookup"><span data-stu-id="8270b-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="8270b-128">Dies sind bevorzugte Speicherorte für Ordner, die einen bestimmten Objekttyp enthalten.</span><span class="sxs-lookup"><span data-stu-id="8270b-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="8270b-129">Eine Entsprechung wäre der Ordner Meine Bilder für Bilddateien in Windows.</span><span class="sxs-lookup"><span data-stu-id="8270b-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="8270b-130">Wenn diese Eigenschaft nicht vorhanden ist, wird in der Regel der [ \_ \_ Name des WPD-Objekts](object-properties.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8270b-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8270b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8270b-131">Requirements</span></span>



| <span data-ttu-id="8270b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8270b-132">Requirement</span></span> | <span data-ttu-id="8270b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8270b-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8270b-134">Header</span><span class="sxs-lookup"><span data-stu-id="8270b-134">Header</span></span><br/> | <dl> <span data-ttu-id="8270b-135"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8270b-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8270b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8270b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8270b-137">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="8270b-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




