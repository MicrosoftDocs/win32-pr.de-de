---
title: Iremotedesktopclient Settings-Eigenschaft
description: Ruft das Einstellungs Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client ab.
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Einstellungs Eigenschaft Remotedesktopdienste
- Einstellungs Eigenschaft Remotedesktopdienste, iremotedesktopclient-Schnittstelle
- Iremotedesktopclient-Schnittstelle Remotedesktopdienste, Einstellungs Eigenschaft
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956752"
---
# <a name="iremotedesktopclientsettings-property"></a><span data-ttu-id="48fe3-106">Iremotedesktopclient:: Settings-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="48fe3-106">IRemoteDesktopClient::Settings property</span></span>

<span data-ttu-id="48fe3-107">Ruft das Einstellungs Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client ab.</span><span class="sxs-lookup"><span data-stu-id="48fe3-107">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span>

<span data-ttu-id="48fe3-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="48fe3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48fe3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="48fe3-109">Syntax</span></span>


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a><span data-ttu-id="48fe3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="48fe3-110">Property value</span></span>

<span data-ttu-id="48fe3-111">Das Einstellungs Objekt für den RDP-Client.</span><span class="sxs-lookup"><span data-stu-id="48fe3-111">The settings object for the RDP client.</span></span>

## <a name="requirements"></a><span data-ttu-id="48fe3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48fe3-112">Requirements</span></span>



| <span data-ttu-id="48fe3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48fe3-113">Requirement</span></span> | <span data-ttu-id="48fe3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="48fe3-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48fe3-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48fe3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="48fe3-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="48fe3-116">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="48fe3-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48fe3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="48fe3-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48fe3-118">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="48fe3-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="48fe3-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="48fe3-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48fe3-120"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="48fe3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="48fe3-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48fe3-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48fe3-122"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="48fe3-123">IID</span><span class="sxs-lookup"><span data-stu-id="48fe3-123">IID</span></span><br/>                      | <span data-ttu-id="48fe3-124">IID \_ iremotedesktopclient ist als 57d25668-625A-4905-BE4E-304caa13f 89c definiert.</span><span class="sxs-lookup"><span data-stu-id="48fe3-124">IID\_IRemoteDesktopClient is defined as 57D25668-625A-4905-BE4E-304CAA13F89C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48fe3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48fe3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fe3-126">**Iremotedesktopclient**</span><span class="sxs-lookup"><span data-stu-id="48fe3-126">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

