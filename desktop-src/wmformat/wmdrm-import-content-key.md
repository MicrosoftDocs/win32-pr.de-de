---
title: WMDRM_IMPORT_CONTENT_KEY Struktur (drmexternals. h)
description: Die WMDRM \_ - \_ Schlüsselstruktur zum Importieren von Inhalten \_ speichert den Inhalts Schlüssel, der beim Importieren geschützter Inhalte verwendet wird.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391578"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="37115-105">WMDRM \_ - \_ Schlüsselstruktur zum Importieren von Inhalten \_</span><span class="sxs-lookup"><span data-stu-id="37115-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="37115-106">Die **WMDRM \_ - \_ \_ Schlüssel** Struktur zum Importieren von Inhalten speichert den Inhalts Schlüssel, der beim Importieren geschützter Inhalte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37115-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="37115-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37115-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="37115-108">Member</span><span class="sxs-lookup"><span data-stu-id="37115-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37115-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="37115-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="37115-110">Version.</span><span class="sxs-lookup"><span data-stu-id="37115-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="37115-111">**cbstructsize**</span><span class="sxs-lookup"><span data-stu-id="37115-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="37115-112">Größe der Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="37115-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="37115-113">**dwivkeytype**</span><span class="sxs-lookup"><span data-stu-id="37115-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="37115-114">Der Initialisierungs Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="37115-114">Initialization vector key type.</span></span> <span data-ttu-id="37115-115">Legen Sie auf WMDRM \_ KeyType \_ RC4 fest.</span><span class="sxs-lookup"><span data-stu-id="37115-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="37115-116">**cbivkey**</span><span class="sxs-lookup"><span data-stu-id="37115-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="37115-117">Größe des Initialisierungs Vektor Schlüssels in Bytes.</span><span class="sxs-lookup"><span data-stu-id="37115-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="37115-118">**dwcontentkeytype**</span><span class="sxs-lookup"><span data-stu-id="37115-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="37115-119">Der Inhalts Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="37115-119">Content key type.</span></span> <span data-ttu-id="37115-120">Legen Sie auf WMDRM \_ KeyType \_ Cocktail fest.</span><span class="sxs-lookup"><span data-stu-id="37115-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="37115-121">**cbcontentkey**</span><span class="sxs-lookup"><span data-stu-id="37115-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="37115-122">Größe des Inhalts Schlüssels in Bytes.</span><span class="sxs-lookup"><span data-stu-id="37115-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="37115-123">**rgbkeydata**</span><span class="sxs-lookup"><span data-stu-id="37115-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="37115-124">Adresse eines Puffers, der den Inhalts Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="37115-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="37115-125">Die Puffergröße muss mit dem Wert von **cbcontentkey** identisch sein.</span><span class="sxs-lookup"><span data-stu-id="37115-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="37115-126">Dieser Schlüssel sollte dem Schlüssel entsprechen, der aus der XMR-Lizenz Meldung importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="37115-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37115-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37115-127">Remarks</span></span>

<span data-ttu-id="37115-128">Diese Struktur, einschließlich des Puffers, der den Sitzungsschlüssel enthält, muss mit dem Sitzungsschlüssel verschlüsselt und in das **pbencryptedkeymess** -Member der [**WMDRM- \_ Import \_ Init \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) -Struktur-Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="37115-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="37115-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37115-129">Requirements</span></span>



| <span data-ttu-id="37115-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37115-130">Requirement</span></span> | <span data-ttu-id="37115-131">Wert</span><span class="sxs-lookup"><span data-stu-id="37115-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="37115-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37115-132">Minimum supported client</span></span><br/> | <span data-ttu-id="37115-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37115-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37115-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37115-134">Minimum supported server</span></span><br/> | <span data-ttu-id="37115-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37115-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="37115-136">Version</span><span class="sxs-lookup"><span data-stu-id="37115-136">Version</span></span><br/>                  | <span data-ttu-id="37115-137">SDK für Windows Media-Format 11</span><span class="sxs-lookup"><span data-stu-id="37115-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="37115-138">Header</span><span class="sxs-lookup"><span data-stu-id="37115-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="37115-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="37115-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37115-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37115-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37115-141">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="37115-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





