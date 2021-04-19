---
description: Wenn ein Client und Server das Einrichten des Sicherheits Kontexts abgeschlossen haben, können Nachrichten Unterstützungsfunktionen verwendet werden.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Signieren einer Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349605"
---
# <a name="signing-a-message"></a>Signieren einer Nachricht

Wenn ein Client und Server das Einrichten des [*Sicherheits Kontexts*](../secgloss/s-gly.md)abgeschlossen haben, können Nachrichten Unterstützungsfunktionen verwendet werden. Client und Server verwenden das Sicherheitskontext Token, das beim Erstellen der Sitzung erstellt wurde, um [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktionen aufzurufen. Das Kontext Token kann mit [**verschlüsselungsmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) für den Kommunikations [*Datenschutz*](../secgloss/p-gly.md)verwendet werden.

Im folgenden Beispiel wird die Client seitige Erstellung einer signierten Nachricht veranschaulicht, die an den Server gesendet wird. Vor dem Aufrufen von [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)ruft der Client [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) mit einer [**secpkgcontext \_ sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) -Struktur auf, um die Länge des Puffers zu bestimmen, der zum Speichern der Nachrichten Signatur benötigt wird. Wenn der **cbmaxsignature** -Member 0 (null) ist, unterstützt das [*Sicherheitspaket*](../secgloss/s-gly.md) keine Signierung von Nachrichten. Andernfalls gibt dieser Member die Größe des Puffers an, der für den Empfang der Signatur zugewiesen werden soll.

Im Beispiel wird davon ausgegangen, dass eine **sechandle** -Variable namens *phcontext* und eine **Socketstruktur** mit dem Namen *s* initialisiert werden. Informationen zu den Deklarationen und Initiierungen dieser Variablen finden [Sie unter Verwenden von SSPI mit einem Windows Sockets-Client](using-sspi-with-a-windows-sockets-client.md) und [Verwenden von SSPI mit einem Windows Sockets-Server](using-sspi-with-a-windows-sockets-server.md). Dieses Beispiel umfasst Aufrufe von Funktionen in Secur32. lib, die in den Linkbibliotheken enthalten sein müssen.


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



[**Makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) gibt **true** zurück, wenn der Kontext für das Signieren von Nachrichten eingerichtet ist und der Eingabepuffer Deskriptor ordnungsgemäß formatiert ist. Nachdem die Nachricht signiert wurde, werden die Nachricht und die Signatur mit ihren Längen an den Remote Computer gesendet.

> [!Note]  
> Der Dateninhalt der [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Strukturen wird gesendet, nicht die **secbuffer** -Strukturen selbst und die [**secbufferabsc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) -Struktur. Neue **secbuffer** -Strukturen und eine neue **secbufferdesc** -Struktur werden von der empfangenden Anwendung erstellt, um die Signatur zu überprüfen.

 

 

 
