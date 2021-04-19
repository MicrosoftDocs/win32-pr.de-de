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
# <a name="receiving-the-returned-certificate"></a>Empfangen des zurückgegebenen Zertifikats

Wenn die Zertifizierungsstelle (Certification Authority, ca) die Identitätsinformationen des Anforderers überprüft hat und erfüllt ist, dass die anfordernde Person der Besitzer des privaten Schlüssels ist und dass die Daten zu diesem Anforderer korrekt sind, die Zertifizierungsstelle erstellt ein X. 509-Zertifikat, signiert Sie, verpackt Sie mit allen anderen benötigten Zertifikaten (z. b. dem Zertifikat der Zertifizierungsstelle) in einer Nachricht und sendet die Nachricht an den Anforderer. Bei der Nachricht kann es sich um eine PKCS \# 7-Nachricht oder eine CMC-Antwort handeln (v2-Vorlagen führen zu einer CMC-Antwort).

Die empfangende Anwendung übergibt die Nachricht an die Zertifikat Registrierungs Steuerung. Die Zertifikat Registrierungs Steuerung öffnet dann die Nachricht und extrahiert die Zertifikate. Der Benutzer wird in einem Dialogfeld gefragt, ob der Benutzer selbst signierte Zertifikate im Speicher "root" annimmt. Wenn der Benutzer das Stamm Zertifikat annimmt, werden die restlichen Zertifikate (mit Ausnahme des Zertifikats der anfordernden Person) im Speicher der Zertifizierungsstelle abgelegt. Das Zertifikat der Anforderer wird in den Zertifikat Speicher eingefügt, der von der anfordernden Person in der [**mystorename**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) -Eigenschaft angegeben wird.

Im folgenden Beispiel wird gezeigt, wie die Visual Basic Scripting Edition (VBScript) und HTML auf einer Webseite zum empfangen und Speichern der zurückgegebenen Zertifikate verwendet werden.


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



 

 
