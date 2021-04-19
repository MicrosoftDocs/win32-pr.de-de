---
title: Session. identifigingmethode (WSManDisp. h)
description: Fragt einen Remote Computer ab, um zu bestimmen, ob das WS-Management Protokoll unterstützt wird.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Methoden Windows-Remoteverwaltung identifizieren
- Methoden Windows-Remoteverwaltung identifizieren, Sitzungs Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, identifizmethode
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342874"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="80a94-106">Session. identifizmethode</span><span class="sxs-lookup"><span data-stu-id="80a94-106">Session.Identify method</span></span>

<span data-ttu-id="80a94-107">Die **Session. identifigingmethode** fragt einen Remote Computer ab, um zu bestimmen, ob das WS-Management Protokoll unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="80a94-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="80a94-108">Weitere Informationen finden Sie [unter erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="80a94-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80a94-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="80a94-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="80a94-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80a94-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a94-111">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="80a94-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="80a94-112">Um die Anforderung im authentifizierten Modus zu senden, verwenden Sie die Authentifizierungs Konstante aus der **wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="80a94-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="80a94-113">Verwenden Sie zum Senden im nicht authentifizierten Modus **wsmanflagusenoauthentication**.</span><span class="sxs-lookup"><span data-stu-id="80a94-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="80a94-114">Weitere Informationen finden Sie unter [**Authentifizierungs Konstanten**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="80a94-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a94-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80a94-115">Return value</span></span>

<span data-ttu-id="80a94-116">Eine XML-Zeichenfolge, die die WS-Management Protokollversion, den Hersteller des Betriebssystems und, wenn die Anforderung authentifiziert wurde, die Betriebssystemversion angibt.</span><span class="sxs-lookup"><span data-stu-id="80a94-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a94-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80a94-117">Remarks</span></span>

<span data-ttu-id="80a94-118">**Session. Identifizierung** basiert auf dem [WS-Management-Protokoll](ws-management-protocol.md) Vorgang, der als wsmanidentity definiert ist.</span><span class="sxs-lookup"><span data-stu-id="80a94-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="80a94-119">Dies wird im SOAP-Paket wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="80a94-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="80a94-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80a94-120">Examples</span></span>

<span data-ttu-id="80a94-121">Das folgende VBScript-Beispiel sendet eine nicht authentifizierte Identifizierungs Anforderung an den Remote Computer mit dem Namen Remote in derselben Domäne.</span><span class="sxs-lookup"><span data-stu-id="80a94-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="80a94-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80a94-122">Requirements</span></span>



| <span data-ttu-id="80a94-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80a94-123">Requirement</span></span> | <span data-ttu-id="80a94-124">Wert</span><span class="sxs-lookup"><span data-stu-id="80a94-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a94-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80a94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="80a94-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80a94-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="80a94-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80a94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="80a94-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80a94-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="80a94-129">Header</span><span class="sxs-lookup"><span data-stu-id="80a94-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="80a94-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a94-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="80a94-131">IDL</span><span class="sxs-lookup"><span data-stu-id="80a94-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80a94-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80a94-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="80a94-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="80a94-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="80a94-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="80a94-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="80a94-135">DLL</span><span class="sxs-lookup"><span data-stu-id="80a94-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80a94-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80a94-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80a94-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80a94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a94-138">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="80a94-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="80a94-139">**Iwsmansession:: Identifizierung**</span><span class="sxs-lookup"><span data-stu-id="80a94-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="80a94-140">WS-Verwaltungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="80a94-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





