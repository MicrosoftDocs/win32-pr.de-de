---
title: Iadspath-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadspath-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- Iadspath-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742681"
---
# <a name="iadspath-property-methods"></a><span data-ttu-id="29e5d-105">Iadspath-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="29e5d-105">IADsPath Property Methods</span></span>

<span data-ttu-id="29e5d-106">Die-Eigenschaften Methode der [**iadspath**](/windows/desktop/api/Iads/nn-iads-iadspath) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="29e5d-106">The property method of the [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) interface sets the property described in the following table.</span></span> <span data-ttu-id="29e5d-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="29e5d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="29e5d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29e5d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="29e5d-109">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="29e5d-109">**Path**</span></span>
<span data-ttu-id="29e5d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="29e5d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="29e5d-111">Pfad zu einem Verzeichnis des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="29e5d-111">Path of a directory of the file system.</span></span>

<dt>

<span data-ttu-id="29e5d-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29e5d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="29e5d-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="29e5d-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="29e5d-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="29e5d-114">**Type**</span></span>
<span data-ttu-id="29e5d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="29e5d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="29e5d-116">Dateityp des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="29e5d-116">File type of the file system.</span></span>

<dt>

<span data-ttu-id="29e5d-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29e5d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="29e5d-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="29e5d-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="29e5d-119">**Volumename**</span><span class="sxs-lookup"><span data-stu-id="29e5d-119">**VolumeName**</span></span>
<span data-ttu-id="29e5d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="29e5d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="29e5d-121">Name eines vorhandenen Volumes des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="29e5d-121">Name of an existing volume of the file system.</span></span>

<dt>

<span data-ttu-id="29e5d-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29e5d-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="29e5d-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="29e5d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="29e5d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29e5d-124">Requirements</span></span>



| <span data-ttu-id="29e5d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29e5d-125">Requirement</span></span> | <span data-ttu-id="29e5d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="29e5d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29e5d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29e5d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29e5d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29e5d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29e5d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29e5d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29e5d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29e5d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29e5d-131">Header</span><span class="sxs-lookup"><span data-stu-id="29e5d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="29e5d-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="29e5d-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="29e5d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="29e5d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29e5d-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29e5d-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="29e5d-135">IID</span><span class="sxs-lookup"><span data-stu-id="29e5d-135">IID</span></span><br/>                      | <span data-ttu-id="29e5d-136">IID \_ iadspath ist als B287FCD5-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="29e5d-136">IID\_IADsPath is defined as B287FCD5-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="29e5d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29e5d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e5d-138">**IADsPath**</span><span class="sxs-lookup"><span data-stu-id="29e5d-138">**IADsPath**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[<span data-ttu-id="29e5d-139">**ADS- \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="29e5d-139">**ADS\_PATH**</span></span>](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





