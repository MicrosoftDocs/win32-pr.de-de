---
description: 'Enthält Eingabedaten für die IDirect3DAuthenticatedChannel9:: Configure-Methode.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214328"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="a643f-103">D3DAUTHENTICATEDCHANNEL \_ Konfigurieren der \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="a643f-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="a643f-104">Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a643f-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a643f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a643f-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="a643f-106">Member</span><span class="sxs-lookup"><span data-stu-id="a643f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a643f-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="a643f-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="a643f-108">Eine [**D3D \_ OMAC**](d3d-omac.md) -Struktur, die einen Nachrichtenauthentifizierungscode (Mac) der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a643f-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="a643f-109">Der Treiber verwendet einen AES-basierten, einstufigen CBC-MAC (OMAC), um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmember angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a643f-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="a643f-110">**Konfiguriertyp**</span><span class="sxs-lookup"><span data-stu-id="a643f-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="a643f-111">Eine GUID, die den Befehl angibt.</span><span class="sxs-lookup"><span data-stu-id="a643f-111">A GUID that specifies the command.</span></span> <span data-ttu-id="a643f-112">Eine Liste der Werte finden Sie unter [Content Protection-Befehle](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="a643f-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="a643f-113">**hchannel**</span><span class="sxs-lookup"><span data-stu-id="a643f-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="a643f-114">Ein Handle für den authentifizierten Kanal.</span><span class="sxs-lookup"><span data-stu-id="a643f-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="a643f-115">Um das Handle abzurufen, nennen Sie [**IDirect3DDevice9Video:: kreateauthentiinitiedchannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="a643f-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="a643f-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="a643f-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a643f-117">Die Abfrage Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="a643f-117">The query sequence number.</span></span> <span data-ttu-id="a643f-118">Generieren Sie zu Beginn der Sitzung eine kryptografisch sichere 32-Bit-Zufallszahl, die als Startsequenz Nummer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a643f-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="a643f-119">Erhöhen Sie die Sequenznummer für jeden Befehl um 1.</span><span class="sxs-lookup"><span data-stu-id="a643f-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a643f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a643f-120">Requirements</span></span>



| <span data-ttu-id="a643f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a643f-121">Requirement</span></span> | <span data-ttu-id="a643f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a643f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a643f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a643f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a643f-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a643f-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a643f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a643f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a643f-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a643f-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a643f-127">Header</span><span class="sxs-lookup"><span data-stu-id="a643f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a643f-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a643f-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a643f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a643f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a643f-130">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="a643f-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a643f-131">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="a643f-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




