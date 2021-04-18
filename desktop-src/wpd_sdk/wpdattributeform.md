---
description: Der wpdattributeform-Enumerationstyp beschreibt, wie eine Eigenschaft ihre Werte speichert.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Wpdattributeform-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365413"
---
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="a20f2-103">Wpdattributeform-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a20f2-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="a20f2-104">Der **wpdattributeform** -Enumerationstyp beschreibt, wie eine Eigenschaft ihre Werte speichert.</span><span class="sxs-lookup"><span data-stu-id="a20f2-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20f2-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="a20f2-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a20f2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a20f2-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**Das WPD- \_ Eigenschafts \_ Attribut ist \_ \_ nicht angegeben.**</span><span class="sxs-lookup"><span data-stu-id="a20f2-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="a20f2-108">Die Form der Eigenschaften Daten ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="a20f2-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="a20f2-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD- \_ Eigenschafts \_ Attribut- \_ Formular \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="a20f2-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="a20f2-110">Der Wert wird als Wertebereich mit einem minimal-und Maximalwert ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="a20f2-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="a20f2-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD- \_ Eigenschafts \_ Attribut- \_ Formular \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a20f2-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="a20f2-112">Die-Eigenschaft verfügt über eine Reihe einzelner Werte.</span><span class="sxs-lookup"><span data-stu-id="a20f2-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="a20f2-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ \_ regulärer \_ Ausdruck für WPD-Eigenschafts Attribut**</span><span class="sxs-lookup"><span data-stu-id="a20f2-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="a20f2-114">Der Eigenschafts Wert ist ein regulärer Ausdruck und kein literaler Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="a20f2-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="a20f2-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD- \_ Eigenschafts \_ Attribut ( \_ \_ Ojbect- \_ Bezeichner)**</span><span class="sxs-lookup"><span data-stu-id="a20f2-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="a20f2-116">Der Eigenschafts Wert stellt einen Objekt Bezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="a20f2-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a20f2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a20f2-117">Remarks</span></span>

<span data-ttu-id="a20f2-118">Diese Enumeration wird von der Eigenschaft " [WPD \_ Property \_ Attribute \_ Form](attributes.md) " verwendet, um zu beschreiben, wie die Daten einer Eigenschaft gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a20f2-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20f2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a20f2-119">Requirements</span></span>



| <span data-ttu-id="a20f2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a20f2-120">Requirement</span></span> | <span data-ttu-id="a20f2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a20f2-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a20f2-122">Header</span><span class="sxs-lookup"><span data-stu-id="a20f2-122">Header</span></span><br/> | <dl> <span data-ttu-id="a20f2-123"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a20f2-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20f2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a20f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20f2-125">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="a20f2-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




