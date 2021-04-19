---
title: Imsrdpclientshell rdpfilecontents (Eigenschaft)
description: Gibt den Inhalt der Remotedesktopprotokoll Datei (RDP) an, die von Remotedesktop Webzugriff (RD-Webzugriff) oder einem anderen Webportal gestartet werden soll, oder ruft ihn ab.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Rdpfilecontents-Eigenschaft Remotedesktopdienste
- Rdpfilecontents-Eigenschaft Remotedesktopdienste, imsrdpclientshell-Schnittstelle
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, rdpfilecontents-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342226"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="ec0d1-106">Imsrdpclientshell:: rdpfilecontents-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec0d1-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="ec0d1-107">Gibt den Inhalt der Remotedesktopprotokoll Datei (RDP) an, die von Remotedesktop Webzugriff (RD-Webzugriff) oder einem anderen Webportal gestartet werden soll, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="ec0d1-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec0d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec0d1-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="ec0d1-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ec0d1-110">Property value</span></span>

<span data-ttu-id="ec0d1-111">Gibt den Inhalt der RDP-Datei an, die über das Webportal gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0d1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec0d1-112">Requirements</span></span>



| <span data-ttu-id="ec0d1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec0d1-113">Requirement</span></span> | <span data-ttu-id="ec0d1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ec0d1-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0d1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec0d1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0d1-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec0d1-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ec0d1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec0d1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0d1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec0d1-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ec0d1-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ec0d1-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec0d1-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec0d1-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec0d1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ec0d1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec0d1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec0d1-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec0d1-123">IID</span><span class="sxs-lookup"><span data-stu-id="ec0d1-123">IID</span></span><br/>                      | <span data-ttu-id="ec0d1-124">IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ec0d1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec0d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0d1-126">**Imsrdpclientshell**</span><span class="sxs-lookup"><span data-stu-id="ec0d1-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





