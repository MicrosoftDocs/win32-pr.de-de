---
description: 'Enthält die Antwort auf einen aufzurufenden Befehl der IDirect3DAuthenticatedChannel9:: Configure-Methode.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342538"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a><span data-ttu-id="ef7e4-103">D3DAUTHENTICATEDCHANNEL \_ Konfigurieren der \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="ef7e4-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_OUTPUT structure</span></span>

<span data-ttu-id="ef7e4-104">Enthält die Antwort auf einen aufzurufenden Befehl der [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-104">Contains the response to a call to the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef7e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef7e4-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ef7e4-106">Member</span><span class="sxs-lookup"><span data-stu-id="ef7e4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef7e4-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="ef7e4-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e4-108">Eine [**D3D \_ OMAC**](d3d-omac.md) -Struktur, die einen Nachrichtenauthentifizierungscode (Mac) der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="ef7e4-109">Der Treiber verwendet einen AES-basierten, einstufigen CBC-MAC (OMAC), um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmember angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="ef7e4-110">**Konfiguriertyp**</span><span class="sxs-lookup"><span data-stu-id="ef7e4-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e4-111">Eine GUID, die den Befehl angibt.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-111">A GUID that specifies the command.</span></span> <span data-ttu-id="ef7e4-112">Eine Liste der Werte finden Sie unter [Content Protection-Befehle](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="ef7e4-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef7e4-113">**hchannel**</span><span class="sxs-lookup"><span data-stu-id="ef7e4-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e4-114">Ein Handle für den authentifizierten Kanal.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="ef7e4-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="ef7e4-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e4-116">Die Sequenznummer des Befehls.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-116">The command sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="ef7e4-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="ef7e4-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e4-118">Der Ergebniscode für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-118">The result code for the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef7e4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef7e4-119">Remarks</span></span>

<span data-ttu-id="ef7e4-120">Für die Member "configure **Retype**", " **hchannel**" und " **SequenceNumber** " verwendet der Treiber dieselben Werte, die von der Anwendung in der [**D3DAUTHENTICATEDCHANNEL- \_ \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-120">For the **ConfigureType**, **hChannel**, and **SequenceNumber** members, the driver uses the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure.</span></span> <span data-ttu-id="ef7e4-121">Die Anwendung sollte überprüfen, ob diese Werte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ef7e4-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef7e4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef7e4-122">Requirements</span></span>



| <span data-ttu-id="ef7e4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef7e4-123">Requirement</span></span> | <span data-ttu-id="ef7e4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ef7e4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7e4-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef7e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7e4-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef7e4-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef7e4-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef7e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7e4-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef7e4-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ef7e4-129">Header</span><span class="sxs-lookup"><span data-stu-id="ef7e4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef7e4-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef7e4-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef7e4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef7e4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef7e4-132">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="ef7e4-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ef7e4-133">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="ef7e4-133">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




