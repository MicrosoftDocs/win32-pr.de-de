---
description: Beschreibt, wie ein-Parameter (Methode oder Ereignis) seinen Wert speichert.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Wpdparameterattributeform-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369592"
---
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="00290-103">Wpdparameterattributeform-Enumeration</span><span class="sxs-lookup"><span data-stu-id="00290-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="00290-104">Der [**wpdparameterattributeform**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) -Enumerationstyp beschreibt, wie ein (Methode-oder Ereignis)-Parameter seinen Wert speichert.</span><span class="sxs-lookup"><span data-stu-id="00290-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="00290-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00290-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="00290-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="00290-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00290-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**Das WPD- \_ Parameter \_ Attribut ist \_ \_ nicht angegeben.**</span><span class="sxs-lookup"><span data-stu-id="00290-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="00290-108">Die Form des-Parameters ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="00290-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="00290-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00290-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="00290-110">Der-Parameter gibt einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="00290-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="00290-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ Attribut \_ Formular- \_ Enumeration für WPD-Parameter**</span><span class="sxs-lookup"><span data-stu-id="00290-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="00290-112">Der-Parameter ist eine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="00290-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="00290-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ \_ regulärer \_ Ausdruck des WPD-Parameter Attributs**</span><span class="sxs-lookup"><span data-stu-id="00290-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="00290-114">Der-Parameter ist ein regulärer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="00290-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="00290-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**Objekt-ID des WPD- \_ Parameter \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00290-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="00290-116">Der-Parameter ist ein Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="00290-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00290-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00290-117">Requirements</span></span>



| <span data-ttu-id="00290-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00290-118">Requirement</span></span> | <span data-ttu-id="00290-119">Wert</span><span class="sxs-lookup"><span data-stu-id="00290-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="00290-120">Header</span><span class="sxs-lookup"><span data-stu-id="00290-120">Header</span></span><br/> | <dl> <span data-ttu-id="00290-121"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="00290-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

