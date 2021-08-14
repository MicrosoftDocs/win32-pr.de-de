---
description: Bei verwendung des Kerberos-Sicherheitssupportanbieters (Security Support Provider, SSP) muss Vorsichtsmaßnahmen ergriffen werden, wenn die Interoperabilität mit GSSAPI erforderlich ist.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: SSPI/Kerberos-Interoperabilität mit GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5907c79fbf4ef53a40b9dc2198715f216794de5634c60c66fe3d767bfe4af026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916827"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a>SSPI/Kerberos-Interoperabilität mit GSSAPI

Bei verwendung des Kerberos-Sicherheitssupportanbieters (Security [](../secgloss/k-gly.md) [*Support Provider,*](../secgloss/s-gly.md) SSP) muss Vorsichtsmaßnahmen ergriffen werden, wenn die Interoperabilität mit GSSAPI erforderlich ist. Die folgenden Codekonventionen ermöglichen die Interoperabilität mit GSSAPI-basierten Anwendungen:

-   [Windows kompatible Namen](#windows-compatible-names)
-   [Authentifizierung](#authentication)
-   [Nachrichtenintegrität und Datenschutz](#message-integrity-and-privacy)

Beispielcode finden Sie im Platform Software Development Kit (SDK) unter Samples \\ Security \\ SSPI \\ GSS (Sicherheits-SSPI-GSS). Darüber hinaus wird das entsprechende UNIX in den KERBEROS-Verteilungen MIT und Heimdal, GSS-Client und -Server verteilt.

## <a name="windows-compatible-names"></a>Windows-Compatible Namen

GSSAPI-Funktionen verwenden ein Namensformat, das als gss \_ \_ \_ nt-Dienstname bezeichnet wird, wie im RFC angegeben. Beispielsweise ist sample@host.dom.com ein Name, der in einer GSSAPI-basierten Anwendung verwendet werden kann. Das Windows erkennt das gss nt-Dienstnamenformat nicht, und der vollständige Dienstprinzipalname , z. B. \_ \_ , muss verwendet \_ [](../secgloss/s-gly.md) sample/host.dom.com@REALM werden.

## <a name="authentication"></a>Authentifizierung

Die Authentifizierung erfolgt in der Regel, wenn eine Verbindung zum ersten Mal zwischen einem Client und einem Server eingerichtet wird. In diesem Beispiel verwendet der Client die [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), und der Server verwendet GSSAPI.

**So richten Sie die Authentifizierung im SSPI-Client ein**

1.  Verwenden Sie [](../secgloss/c-gly.md) [**AcquireCredentialsHandle, um ausgehende Anmeldeinformationen zu erhalten.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)
2.  Erstellen Sie einen Dienstnamen mit **gss \_ import \_ name()** , und erhalten Sie eingehende Anmeldeinformationen, indem **Sie gss \_ acquire \_ cred verwenden.**
3.  Abrufen eines Authentifizierungstokens, das mit [**initializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)an den Server gesendet werden soll.
4.  Senden Sie das Token an den Server.

**So richten Sie die Authentifizierung auf dem GSSAPI-Server ein**

1.  Analysieren Sie die Nachricht vom Client, um das Sicherheitstoken zu extrahieren. Verwenden Sie die **Kontextfunktion gss \_ accept \_ sec, \_** und übergeben Sie das Token als Argument.
2.  Analysieren Sie die Nachricht vom Server, um das Sicherheitstoken zu extrahieren. Übergeben Sie dieses Sicherheitstoken [**an InitializeSecurityContext (Kerberos).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
3.  Senden Sie ein Antworttoken an den Client.

    Die **gss \_ accept \_ \_ sec-Kontextfunktion** kann ein Token zurückgeben, das Sie zurück an den Client senden können.

4.  Wenn es erforderlich ist, fortzufahren, senden Sie ein Antworttoken an den Server. Andernfalls ist die Einrichtung der Authentifizierung abgeschlossen.
5.  Wenn es erforderlich ist, fortzufahren, warten Sie auf das nächste Token vom Client. Andernfalls ist die Einrichtung der Authentifizierung abgeschlossen.

## <a name="message-integrity-and-privacy"></a>Nachrichtenintegrität und Datenschutz

Die meisten GSSAPI-basierten Anwendungen verwenden die **GSS \_ Wrap-Funktion,** um eine Nachricht vor dem Senden zu signieren. Im Gegensatz dazu überprüft **die GSS \_ Unwrap-Funktion** die Signatur. **GSS \_ Wrap** ist in Version 2.0 der API verfügbar und wird jetzt häufig verwendet und in Internetstandards angegeben, die die Verwendung der GSSAPI zum Hinzufügen von Sicherheit zu Protokollen beschreiben. Zuvor wurden die **GSS-Funktionen SignMessage** und **SealMessage** für die Nachrichtenintegrität [*und den*](../secgloss/i-gly.md) Datenschutz [*verwendet.*](../secgloss/p-gly.md) **GSS \_ Wrap** und **GSS \_ Unwrap** werden sowohl für Integrität als auch für den Datenschutz mit der Verwendung von Datenschutz verwendet, der durch den Wert des Arguments "conf \_ flag" gesteuert wird.

Wenn ein GSSAPI-basiertes Protokoll angegeben wird, um die **gss \_ get \_ mic-** und **gss \_ verify \_** mic-Funktionen zu verwenden, sind [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)die richtigen SSPI-Funktionen. Beachten Sie, **dass MakeSignature** und **VerifySignature** nicht mit **GSS \_ Wrap** zusammenarbeiten, wenn das Conf-Flag auf \_ 0 (null) oder **mit GSS \_ Wrap festgelegt ist.** Dasselbe gilt für die Mischung von [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) nur für Signaturen und **gss \_ verify \_ mic**.

> [!Note]  
> Verwenden Sie nicht die [**Funktionen MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) oder [**VerifySignature,**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) wenn **GSS \_ Wrap** und **GSS \_ Unwrap** aufgerufen werden.

 

Das SSPI-Äquivalent zu **GSS \_ Wrap** ist [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) für Integrität und Datenschutz.

Das folgende Beispiel zeigt die Verwendung [**von EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) zum Signieren von Daten, die von **GSS \_ Unwrap überprüft werden.**

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



Das SSPI-Äquivalent zu **GSS \_ Unwrap** ist [**DecryptMessage (Kerberos).**](/windows/win32/api/sspi/nf-sspi-decryptmessage) Hier ist ein Beispiel, das zeigt, wie **DecryptMessage (Kerberos)** zum Entschlüsseln von Daten verwendet wird, die mit **GSS \_ Wrap verschlüsselt wurden.**

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



 

 
