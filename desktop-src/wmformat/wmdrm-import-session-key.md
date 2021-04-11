---
title: WMDRM_IMPORT_SESSION_KEY Struktur (drmexternals. h)
description: Die Schlüsselstruktur der WMDRM- \_ Import \_ Sitzung \_ enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105303"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="1fc1f-105">WMDRM- \_ Struktur zum Importieren von \_ Sitzungs \_ Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="1fc1f-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="1fc1f-106">Die **Schlüsselstruktur der WMDRM- \_ Import \_ Sitzung \_** enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc1f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fc1f-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="1fc1f-108">Member</span><span class="sxs-lookup"><span data-stu-id="1fc1f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fc1f-109">**dwkeytype**</span><span class="sxs-lookup"><span data-stu-id="1fc1f-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="1fc1f-110">Der Sitzungs Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-110">Session key type.</span></span> <span data-ttu-id="1fc1f-111">Legen Sie auf WMDRM \_ KeyType \_ RC4 fest.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="1fc1f-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="1fc1f-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="1fc1f-113">Größe des Sitzungsschlüssels in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="1fc1f-114">Dieser Wert kann so groß sein, wie Sie benötigen, wenn die Grenzen eines einzelnen RSA-OAEP-Vorgangs über die gesamte Nachricht (diese Struktur und den Sitzungsschlüssel) liegen.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1f-115">**rgbKey**</span><span class="sxs-lookup"><span data-stu-id="1fc1f-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="1fc1f-116">Adresse eines Puffers, der den Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="1fc1f-117">Die Puffergröße muss mit dem Wert von **cbkey** identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="1fc1f-118">Die Daten im Puffer sind ein zufällig generierter Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fc1f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fc1f-119">Remarks</span></span>

<span data-ttu-id="1fc1f-120">Diese Struktur, einschließlich des Puffers, der den Sitzungsschlüssel enthält, muss mit dem öffentlichen Schlüssel des Windows Media DRM-Computers verschlüsselt und im Member **pbencryptedsessionkeymess** der [**WMDRM-Struktur \_ Import \_ Init \_ struct**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1fc1f-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc1f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fc1f-121">Requirements</span></span>



| <span data-ttu-id="1fc1f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fc1f-122">Requirement</span></span> | <span data-ttu-id="1fc1f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc1f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc1f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fc1f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc1f-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fc1f-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1fc1f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fc1f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc1f-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fc1f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1fc1f-128">Version</span><span class="sxs-lookup"><span data-stu-id="1fc1f-128">Version</span></span><br/>                  | <span data-ttu-id="1fc1f-129">SDK für Windows Media-Format 11</span><span class="sxs-lookup"><span data-stu-id="1fc1f-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="1fc1f-130">Header</span><span class="sxs-lookup"><span data-stu-id="1fc1f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc1f-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc1f-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc1f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fc1f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc1f-133">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="1fc1f-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





