---
description: Bei der Verwendung des Kerberos-Security Support Provider (SSP) ist Vorsicht geboten, wenn die Interoperabilität mit GSSAPI erforderlich ist.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: SSPI/Kerberos-Interoperabilität mit GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749600"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="c9da3-103">SSPI/Kerberos-Interoperabilität mit GSSAPI</span><span class="sxs-lookup"><span data-stu-id="c9da3-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="c9da3-104">Bei der Verwendung des [*Kerberos*](../secgloss/k-gly.md) - [*Security Support Provider*](../secgloss/s-gly.md) (SSP) ist Vorsicht geboten, wenn die Interoperabilität mit GSSAPI erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c9da3-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="c9da3-105">Die folgenden Code Konventionen ermöglichen die Interoperabilität mit GSSAPI-basierten Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="c9da3-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="c9da3-106">Windows-kompatible Namen</span><span class="sxs-lookup"><span data-stu-id="c9da3-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="c9da3-107">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="c9da3-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="c9da3-108">Nachrichten Integrität und Datenschutz</span><span class="sxs-lookup"><span data-stu-id="c9da3-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="c9da3-109">Beispielcode finden Sie im Platform Software Development Kit (SDK) unter Samples \\ Security \\ SSPI \\ GSS.</span><span class="sxs-lookup"><span data-stu-id="c9da3-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="c9da3-110">Außerdem wird das entsprechende Unix-Beispiel in den Kerberos-Verteilungen mit und heimdal, GSS-Client und-Server, verteilt.</span><span class="sxs-lookup"><span data-stu-id="c9da3-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="c9da3-111">Windows-Compatible Namen</span><span class="sxs-lookup"><span data-stu-id="c9da3-111">Windows-Compatible Names</span></span>

<span data-ttu-id="c9da3-112">GSSAPI-Funktionen verwenden ein Namensformat, das als GSS NT-Dienst Name bezeichnet wird, \_ \_ \_ wie in der RFC angegeben.</span><span class="sxs-lookup"><span data-stu-id="c9da3-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="c9da3-113">Beispielsweise sample@host.dom.com ist ein Name, der in einer GSSAPI-basierten Anwendung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9da3-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="c9da3-114">Das Windows-Betriebssystem erkennt das Format des GSS \_ NT \_ \_ -Dienst namens nicht, und der vollständige [*Dienst Prinzipal Name*](../secgloss/s-gly.md)muss beispielsweise sample/host.dom.com@REALM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9da3-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="c9da3-115">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="c9da3-115">Authentication</span></span>

<span data-ttu-id="c9da3-116">Die Authentifizierung wird in der Regel verarbeitet, wenn eine Verbindung zwischen einem Client und einem Server eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="c9da3-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="c9da3-117">In diesem Beispiel verwendet der Client die [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI), und der Server verwendet GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="c9da3-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="c9da3-118">**So richten Sie die Authentifizierung im SSPI-Client ein**</span><span class="sxs-lookup"><span data-stu-id="c9da3-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="c9da3-119">Erhalten Sie ausgehende [*Anmelde*](../secgloss/c-gly.md) Informationen mithilfe von [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span><span class="sxs-lookup"><span data-stu-id="c9da3-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="c9da3-120">Erstellen Sie einen Dienstnamen mit dem **GSS- \_ Import \_ Namen ()** , und rufen Sie eingehende Anmelde Informationen mithilfe von **GSS get \_ \_ -** Anmelde Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="c9da3-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="c9da3-121">Senden Sie ein Authentifizierungs Token, das mithilfe von [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9da3-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="c9da3-122">Sendet das Token an den Server.</span><span class="sxs-lookup"><span data-stu-id="c9da3-122">Send the token to the server.</span></span>

<span data-ttu-id="c9da3-123">**So richten Sie die Authentifizierung auf dem GSSAPI-Server ein**</span><span class="sxs-lookup"><span data-stu-id="c9da3-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="c9da3-124">Analysieren Sie die Meldung vom Client, um das Sicherheits Token zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c9da3-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="c9da3-125">Verwenden Sie die **GSS \_ Accept \_ sec- \_ Kontext** Funktion, und übergeben Sie das Token als Argument.</span><span class="sxs-lookup"><span data-stu-id="c9da3-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="c9da3-126">Analysieren Sie die Meldung vom Server, um das Sicherheits Token zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c9da3-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="c9da3-127">Übergeben Sie dieses Sicherheits Token an [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="c9da3-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="c9da3-128">Senden Sie ein Antwort Token an den Client.</span><span class="sxs-lookup"><span data-stu-id="c9da3-128">Send a response token to the client.</span></span>

    <span data-ttu-id="c9da3-129">Die **GSS \_ Accept \_ sec- \_ Kontext** Funktion kann ein Token zurückgeben, das Sie an den Client zurücksenden können.</span><span class="sxs-lookup"><span data-stu-id="c9da3-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="c9da3-130">Wenn der Vorgang fortgesetzt werden muss, senden Sie ein Antwort Token an den Server. Andernfalls ist das Einrichten der Authentifizierung fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="c9da3-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="c9da3-131">Wenn der Vorgang fortgesetzt werden muss, warten Sie auf das nächste Token vom Client. Andernfalls ist das Einrichten der Authentifizierung fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="c9da3-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="c9da3-132">Nachrichten Integrität und Datenschutz</span><span class="sxs-lookup"><span data-stu-id="c9da3-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="c9da3-133">Die meisten GSSAPI-basierten Anwendungen verwenden die **GSS \_ Wrap** -Funktion, um eine Nachricht vor dem senden zu signieren.</span><span class="sxs-lookup"><span data-stu-id="c9da3-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="c9da3-134">Umgekehrt überprüft die **GSS-Funktion \_ Unwrap** die Signatur.</span><span class="sxs-lookup"><span data-stu-id="c9da3-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="c9da3-135">**GSS \_ Wrap** ist in Version 2,0 der API verfügbar und wird nun häufig verwendet und in Internet Standards angegeben, die die Verwendung der GSSAPI zum Hinzufügen von Sicherheit zu Protokollen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c9da3-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="c9da3-136">Früher wurden die Funktionen "GSS **signmessage** " und " **sealmessage** " für Nachrichten [*Integrität*](../secgloss/i-gly.md) und [*Datenschutz*](../secgloss/p-gly.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9da3-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="c9da3-137">**GSS \_ Wrap** und **GSS \_ Unwrap** werden sowohl für die Integrität als auch für den Datenschutz verwendet, wobei der Datenschutz durch den Wert des Arguments "conf- \_ Flag" gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="c9da3-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="c9da3-138">Wenn ein GSSAPI-basiertes Protokoll für die Verwendung der **GSS \_ get \_ MIC** -und **GSS \_ Verify \_ MIC** -Funktionen angegeben wird, sind die richtigen SSPI-Funktionen " [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) " und " [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)".</span><span class="sxs-lookup"><span data-stu-id="c9da3-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="c9da3-139">Beachten Sie, dass **makesignature** und **VerifySignature** nicht mit **GSS- \_ Wrap** interagieren, wenn das conf- \_ Flag auf 0 (null) festgelegt ist, oder mit **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="c9da3-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="c9da3-140">Das gleiche gilt für das Kombinieren von [**verschlüsselungsmessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) , der nur für die Signatur festgelegt ist, und **GSS \_ Verify \_ MIC**.</span><span class="sxs-lookup"><span data-stu-id="c9da3-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="c9da3-141">Verwenden Sie die Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) oder [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) nicht, wenn **GSS \_ Wrap** und **GSS \_ Unwrap** für aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c9da3-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="c9da3-142">Die SSPI-Entsprechung zu **GSS \_ Wrap** ist [**Verschlüsselungs Nachricht (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) für Integrität und Datenschutz.</span><span class="sxs-lookup"><span data-stu-id="c9da3-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="c9da3-143">Das folgende Beispiel zeigt die Verwendung von " [**verschlüsseltmessage" (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) zum Signieren von Daten, die durch **GSS \_ Unwrap** überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c9da3-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="c9da3-144">Im SSPI-Client:</span><span class="sxs-lookup"><span data-stu-id="c9da3-144">In the SSPI client:</span></span>


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



<span data-ttu-id="c9da3-145">Auf dem GSSAPI-Server:</span><span class="sxs-lookup"><span data-stu-id="c9da3-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="c9da3-146">Die SSPI-Entsprechung zu **GSS \_ Unwrap** ist [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="c9da3-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="c9da3-147">Im folgenden Beispiel wird gezeigt, wie mit **DecryptMessage (Kerberos)** Daten entschlüsselt werden, die mit **GSS- \_ Wrap** verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="c9da3-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="c9da3-148">Auf dem GSSAPI-Server:</span><span class="sxs-lookup"><span data-stu-id="c9da3-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="c9da3-149">Im SSPI-Client:</span><span class="sxs-lookup"><span data-stu-id="c9da3-149">In the SSPI client:</span></span>


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 
