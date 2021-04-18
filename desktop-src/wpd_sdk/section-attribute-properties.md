---
description: Tragbare Windows-Geräte unterstützen die folgenden Abschnitts Daten Eigenschaften.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Abschnitts Attribut Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371741"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="cf677-103">Eigenschaften des Abschnitts Attributs</span><span class="sxs-lookup"><span data-stu-id="cf677-103">Section Attribute Properties</span></span>

<span data-ttu-id="cf677-104">Tragbare Windows-Geräte unterstützen die folgenden Abschnitts Daten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf677-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="cf677-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cf677-105">Property</span></span>                                             | <span data-ttu-id="cf677-106">VarType</span><span class="sxs-lookup"><span data-stu-id="cf677-106">VarType</span></span>         | <span data-ttu-id="cf677-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf677-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf677-108">**\_ \_ Daten \_ Länge des WPD-Abschnitts**</span><span class="sxs-lookup"><span data-stu-id="cf677-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="cf677-109">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="cf677-109">**VT\_UI8**</span></span>     | <span data-ttu-id="cf677-110">Gibt die Länge des Objekts an, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cf677-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cf677-111">**\_ \_ Daten \_ Offset für WPD-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="cf677-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="cf677-112">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="cf677-112">**VT\_UI8**</span></span>     | <span data-ttu-id="cf677-113">Gibt den NULL basierten Offset der Daten für das Objekt an, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cf677-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cf677-114">**\_ \_ \_ referenzierte \_ Objekt \_ Ressource für WPD-Abschnitts Daten**</span><span class="sxs-lookup"><span data-stu-id="cf677-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="cf677-115">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="cf677-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="cf677-116">Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) mit einem einzelnen Wert, der den Schlüssel für eine bestimmte Ressource angibt. Diese Ressource ist das Objekt, auf das im WPD-Abschnitts Daten \_ \_ \_ Offset und der WPD- \_ Abschnitts \_ Daten \_ Länge verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cf677-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="cf677-117">Wenn diese Eigenschaft nicht vorhanden ist, wird der Standardwert für die WPD- \_ Ressource \_ angenommen.</span><span class="sxs-lookup"><span data-stu-id="cf677-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="cf677-118">**\_ \_ Daten \_ Einheiten für WPD-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="cf677-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="cf677-119">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="cf677-119">**VT\_UI4**</span></span>     | <span data-ttu-id="cf677-120">Gibt die für diesen Offset verwendeten Einheiten an, z. b. bytes, Millisekunden usw. Die möglichen Werte für diese Eigenschaft werden im **WPD- \_ Abschnitt \_ \_ Dateneinheiten \_ Werte** Enumeration in der Datei portabledevice. h definiert.</span><span class="sxs-lookup"><span data-stu-id="cf677-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="cf677-121">Wenn keine Einheiten angegeben werden, werden die Bytes angenommen.</span><span class="sxs-lookup"><span data-stu-id="cf677-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="cf677-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf677-122">Requirements</span></span>



| <span data-ttu-id="cf677-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf677-123">Requirement</span></span> | <span data-ttu-id="cf677-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cf677-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf677-125">Header</span><span class="sxs-lookup"><span data-stu-id="cf677-125">Header</span></span><br/> | <dl> <span data-ttu-id="cf677-126"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf677-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf677-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf677-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf677-128">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="cf677-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




