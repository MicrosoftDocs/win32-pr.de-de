---
title: ADSI-Attribut Änderungs Typen (IADs. h)
description: Wird verwendet \_ \_ , um den Typ des Vorgangs anzugeben, der ausgeführt werden soll, wenn ein Attribut mit der IDirectoryObject setobjectattributes-Methode geändert wird.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- Typen von Attribut Änderungen ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040320"
---
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="f8e7a-104">Typen von ADSI-Attribut Änderungen</span><span class="sxs-lookup"><span data-stu-id="f8e7a-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="f8e7a-105">Die folgenden Konstanten werden zusammen mit dem **dwcontrolcode** -Member der [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur verwendet, um den Typ des Vorgangs anzugeben, der ausgeführt werden soll, wenn ein Attribut mit der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="f8e7a-106">Weitere Informationen zum Verwenden dieser Werte finden Sie unter [Ändern von Attributen mit ADSI](modifying-attributes-with-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="f8e7a-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="f8e7a-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS ist \_ \_ klar**</span><span class="sxs-lookup"><span data-stu-id="f8e7a-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8e7a-108">1</span><span class="sxs-lookup"><span data-stu-id="f8e7a-108">1</span></span>
</dt> <dt>



<span data-ttu-id="f8e7a-109">Bewirkt, dass alle Attributwerte aus einem-Objekt entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e7a-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS- \_ \_ Update**</span><span class="sxs-lookup"><span data-stu-id="f8e7a-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8e7a-111">2</span><span class="sxs-lookup"><span data-stu-id="f8e7a-111">2</span></span>
</dt> <dt>



<span data-ttu-id="f8e7a-112">Bewirkt, dass die angegebenen Attributwerte aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e7a-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**Werbung \_ \_ Anfügen**</span><span class="sxs-lookup"><span data-stu-id="f8e7a-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8e7a-114">3</span><span class="sxs-lookup"><span data-stu-id="f8e7a-114">3</span></span>
</dt> <dt>



<span data-ttu-id="f8e7a-115">Bewirkt, dass die angegebenen Attributwerte an die vorhandenen Attributwerte angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e7a-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS- \_ \_ Löschung**</span><span class="sxs-lookup"><span data-stu-id="f8e7a-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8e7a-117">4</span><span class="sxs-lookup"><span data-stu-id="f8e7a-117">4</span></span>
</dt> <dt>



<span data-ttu-id="f8e7a-118">Bewirkt, dass die angegebenen Attributwerte aus einem-Objekt entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8e7a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8e7a-119">Remarks</span></span>

<span data-ttu-id="f8e7a-120">Diese Konstanten sollen mit der [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur in der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="f8e7a-121">Diese Konstanten sollten nicht mit Membern der Enumeration der [**ADS- \_ Eigenschaften \_ Operation \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) verwechselt werden, die mit der [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8e7a-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e7a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8e7a-122">Requirements</span></span>



| <span data-ttu-id="f8e7a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8e7a-123">Requirement</span></span> | <span data-ttu-id="f8e7a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f8e7a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f8e7a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8e7a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e7a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8e7a-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="f8e7a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8e7a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e7a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8e7a-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="f8e7a-129">Header</span><span class="sxs-lookup"><span data-stu-id="f8e7a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e7a-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e7a-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8e7a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8e7a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e7a-132">**Anzeige \_ \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f8e7a-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="f8e7a-133">**IDirectoryObject:: setobjectattributes**</span><span class="sxs-lookup"><span data-stu-id="f8e7a-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="f8e7a-134">Ändern von Attributen mit ADSI</span><span class="sxs-lookup"><span data-stu-id="f8e7a-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





