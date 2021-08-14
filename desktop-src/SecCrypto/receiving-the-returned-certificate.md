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
ms.openlocfilehash: cb2efe504e2d09b3fae2b6d6293772bf67a3f038a5f9c43330707f541e2ba8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900966"
---
# <a name="receiving-the-returned-certificate"></a>Empfangen des zurückgegebenen Zertifikats

Wenn die Zertifizierungsstelle die Identitätsinformationen des Anfordernden überprüft hat und sich davon überzeugt hat, dass der Anfordernde der Besitzer des privaten Schlüssels ist und die Daten über diesen Anfordernden korrekt sind, erstellt die Zertifizierungsstelle ein X.509-Zertifikat, signiert es und verpackt es mit allen anderen erforderlichen Zertifikaten (z. B. dem eigenen Zertifikat der Zertifizierungsstelle) in einer Nachricht.  und sendet die Nachricht an den Anfordernden. Die Nachricht kann eine PKCS \# 7-Nachricht oder eine CMC-Antwort sein (V2-Vorlagen führen zu einer CMC-Antwort).

Die empfangende Anwendung übergibt die Nachricht an die Zertifikatregistrierungssteuerung. Die Zertifikatregistrierungssteuerung öffnet dann die Meldung und extrahiert die Zertifikate. Der Benutzer wird in einem Dialogfeld gefragt, ob der Benutzer selbstsignierte Zertifikate im Stammspeicher akzeptiert. Wenn der Benutzer das Stammzertifikat akzeptiert, werden die restlichen Zertifikate (mit Ausnahme des Zertifikats des Anfordernden) im Speicher der Zertifizierungsstelle platziert. Das Zertifikat des Anfordernden wird in dem zertifikatspeicher platziert, der vom Anfordernden in der [**MyStoreName-Eigenschaft angegeben**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) wird.

Das folgende Beispiel zeigt, wie sie die Visual Basic Scripting Edition (VBScript) und HTML auf einer Webseite verwenden, um die zurückgegebenen Zertifikate zu empfangen und zu speichern.


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



 

 
