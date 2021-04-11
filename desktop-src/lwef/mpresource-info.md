---
title: MPRESOURCE_INFO Struktur (mpclient. h)
description: Struktur der Ressourcen Informationen.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPRESOURCE_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956736"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="c17ae-105">Mpresource- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="c17ae-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="c17ae-106">Struktur der Ressourcen Informationen.</span><span class="sxs-lookup"><span data-stu-id="c17ae-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c17ae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c17ae-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="c17ae-108">Member</span><span class="sxs-lookup"><span data-stu-id="c17ae-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c17ae-109">**Schrift**</span><span class="sxs-lookup"><span data-stu-id="c17ae-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="c17ae-110">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c17ae-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="c17ae-111">Ressourcen Schema Bezeichner, z. b. "file" oder "dir".</span><span class="sxs-lookup"><span data-stu-id="c17ae-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="c17ae-112">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="c17ae-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="c17ae-113">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c17ae-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="c17ae-114">Absoluter Pfad der Ressource, basierend auf dem **Schema**.</span><span class="sxs-lookup"><span data-stu-id="c17ae-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="c17ae-115">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="c17ae-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="c17ae-116">Type: **mpresource- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="c17ae-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="c17ae-117">Dieses Feld wird festgelegt, wenn die Ressource als Teil der Bedrohung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c17ae-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="c17ae-118">Es gibt die Ressourcen Klasse an, hauptsächlich konkrete und latente.</span><span class="sxs-lookup"><span data-stu-id="c17ae-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="c17ae-119">Dies kann eine Kombination der folgenden möglichen Werte sein:</span><span class="sxs-lookup"><span data-stu-id="c17ae-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="c17ae-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c17ae-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="c17ae-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c17ae-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="c17ae-122"><dt>**MP \_ Ressourcen \_ Klasse \_ unbekannt**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="c17ae-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="c17ae-123"><dt>**MP \_ Ressourcen \_ Klasse \_ konkret**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c17ae-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="c17ae-124">Schließen Sie sich gegenseitig mit der **MP- \_ Ressourcen \_ Klasse \_** aus</span><span class="sxs-lookup"><span data-stu-id="c17ae-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="c17ae-125"><dt>**MP \_ Ressourcen \_ Klasse, \_ LATENT**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c17ae-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="c17ae-126">Schließen Sie sich gegenseitig mit **MP- \_ Ressourcen \_ Klasse \_** aus.</span><span class="sxs-lookup"><span data-stu-id="c17ae-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="c17ae-127"><dt>**MP \_ Ressourcen \_ Klassen- \_ Beispiel \_ Datei**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c17ae-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="c17ae-128"><dt>**MP \_ Ressourcen \_ Klasse \_ Shared**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="c17ae-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c17ae-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c17ae-129">Requirements</span></span>



| <span data-ttu-id="c17ae-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c17ae-130">Requirement</span></span> | <span data-ttu-id="c17ae-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c17ae-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c17ae-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c17ae-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c17ae-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c17ae-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c17ae-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c17ae-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c17ae-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c17ae-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c17ae-136">Header</span><span class="sxs-lookup"><span data-stu-id="c17ae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c17ae-137"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c17ae-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





