---
description: Wählt ein Client Zertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Iwinhttprequest:: setclientcertificate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347208"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="39b8a-103">Iwinhttprequest:: setclientcertificate-Methode</span><span class="sxs-lookup"><span data-stu-id="39b8a-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="39b8a-104">Mit der **setclientcertificate** -Methode wird ein Client Zertifikat ausgewählt, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39b8a-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39b8a-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="39b8a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39b8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b8a-107">*ClientCertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39b8a-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b8a-108">Gibt den Speicherort, den [*Zertifikat Speicher*](glossary.md)und den Betreff eines Client Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="39b8a-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b8a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39b8a-109">Return value</span></span>

<span data-ttu-id="39b8a-110">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="39b8a-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b8a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39b8a-111">Remarks</span></span>

<span data-ttu-id="39b8a-112">Die im *ClientCertificate* -Parameter angegebene Zeichenfolge besteht aus dem Zertifikat Speicherort, dem Zertifikat Speicher und dem Antragsteller Namen, die durch umgekehrte Schrägstriche getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="39b8a-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="39b8a-113">Weitere Informationen zu den Komponenten der Zertifikat Zeichenfolge finden Sie unter [Client Zertifikate](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="39b8a-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="39b8a-114">Der Name und Speicherort des Zertifikat Speicher sind optional.</span><span class="sxs-lookup"><span data-stu-id="39b8a-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="39b8a-115">Wenn Sie jedoch einen Zertifikat Speicher angeben, müssen Sie auch den Speicherort dieses Zertifikat Speicher angeben.</span><span class="sxs-lookup"><span data-stu-id="39b8a-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="39b8a-116">Der Standard Speicherort ist aktueller \_ Benutzer und der Standard Zertifikat Speicher "My".</span><span class="sxs-lookup"><span data-stu-id="39b8a-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="39b8a-117">Ein leerer Betreff gibt an, dass das erste Zertifikat im Zertifikat Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39b8a-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="39b8a-118">Rufen Sie **setclientcertificate** auf, um ein Zertifikat auszuwählen, bevor [**Sie Send**](iwinhttprequest-send.md) aufrufen, um die Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="39b8a-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="39b8a-119">Microsoft Windows HTTP-Dienste (WinHTTP) stellen keine Client Zertifikate für Proxy Server bereit, die Zertifikate für die Authentifizierung anfordern.</span><span class="sxs-lookup"><span data-stu-id="39b8a-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="39b8a-120">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="39b8a-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="39b8a-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39b8a-121">Examples</span></span>

<span data-ttu-id="39b8a-122">Im folgenden Skript Beispiel wird gezeigt, wie Sie ein Client Zertifikat auswählen, das mit einer Anforderung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39b8a-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="39b8a-123">Ein Zertifikat mit dem Betreff "My Middle-Tier Certificate" wird aus dem Zertifikat Speicher "persönlich" in der Registrierung unter **HKEY \_ local \_ Machine** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="39b8a-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="39b8a-124">Da dieses Codebeispiel spezifisch für Microsoft JScript ist, das den umgekehrten Schrägstrich als Escapezeichen verwendet, sind zwei aufeinander folgende umgekehrte Schrägstriche erforderlich, um die Komponenten der Zertifikat Zeichenfolge zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="39b8a-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="39b8a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39b8a-125">Requirements</span></span>



| <span data-ttu-id="39b8a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39b8a-126">Requirement</span></span> | <span data-ttu-id="39b8a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="39b8a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b8a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39b8a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39b8a-129">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39b8a-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="39b8a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39b8a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39b8a-131">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39b8a-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="39b8a-132">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="39b8a-132">Redistributable</span></span><br/>          | <span data-ttu-id="39b8a-133">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="39b8a-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="39b8a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="39b8a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39b8a-135"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39b8a-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="39b8a-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39b8a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="39b8a-137"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39b8a-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="39b8a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="39b8a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b8a-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b8a-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="39b8a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39b8a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b8a-141">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="39b8a-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="39b8a-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="39b8a-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="39b8a-143">SSL in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="39b8a-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="39b8a-144">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="39b8a-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




