---
description: Erläutert, wie eine Anwendung ein Zertifikat empfängt.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Empfangen des zurückgegebenen Zertifikats
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362927"
---
# <a name="receiving-the-returned-certificate"></a><span data-ttu-id="07ab4-103">Empfangen des zurückgegebenen Zertifikats</span><span class="sxs-lookup"><span data-stu-id="07ab4-103">Receiving the Returned Certificate</span></span>

<span data-ttu-id="07ab4-104">Wenn die Zertifizierungsstelle (Certification Authority, ca) die Identitätsinformationen des Anforderers überprüft hat und erfüllt ist, dass die anfordernde Person der Besitzer des privaten Schlüssels ist und dass die Daten zu diesem Anforderer korrekt sind, die Zertifizierungsstelle erstellt ein X. 509-Zertifikat, signiert Sie, verpackt Sie mit allen anderen benötigten Zertifikaten (z. b. dem Zertifikat der Zertifizierungsstelle) in einer Nachricht und sendet die Nachricht an den Anforderer.</span><span class="sxs-lookup"><span data-stu-id="07ab4-104">When the certification authority (CA) has verified the requester's identity information and is satisfied that the requester is the owner of the private key and that the data about that requester is accurate, the CA constructs an X.509 certificate, signs it, packages it with any other needed certificates (such as the CA's own certificate) in a message, and sends the message to the requester.</span></span> <span data-ttu-id="07ab4-105">Bei der Nachricht kann es sich um eine PKCS \# 7-Nachricht oder eine CMC-Antwort handeln (v2-Vorlagen führen zu einer CMC-Antwort).</span><span class="sxs-lookup"><span data-stu-id="07ab4-105">The message can be a PKCS \#7 message or a CMC response (V2 templates result in a CMC response).</span></span>

<span data-ttu-id="07ab4-106">Die empfangende Anwendung übergibt die Nachricht an die Zertifikat Registrierungs Steuerung.</span><span class="sxs-lookup"><span data-stu-id="07ab4-106">The receiving application passes the message to the Certificate Enrollment Control.</span></span> <span data-ttu-id="07ab4-107">Die Zertifikat Registrierungs Steuerung öffnet dann die Nachricht und extrahiert die Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="07ab4-107">The Certificate Enrollment Control then opens the message and extracts the certificates.</span></span> <span data-ttu-id="07ab4-108">Der Benutzer wird in einem Dialogfeld gefragt, ob der Benutzer selbst signierte Zertifikate im Speicher "root" annimmt.</span><span class="sxs-lookup"><span data-stu-id="07ab4-108">The user is prompted with a dialog box asking whether the user will accept self-signed certificates in the "Root" store.</span></span> <span data-ttu-id="07ab4-109">Wenn der Benutzer das Stamm Zertifikat annimmt, werden die restlichen Zertifikate (mit Ausnahme des Zertifikats der anfordernden Person) im Speicher der Zertifizierungsstelle abgelegt.</span><span class="sxs-lookup"><span data-stu-id="07ab4-109">If the user accepts the root certificate, the rest of the certificates (except for the requester's certificate) are placed in the "CA" store.</span></span> <span data-ttu-id="07ab4-110">Das Zertifikat der Anforderer wird in den Zertifikat Speicher eingefügt, der von der anfordernden Person in der [**mystorename**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07ab4-110">The requester's certificate is placed in the certificate store specified by the requester in the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span>

<span data-ttu-id="07ab4-111">Im folgenden Beispiel wird gezeigt, wie die Visual Basic Scripting Edition (VBScript) und HTML auf einer Webseite zum empfangen und Speichern der zurückgegebenen Zertifikate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07ab4-111">The following example shows how to use the Visual Basic Scripting Edition (VBScript) and HTML in a webpage to receive and store the returned certificates.</span></span>


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
