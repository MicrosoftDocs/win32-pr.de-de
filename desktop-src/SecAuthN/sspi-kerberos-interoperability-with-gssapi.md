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
# <a name="sspikerberos-interoperability-with-gssapi"></a>SSPI/Kerberos-Interoperabilität mit GSSAPI

Bei der Verwendung des [*Kerberos*](../secgloss/k-gly.md) - [*Security Support Provider*](../secgloss/s-gly.md) (SSP) ist Vorsicht geboten, wenn die Interoperabilität mit GSSAPI erforderlich ist. Die folgenden Code Konventionen ermöglichen die Interoperabilität mit GSSAPI-basierten Anwendungen:

-   [Windows-kompatible Namen](#windows-compatible-names)
-   [Authentifizierung](#authentication)
-   [Nachrichten Integrität und Datenschutz](#message-integrity-and-privacy)

Beispielcode finden Sie im Platform Software Development Kit (SDK) unter Samples \\ Security \\ SSPI \\ GSS. Außerdem wird das entsprechende Unix-Beispiel in den Kerberos-Verteilungen mit und heimdal, GSS-Client und-Server, verteilt.

## <a name="windows-compatible-names"></a>Windows-Compatible Namen

GSSAPI-Funktionen verwenden ein Namensformat, das als GSS NT-Dienst Name bezeichnet wird, \_ \_ \_ wie in der RFC angegeben. Beispielsweise sample@host.dom.com ist ein Name, der in einer GSSAPI-basierten Anwendung verwendet werden kann. Das Windows-Betriebssystem erkennt das Format des GSS \_ NT \_ \_ -Dienst namens nicht, und der vollständige [*Dienst Prinzipal Name*](../secgloss/s-gly.md)muss beispielsweise sample/host.dom.com@REALM verwendet werden.

## <a name="authentication"></a>Authentifizierung

Die Authentifizierung wird in der Regel verarbeitet, wenn eine Verbindung zwischen einem Client und einem Server eingerichtet wird. In diesem Beispiel verwendet der Client die [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI), und der Server verwendet GSSAPI.

**So richten Sie die Authentifizierung im SSPI-Client ein**

1.  Erhalten Sie ausgehende [*Anmelde*](../secgloss/c-gly.md) Informationen mithilfe von [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Erstellen Sie einen Dienstnamen mit dem **GSS- \_ Import \_ Namen ()** , und rufen Sie eingehende Anmelde Informationen mithilfe von **GSS get \_ \_ -** Anmelde Informationen ab.
3.  Senden Sie ein Authentifizierungs Token, das mithilfe von [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)an den Server gesendet wird.
4.  Sendet das Token an den Server.

**So richten Sie die Authentifizierung auf dem GSSAPI-Server ein**

1.  Analysieren Sie die Meldung vom Client, um das Sicherheits Token zu extrahieren. Verwenden Sie die **GSS \_ Accept \_ sec- \_ Kontext** Funktion, und übergeben Sie das Token als Argument.
2.  Analysieren Sie die Meldung vom Server, um das Sicherheits Token zu extrahieren. Übergeben Sie dieses Sicherheits Token an [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
3.  Senden Sie ein Antwort Token an den Client.

    Die **GSS \_ Accept \_ sec- \_ Kontext** Funktion kann ein Token zurückgeben, das Sie an den Client zurücksenden können.

4.  Wenn der Vorgang fortgesetzt werden muss, senden Sie ein Antwort Token an den Server. Andernfalls ist das Einrichten der Authentifizierung fertiggestellt.
5.  Wenn der Vorgang fortgesetzt werden muss, warten Sie auf das nächste Token vom Client. Andernfalls ist das Einrichten der Authentifizierung fertiggestellt.

## <a name="message-integrity-and-privacy"></a>Nachrichten Integrität und Datenschutz

Die meisten GSSAPI-basierten Anwendungen verwenden die **GSS \_ Wrap** -Funktion, um eine Nachricht vor dem senden zu signieren. Umgekehrt überprüft die **GSS-Funktion \_ Unwrap** die Signatur. **GSS \_ Wrap** ist in Version 2,0 der API verfügbar und wird nun häufig verwendet und in Internet Standards angegeben, die die Verwendung der GSSAPI zum Hinzufügen von Sicherheit zu Protokollen beschreiben. Früher wurden die Funktionen "GSS **signmessage** " und " **sealmessage** " für Nachrichten [*Integrität*](../secgloss/i-gly.md) und [*Datenschutz*](../secgloss/p-gly.md)verwendet. **GSS \_ Wrap** und **GSS \_ Unwrap** werden sowohl für die Integrität als auch für den Datenschutz verwendet, wobei der Datenschutz durch den Wert des Arguments "conf- \_ Flag" gesteuert wird.

Wenn ein GSSAPI-basiertes Protokoll für die Verwendung der **GSS \_ get \_ MIC** -und **GSS \_ Verify \_ MIC** -Funktionen angegeben wird, sind die richtigen SSPI-Funktionen " [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) " und " [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)". Beachten Sie, dass **makesignature** und **VerifySignature** nicht mit **GSS- \_ Wrap** interagieren, wenn das conf- \_ Flag auf 0 (null) festgelegt ist, oder mit **GSS \_ Wrap**. Das gleiche gilt für das Kombinieren von [**verschlüsselungsmessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) , der nur für die Signatur festgelegt ist, und **GSS \_ Verify \_ MIC**.

> [!Note]  
> Verwenden Sie die Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) oder [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) nicht, wenn **GSS \_ Wrap** und **GSS \_ Unwrap** für aufgerufen werden.

 

Die SSPI-Entsprechung zu **GSS \_ Wrap** ist [**Verschlüsselungs Nachricht (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) für Integrität und Datenschutz.

Das folgende Beispiel zeigt die Verwendung von " [**verschlüsseltmessage" (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) zum Signieren von Daten, die durch **GSS \_ Unwrap** überprüft werden.

Im SSPI-Client:


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



Auf dem GSSAPI-Server:


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



Die SSPI-Entsprechung zu **GSS \_ Unwrap** ist [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage). Im folgenden Beispiel wird gezeigt, wie mit **DecryptMessage (Kerberos)** Daten entschlüsselt werden, die mit **GSS- \_ Wrap** verschlüsselt wurden.

Auf dem GSSAPI-Server:


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



Im SSPI-Client:


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



 

 
