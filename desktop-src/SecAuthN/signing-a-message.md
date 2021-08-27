---
description: Wenn ein Client und Server die Einrichtung des Sicherheitskontexts abgeschlossen haben, können Nachrichtenunterstützungsfunktionen verwendet werden.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Signieren einer Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b605ccaaa4adfe37dc2bbe5f5c0ed809f0656896e5e85478b0b63740bf6f63e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918049"
---
# <a name="signing-a-message"></a>Signieren einer Nachricht

Wenn ein Client und Server die Einrichtung des Sicherheitskontexts [*abgeschlossen haben,*](../secgloss/s-gly.md)können Nachrichtenunterstützungsfunktionen verwendet werden. Client und Server verwenden das Sicherheitskontexttoken, das beim Herstellen der Sitzung zum Aufrufen der [**Funktionen MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature erstellt**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) wurde. Das Kontexttoken kann für den Datenschutz bei der Kommunikation mit [**EncryptMessage (Allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (Allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) [*verwendet werden.*](../secgloss/p-gly.md)

Das folgende Beispiel zeigt, wie die Clientseite eine signierte Nachricht generiert, die an den Server gesendet werden soll. Vor dem [**Aufruf von MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)ruft der Client [**QueryContextAttributes (Allgemein)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) mit einer [**SecPkgContext \_ Sizes-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) auf, um die Länge des Puffers zu bestimmen, der zum Enthalten der Nachrichtensignatur erforderlich ist. Wenn das **cbMaxSignature-Mitglied** [](../secgloss/s-gly.md) 0 (null) ist, unterstützt das Sicherheitspaket keine Signierungsmeldungen. Andernfalls gibt dieser Member die Größe des Puffers an, der zum Empfangen der Signatur reserviert werden soll.

Im Beispiel wird davon ausgegangen, dass eine **SecHandle-Variable** namens *phContext* und eine **SOCKET-Struktur** namens *s* initialisiert werden. Informationen zu den Deklarationen und Initiierungen dieser Variablen finden Sie unter Using SSPI with a Windows Sockets Client (Verwenden von SSPI mit einem [Windows Sockets-Client)](using-sspi-with-a-windows-sockets-client.md) und [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md)(Verwenden von SSPI mit einem Windows Sockets Server). Dieses Beispiel enthält Aufrufe von Funktionen in Secur32.lib, die in die Linkbibliotheken aufgenommen werden müssen.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



[**MakeSignature gibt**](/windows/desktop/api/Sspi/nf-sspi-makesignature) **TRUE zurück,** wenn der Kontext so eingerichtet ist, dass signierte Nachrichten zulässig sind und der Eingabepufferdeskriptor ordnungsgemäß formatiert ist. Nachdem die Nachricht signiert wurde, werden die Nachricht und die Signatur mit ihrer Länge an den Remotecomputer gesendet.

> [!Note]  
> Der Dateninhalt der [**SecBuffer-Strukturen**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) wird gesendet, nicht die **SecBuffer-Strukturen** selbst oder die [**SecBufferDesc-Struktur.**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) Neue **SecBuffer-Strukturen** und eine neue **SecBufferDesc-Struktur** werden von der empfangenden Anwendung erstellt, um die Signatur zu überprüfen.

 

 

 
