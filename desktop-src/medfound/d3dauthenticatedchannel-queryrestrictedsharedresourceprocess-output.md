---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess-Abfrage.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127925"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a><span data-ttu-id="ff082-103">D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="ff082-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT structure</span></span>

<span data-ttu-id="ff082-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="ff082-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="ff082-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="ff082-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff082-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff082-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ff082-107">Member</span><span class="sxs-lookup"><span data-stu-id="ff082-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff082-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="ff082-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="ff082-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ff082-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="ff082-110">**Processindex**</span><span class="sxs-lookup"><span data-stu-id="ff082-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ff082-111">Der Index des Prozesses in der Liste der Prozesse.</span><span class="sxs-lookup"><span data-stu-id="ff082-111">The index of the process in the list of processes.</span></span>

</dd> <dt>

<span data-ttu-id="ff082-112">**Processidentifer**</span><span class="sxs-lookup"><span data-stu-id="ff082-112">**ProcessIdentifer**</span></span>
</dt> <dd>

<span data-ttu-id="ff082-113">Ein [**D3DAUTHENTICATEDCHANNEL \_ processidentifiertype**](d3dauthenticatedchannel-processidentifiertype.md) -Wert, der den Typ des Prozesses angibt.</span><span class="sxs-lookup"><span data-stu-id="ff082-113">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span>

</dd> <dt>

<span data-ttu-id="ff082-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="ff082-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ff082-115">Ein Prozess handle.</span><span class="sxs-lookup"><span data-stu-id="ff082-115">A process handle.</span></span> <span data-ttu-id="ff082-116">Wenn der **processidentifier** -Member gleich dem **processidtype- \_ handle** ist, enthält das **ProcessHandle** -Element ein gültiges Handle für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="ff082-116">If the **ProcessIdentifier** member equals **PROCESSIDTYPE\_HANDLE**, the **ProcessHandle** member contains a valid handle to a process.</span></span> <span data-ttu-id="ff082-117">Andernfalls wird dieser Member ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ff082-117">Otherwise, this member is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff082-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff082-118">Remarks</span></span>

<span data-ttu-id="ff082-119">Der DWM-Prozess (Desktopfenster-Manager) wird durch Festlegen von **processidentifier** auf **processidtype \_ DWM** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ff082-119">The Desktop Window Manager (DWM) process is identified by setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="ff082-120">Andere Prozesse werden identifiziert, indem das Prozess handle in **ProcessHandle** festgelegt und **processidentifier** auf **processidtype \_ handle** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ff082-120">Other processes are identified by setting the process handle in **ProcessHandle** and setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_HANDLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff082-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff082-121">Requirements</span></span>



| <span data-ttu-id="ff082-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff082-122">Requirement</span></span> | <span data-ttu-id="ff082-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ff082-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff082-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff082-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ff082-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff082-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ff082-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff082-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ff082-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff082-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ff082-128">Header</span><span class="sxs-lookup"><span data-stu-id="ff082-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff082-129"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff082-129"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff082-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff082-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff082-131">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="ff082-131">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ff082-132">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="ff082-132">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




