---
title: WINBIO_ANSI_385_FACE Konstanten (winbio \_ types. h)
description: Geben Sie die Bildtypen für die Vorder-und Gesichtserkennung an.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105411"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="53dbb-103">Winbio \_ ANSI \_ 385- \_ Gesichts Konstanten</span><span class="sxs-lookup"><span data-stu-id="53dbb-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="53dbb-104">Die folgenden Konstanten sind **\_ \_ subtypwerte von winbio-Biometrie** , die verwendet werden können, um die beiden Typen von frontal Bild Bildern anzugeben, wie in ANSI-INCITS 385-2004: "Gesichts Erkennungs Format für Datenaustausch" definiert: vollständige Auflösung und niedrige Auflösung.</span><span class="sxs-lookup"><span data-stu-id="53dbb-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="53dbb-105">In der Praxis verwendet das biometrische Framework nur voll auflösende Bilder für die Gesichtserkennung.</span><span class="sxs-lookup"><span data-stu-id="53dbb-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="53dbb-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="53dbb-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="53dbb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53dbb-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="53dbb-108"><dt>**Winbio \_ ANSI \_ 385- \_ Gesichts \_ Typen \_ unbekannt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53dbb-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="53dbb-109">Der Bildtyp für frontal Gesichter ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="53dbb-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="53dbb-110"><dt>**Winbio \_ ANSI \_ 385 \_ Gesicht \_ frontal \_ voll**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53dbb-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="53dbb-111">Der Bildtyp für frontal Gesichter ist vollständig aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="53dbb-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="53dbb-112"><dt>**Winbio \_ ANSI \_ 385 \_ Gesicht \_ frontaler \_ Token**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53dbb-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="53dbb-113">Der Bildtyp für frontal Gesichter ist eine niedrige Auflösung.</span><span class="sxs-lookup"><span data-stu-id="53dbb-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="53dbb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53dbb-114">Requirements</span></span>



| <span data-ttu-id="53dbb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53dbb-115">Requirement</span></span> | <span data-ttu-id="53dbb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="53dbb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53dbb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53dbb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53dbb-118">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53dbb-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="53dbb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53dbb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53dbb-120">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53dbb-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="53dbb-121">Header</span><span class="sxs-lookup"><span data-stu-id="53dbb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53dbb-122"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53dbb-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





