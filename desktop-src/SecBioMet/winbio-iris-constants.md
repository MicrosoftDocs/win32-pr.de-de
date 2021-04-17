---
title: WINBIO_IRIS Konstanten (winbio \_ types. h)
description: Geben Sie die Typen für die Schwert Erkennung an.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477490"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="5f2d4-103">Winbio \_ IRIS-Konstanten</span><span class="sxs-lookup"><span data-stu-id="5f2d4-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="5f2d4-104">Die folgenden Konstanten sind SubType-Werte für den **\_ \_ Subtyp "winbio** ", die zum Angeben der Typen für die Iris-Erkennung jenseits der ANSI-Werte verwendet werden können 379-2004: "IRIS-Bildaustausch Format", die keine linken/rechten Augen Werte definiert:</span><span class="sxs-lookup"><span data-stu-id="5f2d4-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="5f2d4-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="5f2d4-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="5f2d4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f2d4-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="5f2d4-107"><dt> **Winbio \_ IRIS \_ Type \_ Unknown**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5f2d4-108">Der Iris-Typ ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="5f2d4-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="5f2d4-109"><dt> **Winbio \_ IRIS \_ left \_ Eye**</dt> <dt>0xF 5</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="5f2d4-110">Der Iris-Typ ist das linke Auge.</span><span class="sxs-lookup"><span data-stu-id="5f2d4-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="5f2d4-111"><dt> **Winbio \_ IRIS \_ right \_ Eye**</dt> <dt>0xF 6</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="5f2d4-112">Der Iris-Typ ist das rechte Auge.</span><span class="sxs-lookup"><span data-stu-id="5f2d4-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="5f2d4-113"><dt>**Winbio \_ \_Nicht spezifizierte Schwert- \_ POS \_ 01**</dt> <dt>0xF 7</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="5f2d4-114">Ein Untertyp, der der ersten Vorlage eines Benutzers zugeordnet ist, wenn nur ein Auge den Kamera Rahmen hat und nicht bestimmt werden kann, ob es sich um den Benutzer Links oder rechts handelt.</span><span class="sxs-lookup"><span data-stu-id="5f2d4-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="5f2d4-115"><dt> **Winbio \_ IRIS \_ nicht angegebene \_ POS \_ 02**</dt> <dt>0xF 8</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="5f2d4-116">Ein Untertyp, der der zweiten Vorlage eines Benutzers zugeordnet ist, wenn nur ein Auge den Kamera Rahmen hat und nicht bestimmt werden kann, ob es sich um den Benutzer Links oder rechts handelt.</span><span class="sxs-lookup"><span data-stu-id="5f2d4-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="5f2d4-117"><dt> **Winbio \_ IRIS \_ beide \_ Augen**</dt> <dt>0xF 9</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="5f2d4-118">Der Iris-Typ ist beide Augen.</span><span class="sxs-lookup"><span data-stu-id="5f2d4-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="5f2d4-119"><dt> **Winbio \_ IRIS \_ entweder \_ Eye**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="5f2d4-120">Der Typ "Iris" ist entweder "Eye".</span><span class="sxs-lookup"><span data-stu-id="5f2d4-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="5f2d4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f2d4-121">Requirements</span></span>



| <span data-ttu-id="5f2d4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f2d4-122">Requirement</span></span> | <span data-ttu-id="5f2d4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5f2d4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2d4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f2d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2d4-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f2d4-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5f2d4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f2d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2d4-127">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f2d4-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5f2d4-128">Header</span><span class="sxs-lookup"><span data-stu-id="5f2d4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f2d4-129"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f2d4-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





