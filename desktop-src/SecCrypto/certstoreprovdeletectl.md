---
description: Wird von certdeletectlfromstore aufgerufen, bevor eine CTL aus dem Speicher gelöscht wird.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Certstoreprovdeletectl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864352"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="b3a7e-103">Certstoreprovdeletectl-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="b3a7e-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="b3a7e-104">Die **certstoreprovdeletectl** -Rückruffunktion wird von [**certdeletectlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) aufgerufen, bevor eine CTL aus dem Speicher gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="b3a7e-105">Diese Funktion bestimmt, ob eine CTL gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a7e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3a7e-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b3a7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3a7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a7e-108">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3a7e-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a7e-109">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b3a7e-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3a7e-110">*pctlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3a7e-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a7e-111">Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3a7e-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3a7e-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a7e-113">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a7e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3a7e-114">Return value</span></span>

<span data-ttu-id="b3a7e-115">Gibt " **true** " zurück, wenn eine CTL aus dem Speicher gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a7e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3a7e-116">Requirements</span></span>



| <span data-ttu-id="b3a7e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3a7e-117">Requirement</span></span> | <span data-ttu-id="b3a7e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b3a7e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3a7e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3a7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a7e-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3a7e-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b3a7e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3a7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a7e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3a7e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
