---
description: Enthält Eingabedaten für den D3DAUTHENTICATEDCONFIGURE- \_ Befehl verschlüsselungszugreif barkeit.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339722"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="a79f4-103">D3DAUTHENTICATEDCHANNEL \_ Konfiguration reuncompressedencryption-Struktur</span><span class="sxs-lookup"><span data-stu-id="a79f4-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="a79f4-104">Enthält Eingabedaten für den [**D3DAUTHENTICATEDCONFIGURE-Befehl \_ verschlüsselungszugreif**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) barkeit.</span><span class="sxs-lookup"><span data-stu-id="a79f4-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="a79f4-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="a79f4-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="a79f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a79f4-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="a79f4-107">Member</span><span class="sxs-lookup"><span data-stu-id="a79f4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a79f4-108">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="a79f4-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="a79f4-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a79f4-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a79f4-110">**Verschlüsselungs-GUID**</span><span class="sxs-lookup"><span data-stu-id="a79f4-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="a79f4-111">Eine GUID, die den Typ der anzuwendenden Verschlüsselung angibt.</span><span class="sxs-lookup"><span data-stu-id="a79f4-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a79f4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a79f4-112">Requirements</span></span>



| <span data-ttu-id="a79f4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a79f4-113">Requirement</span></span> | <span data-ttu-id="a79f4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a79f4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a79f4-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a79f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a79f4-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a79f4-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a79f4-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a79f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a79f4-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a79f4-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a79f4-119">Header</span><span class="sxs-lookup"><span data-stu-id="a79f4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a79f4-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a79f4-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a79f4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a79f4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a79f4-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="a79f4-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a79f4-123">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="a79f4-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




