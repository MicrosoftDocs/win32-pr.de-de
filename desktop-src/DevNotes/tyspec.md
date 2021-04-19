---
description: Definiert Methoden für die Zuordnung zu einer Klassen-ID.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Tyspec-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370512"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="e5a19-103">Tyspec-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e5a19-103">TYSPEC enumeration</span></span>

<span data-ttu-id="e5a19-104">Definiert Methoden für die Zuordnung zu einer Klassen-ID.</span><span class="sxs-lookup"><span data-stu-id="e5a19-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a19-105">Syntax</span></span>


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a><span data-ttu-id="e5a19-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e5a19-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5a19-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**tyspec- \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="e5a19-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-108">eine CLSID.</span><span class="sxs-lookup"><span data-stu-id="e5a19-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="e5a19-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**tyspec- \_ fileext**</span><span class="sxs-lookup"><span data-stu-id="e5a19-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-110">Eine Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="e5a19-110">A file name extension.</span></span> <span data-ttu-id="e5a19-111">Dieser Wert wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a19-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="e5a19-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**tyspec- \_ MimeType**</span><span class="sxs-lookup"><span data-stu-id="e5a19-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-113">Ein MIME-Typ.</span><span class="sxs-lookup"><span data-stu-id="e5a19-113">A MIME type.</span></span> <span data-ttu-id="e5a19-114">Dieser Wert wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a19-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="e5a19-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**tyspec \_ Dateiname**</span><span class="sxs-lookup"><span data-stu-id="e5a19-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-116">Ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="e5a19-116">A file name.</span></span> <span data-ttu-id="e5a19-117">Dieser Wert wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a19-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="e5a19-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**tyspec- \_ ProgID**</span><span class="sxs-lookup"><span data-stu-id="e5a19-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-119">eine ProgID.</span><span class="sxs-lookup"><span data-stu-id="e5a19-119">A PROGID.</span></span> <span data-ttu-id="e5a19-120">Dieser Wert wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a19-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="e5a19-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**tyspec \_ PackageName**</span><span class="sxs-lookup"><span data-stu-id="e5a19-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-122">Ein Paketname.</span><span class="sxs-lookup"><span data-stu-id="e5a19-122">A package name.</span></span> <span data-ttu-id="e5a19-123">Dieser Wert wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a19-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="e5a19-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**tyspec \_ objectID**</span><span class="sxs-lookup"><span data-stu-id="e5a19-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="e5a19-125">Eine Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="e5a19-125">An object ID.</span></span> <span data-ttu-id="e5a19-126">Dieser Wert wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a19-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5a19-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5a19-127">Remarks</span></span>

<span data-ttu-id="e5a19-128">Die **uclsspec** -Union ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="e5a19-128">The **uCLSSPEC** union is defined as follows:</span></span>

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a><span data-ttu-id="e5a19-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5a19-129">Requirements</span></span>



| <span data-ttu-id="e5a19-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5a19-130">Requirement</span></span> | <span data-ttu-id="e5a19-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a19-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a19-132">IDL</span><span class="sxs-lookup"><span data-stu-id="e5a19-132">IDL</span></span><br/> | <dl> <span data-ttu-id="e5a19-133"><dt>Wtypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5a19-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a19-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5a19-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a19-135">**Coinstall**</span><span class="sxs-lookup"><span data-stu-id="e5a19-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
