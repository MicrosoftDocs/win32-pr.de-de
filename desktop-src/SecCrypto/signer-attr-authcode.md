---
description: Gibt Attribute für eine Authenticode-Signatur an.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960898"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="bb68b-103">Signer \_ attr \_ AuthCode-Struktur</span><span class="sxs-lookup"><span data-stu-id="bb68b-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="bb68b-104">Die **Signer \_ attr \_ AuthCode** -Struktur gibt Attribute für eine [*Authenticode*](../secgloss/a-gly.md) -Signatur an.</span><span class="sxs-lookup"><span data-stu-id="bb68b-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="bb68b-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="bb68b-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="bb68b-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb68b-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bb68b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb68b-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="bb68b-108">Member</span><span class="sxs-lookup"><span data-stu-id="bb68b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb68b-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="bb68b-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb68b-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bb68b-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb68b-111">**gewerblich**</span><span class="sxs-lookup"><span data-stu-id="bb68b-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="bb68b-112">" **True** ", um den Betreff als kommerzieller Verleger zu signieren. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="bb68b-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bb68b-113">**findividual**</span><span class="sxs-lookup"><span data-stu-id="bb68b-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="bb68b-114">" **True** ", um den Betreff als einzelner Verleger zu signieren. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="bb68b-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bb68b-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="bb68b-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="bb68b-116">Der Anzeige Name der Datei beim herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bb68b-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="bb68b-117">**pwszinfo**</span><span class="sxs-lookup"><span data-stu-id="bb68b-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="bb68b-118">Der Anzeige Name der URL der Datei beim herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bb68b-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb68b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb68b-119">Requirements</span></span>



| <span data-ttu-id="bb68b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb68b-120">Requirement</span></span> | <span data-ttu-id="bb68b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bb68b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb68b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb68b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb68b-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb68b-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bb68b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb68b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb68b-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb68b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb68b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb68b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb68b-127">**\_Signatur Informationen des Signatur Gebers \_**</span><span class="sxs-lookup"><span data-stu-id="bb68b-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
