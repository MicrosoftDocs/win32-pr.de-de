---
description: Legt die aktuelle Richtlinie für die automatische Anmeldung fest.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'Iwinhttprequest:: "abtautologonpolicy"-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350382"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="7fd33-103">Iwinhttprequest:: "abtautologonpolicy"-Methode</span><span class="sxs-lookup"><span data-stu-id="7fd33-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="7fd33-104">Die **setautologonpolicy** -Methode legt die aktuelle [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md)fest.</span><span class="sxs-lookup"><span data-stu-id="7fd33-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fd33-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="7fd33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fd33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd33-107">*Autologonpolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fd33-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd33-108">Gibt die aktuelle Richtlinie für die automatische Anmeldung an.</span><span class="sxs-lookup"><span data-stu-id="7fd33-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd33-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fd33-109">Return value</span></span>

<span data-ttu-id="7fd33-110">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="7fd33-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd33-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fd33-111">Remarks</span></span>

<span data-ttu-id="7fd33-112">Die Standard Richtlinie ist [**autologonpolicy \_ onlyifbypassproxy**](winhttprequestautologonpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7fd33-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="7fd33-113">Rufen Sie **setautologonpolicy** auf, um die automatische Anmelde Richtlinie festzulegen, bevor [**Sie Send**](iwinhttprequest-send.md) aufrufen, um die Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="7fd33-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="7fd33-114">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="7fd33-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7fd33-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fd33-115">Examples</span></span>

<span data-ttu-id="7fd33-116">Im folgenden Beispielskript wird veranschaulicht, wie die Richtlinie für die automatische Anmeldung so festgelegt wird, dass NTLM niemals verwendet oder die Authentifizierung automatisch ausgehandelt</span><span class="sxs-lookup"><span data-stu-id="7fd33-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="7fd33-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fd33-117">Requirements</span></span>



| <span data-ttu-id="7fd33-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fd33-118">Requirement</span></span> | <span data-ttu-id="7fd33-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd33-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd33-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fd33-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd33-121">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fd33-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7fd33-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fd33-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd33-123">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fd33-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7fd33-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7fd33-124">Redistributable</span></span><br/>          | <span data-ttu-id="7fd33-125">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7fd33-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7fd33-126">IDL</span><span class="sxs-lookup"><span data-stu-id="7fd33-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fd33-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fd33-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="7fd33-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7fd33-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="7fd33-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fd33-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="7fd33-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd33-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd33-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd33-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7fd33-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fd33-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd33-133">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="7fd33-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="7fd33-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7fd33-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="7fd33-135">Authentifizierung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7fd33-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="7fd33-136">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="7fd33-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




