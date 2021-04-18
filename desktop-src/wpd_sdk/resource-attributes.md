---
description: Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribute.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Ressourcen Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365624"
---
# <a name="resource-attributes"></a><span data-ttu-id="b127d-103">Ressourcen Attribute</span><span class="sxs-lookup"><span data-stu-id="b127d-103">Resource Attributes</span></span>

<span data-ttu-id="b127d-104">Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribute.</span><span class="sxs-lookup"><span data-stu-id="b127d-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="b127d-105">Diese Attribute werden von den folgenden Methoden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="b127d-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="b127d-106">**Iportabledeviceresources:: getresourceattribute**</span><span class="sxs-lookup"><span data-stu-id="b127d-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="b127d-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="b127d-107">Attribute</span></span>                                                  | <span data-ttu-id="b127d-108">VarType</span><span class="sxs-lookup"><span data-stu-id="b127d-108">VarType</span></span>      | <span data-ttu-id="b127d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b127d-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b127d-110">**Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.**</span><span class="sxs-lookup"><span data-stu-id="b127d-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="b127d-111">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b127d-111">**VT\_BOOL**</span></span> | <span data-ttu-id="b127d-112">Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Löschen der Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="b127d-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="b127d-113">Wenn Sie nicht vorhanden ist, wird angenommen, dass Sie false ist.</span><span class="sxs-lookup"><span data-stu-id="b127d-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="b127d-114">**WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen**</span><span class="sxs-lookup"><span data-stu-id="b127d-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="b127d-115">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b127d-115">**VT\_BOOL**</span></span> | <span data-ttu-id="b127d-116">Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Öffnen der Ressource für den Lesezugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="b127d-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="b127d-117">Wenn Sie nicht vorhanden ist, wird angenommen, dass Sie false ist.</span><span class="sxs-lookup"><span data-stu-id="b127d-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="b127d-118">**WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="b127d-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="b127d-119">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b127d-119">**VT\_BOOL**</span></span> | <span data-ttu-id="b127d-120">Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Öffnen der Ressource für den Schreibzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="b127d-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="b127d-121">Wenn Sie nicht vorhanden ist, wird angenommen, dass Sie false ist.</span><span class="sxs-lookup"><span data-stu-id="b127d-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="b127d-122">**WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="b127d-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="b127d-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b127d-123">**VT\_UI4**</span></span>  | <span data-ttu-id="b127d-124">Die empfohlene Puffergröße, die ein Aufrufer für gepufferte Lesevorgänge aus der Ressource verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="b127d-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="b127d-125">**Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_**</span><span class="sxs-lookup"><span data-stu-id="b127d-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="b127d-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b127d-126">**VT\_UI4**</span></span>  | <span data-ttu-id="b127d-127">Die empfohlene Puffergröße, die ein Aufrufer für gepufferte Schreibvorgänge für die Ressource verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="b127d-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="b127d-128">**Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b127d-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="b127d-129">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="b127d-129">**VT\_UI8**</span></span>  | <span data-ttu-id="b127d-130">Die Gesamtgröße der Ressourcen Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b127d-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="b127d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b127d-131">Requirements</span></span>



| <span data-ttu-id="b127d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b127d-132">Requirement</span></span> | <span data-ttu-id="b127d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b127d-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b127d-134">Header</span><span class="sxs-lookup"><span data-stu-id="b127d-134">Header</span></span><br/> | <dl> <span data-ttu-id="b127d-135"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b127d-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b127d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b127d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b127d-137">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b127d-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




