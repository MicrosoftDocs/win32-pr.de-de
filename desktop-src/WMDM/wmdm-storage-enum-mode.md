---
title: WMDM_STORAGE_ENUM_MODE-Enumeration
description: Der Enumerationstyp der WMDM- \_ Speicher \_ \_ Enumeration definiert, wie der Inhalt des Speichers aufgelistet werden soll. Diese Enumeration wird von IWMDMStorage3 tenumpreference verwendet.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- Device Manager der WMDM_STORAGE_ENUM_MODE-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369946"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="d4708-105">\_ \_ \_ Enumeration des enumerationsmodus für WMDM-Speicher</span><span class="sxs-lookup"><span data-stu-id="d4708-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="d4708-106">Der Enumerationstyp der **WMDM- \_ Speicher \_ \_** Enumeration definiert, wie der Inhalt des Speichers aufgelistet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4708-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="d4708-107">Diese Enumeration wird von [**IWMDMStorage3:: abtenumpreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4708-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4708-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4708-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="d4708-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d4708-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4708-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**Enum- \_ Modus \_ RAW**</span><span class="sxs-lookup"><span data-stu-id="d4708-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="d4708-111">Listet den Inhalt des Speichers auf, so wie er im Dateisystem des Speichers angeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4708-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="d4708-112">**der Enum- \_ Modus \_ verwendet die Geräte- \_ \_ Pref.**</span><span class="sxs-lookup"><span data-stu-id="d4708-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="d4708-113">Listet den Inhalt des Speichers auf der Grundlage der Geräteeinstellung auf, wie vom *UseMetadataViews* -Geräteparameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4708-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="d4708-114">**metadatenansichten im Enum- \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4708-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="d4708-115">Listet den Inhalt des Speichers auf, indem der Inhalt basierend auf einer Metadatenansicht organisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4708-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="d4708-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**der Enum- \_ Modus \_ verwendet die Geräte- \_ \_ Pref.**</span><span class="sxs-lookup"><span data-stu-id="d4708-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="d4708-117">Listet den Inhalt des Speichers auf der Grundlage der Geräteeinstellung auf, wie vom *UseMetadataViews* -Geräteparameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4708-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="d4708-118">**metadatenansichten im Enum- \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4708-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="d4708-119">Listet den Inhalt des Speichers auf, indem der Inhalt basierend auf einer Metadatenansicht organisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4708-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="d4708-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**metadatenansichten im Enum- \_ Modus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4708-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="d4708-121">Listet den Inhalt des Speichers auf, indem der Inhalt basierend auf einer Metadatenansicht organisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4708-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4708-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4708-122">Requirements</span></span>



| <span data-ttu-id="d4708-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4708-123">Requirement</span></span> | <span data-ttu-id="d4708-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d4708-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d4708-125">Header</span><span class="sxs-lookup"><span data-stu-id="d4708-125">Header</span></span><br/> | <dl> <span data-ttu-id="d4708-126"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4708-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4708-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4708-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4708-128">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="d4708-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





