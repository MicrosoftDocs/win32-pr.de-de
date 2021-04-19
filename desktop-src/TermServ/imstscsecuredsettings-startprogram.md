---
title: Imstscsecuredsettings-Start Programm (Eigenschaft)
description: Gibt das Programm an, das auf dem Remote Server bei der Verbindung gestartet werden soll.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- StartProgram-Eigenschaft Remotedesktopdienste
- StartProgram-Eigenschaft Remotedesktopdienste, imstscsecuredsettings-Schnittstelle
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, StartProgram-Eigenschaft
- StartProgram-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, StartProgram-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346338"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="1f6f3-108">Imstscsecuredsettings:: StartProgram-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f6f3-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="1f6f3-109">Gibt das Programm an, das auf dem Remote Server bei der Verbindung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="1f6f3-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6f3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f6f3-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="1f6f3-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1f6f3-112">Property value</span></span>

<span data-ttu-id="1f6f3-113">Der Name des neuen Start Programms.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-113">The name of the new start program.</span></span> <span data-ttu-id="1f6f3-114">Die maximale Länge dieser Zeichenfolge beträgt **Max. \_ Pfad**-1 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f6f3-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1f6f3-115">Error codes</span></span>

<span data-ttu-id="1f6f3-116">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6f3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f6f3-117">Remarks</span></span>

<span data-ttu-id="1f6f3-118">Wenn der Wert dieser Eigenschaft nicht festgelegt ist, wird der Shellbefehl des Sitzungs Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="1f6f3-119">Der Shellbefehl wird aus dem folgenden Registrierungs Wert auf dem Server gelesen:</span><span class="sxs-lookup"><span data-stu-id="1f6f3-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="1f6f3-120">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**</span><span class="sxs-lookup"><span data-stu-id="1f6f3-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="1f6f3-121">Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="1f6f3-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="1f6f3-122">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1f6f3-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6f3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f6f3-123">Requirements</span></span>



| <span data-ttu-id="1f6f3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f6f3-124">Requirement</span></span> | <span data-ttu-id="1f6f3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1f6f3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6f3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f6f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6f3-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f6f3-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="1f6f3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f6f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6f3-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f6f3-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1f6f3-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1f6f3-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f6f3-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f6f3-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="1f6f3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1f6f3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f6f3-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f6f3-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="1f6f3-134">IID</span><span class="sxs-lookup"><span data-stu-id="1f6f3-134">IID</span></span><br/>                      | <span data-ttu-id="1f6f3-135">IID \_ imstscsecuredsettings ist als c9d65442-a0f9-45b2-8f73-d61d2db8cbb6 definiert.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f6f3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f6f3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6f3-137">**Imsrdpclientsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="1f6f3-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1f6f3-138">**Imstscsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="1f6f3-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





