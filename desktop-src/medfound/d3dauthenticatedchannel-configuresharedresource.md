---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ SharedResource-Befehl.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344017"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="6b075-103">D3DAUTHENTICATEDCHANNEL- \_ Struktur konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6b075-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="6b075-104">Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ SharedResource**](d3dauthenticatedconfigure-sharedresource.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="6b075-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="6b075-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="6b075-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b075-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b075-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="6b075-107">Member</span><span class="sxs-lookup"><span data-stu-id="6b075-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b075-108">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="6b075-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="6b075-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="6b075-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="6b075-110">**Processidentifertype**</span><span class="sxs-lookup"><span data-stu-id="6b075-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="6b075-111">Ein [**D3DAUTHENTICATEDCHANNEL \_ processidentifiertype**](d3dauthenticatedchannel-processidentifiertype.md) -Wert, der den Typ des Prozesses angibt.</span><span class="sxs-lookup"><span data-stu-id="6b075-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="6b075-112">Legen Sie diesen Member auf **processidtype \_ DWM** fest, um den Desktopfenster-Manager-Prozess (DWM) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b075-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="6b075-113">Legen Sie diesen Member andernfalls auf **processidtype \_ handle** fest, und legen Sie den **ProcessHandle** -Member auf ein gültiges Handle fest.</span><span class="sxs-lookup"><span data-stu-id="6b075-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="6b075-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="6b075-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6b075-115">Ein Prozess handle.</span><span class="sxs-lookup"><span data-stu-id="6b075-115">A process handle.</span></span> <span data-ttu-id="6b075-116">Wenn das **processidentifier** -Element **\_ mit dem processtidtype-handle** gleich ist, gibt das **ProcessHandle** -Member ein Handle für einen Prozess an.</span><span class="sxs-lookup"><span data-stu-id="6b075-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="6b075-117">Andernfalls wird der Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6b075-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6b075-118">**Allowaccess**</span><span class="sxs-lookup"><span data-stu-id="6b075-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="6b075-119">**True** gibt an, dass der angegebene Prozess Zugriff auf eingeschränkte freigegebene Ressourcen hat.</span><span class="sxs-lookup"><span data-stu-id="6b075-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b075-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b075-120">Requirements</span></span>



| <span data-ttu-id="6b075-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b075-121">Requirement</span></span> | <span data-ttu-id="6b075-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6b075-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b075-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b075-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b075-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b075-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6b075-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b075-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b075-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b075-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b075-127">Header</span><span class="sxs-lookup"><span data-stu-id="6b075-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b075-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b075-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b075-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b075-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b075-130">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="6b075-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="6b075-131">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="6b075-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




