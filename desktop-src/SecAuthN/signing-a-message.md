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
# <a name="signing-a-message"></a><span data-ttu-id="b09ae-103">Signieren einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="b09ae-103">Signing a Message</span></span>

<span data-ttu-id="b09ae-104">Wenn ein Client und Server das Einrichten des [*Sicherheits Kontexts*](../secgloss/s-gly.md)abgeschlossen haben, können Nachrichten Unterstützungsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b09ae-104">When a client and server finish setting up the [*security context*](../secgloss/s-gly.md), message support functions can be used.</span></span> <span data-ttu-id="b09ae-105">Client und Server verwenden das Sicherheitskontext Token, das beim Erstellen der Sitzung erstellt wurde, um [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b09ae-105">The client and server use the security context token created when the session was established to call [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions.</span></span> <span data-ttu-id="b09ae-106">Das Kontext Token kann mit [**verschlüsselungsmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) für den Kommunikations [*Datenschutz*](../secgloss/p-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b09ae-106">The context token can be used with [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) for communications [*privacy*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="b09ae-107">Im folgenden Beispiel wird die Client seitige Erstellung einer signierten Nachricht veranschaulicht, die an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b09ae-107">The following example shows the client side generating a signed message to send to the server.</span></span> <span data-ttu-id="b09ae-108">Vor dem Aufrufen von [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)ruft der Client [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) mit einer [**secpkgcontext \_ sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) -Struktur auf, um die Länge des Puffers zu bestimmen, der zum Speichern der Nachrichten Signatur benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b09ae-108">Before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the client calls [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) with a [**SecPkgContext\_Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) structure to determine the length of the buffer needed to hold the message signature.</span></span> <span data-ttu-id="b09ae-109">Wenn der **cbmaxsignature** -Member 0 (null) ist, unterstützt das [*Sicherheitspaket*](../secgloss/s-gly.md) keine Signierung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="b09ae-109">If the **cbMaxSignature** member is zero, the [*security package*](../secgloss/s-gly.md) does not support signing messages.</span></span> <span data-ttu-id="b09ae-110">Andernfalls gibt dieser Member die Größe des Puffers an, der für den Empfang der Signatur zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b09ae-110">Otherwise, this member indicates the size of the buffer to allocate to receive the signature.</span></span>

<span data-ttu-id="b09ae-111">Im Beispiel wird davon ausgegangen, dass eine **sechandle** -Variable namens *phcontext* und eine **Socketstruktur** mit dem Namen *s* initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b09ae-111">The example assumes that a **SecHandle** variable named *phContext* and a **SOCKET** structure named *s* are initialized.</span></span> <span data-ttu-id="b09ae-112">Informationen zu den Deklarationen und Initiierungen dieser Variablen finden [Sie unter Verwenden von SSPI mit einem Windows Sockets-Client](using-sspi-with-a-windows-sockets-client.md) und [Verwenden von SSPI mit einem Windows Sockets-Server](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="b09ae-112">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="b09ae-113">Dieses Beispiel umfasst Aufrufe von Funktionen in Secur32. lib, die in den Linkbibliotheken enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="b09ae-113">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


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



<span data-ttu-id="b09ae-114">[**Makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) gibt **true** zurück, wenn der Kontext für das Signieren von Nachrichten eingerichtet ist und der Eingabepuffer Deskriptor ordnungsgemäß formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="b09ae-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) returns **TRUE** if the context is set up to allow signing messages and if the input buffer descriptor is correctly formatted.</span></span> <span data-ttu-id="b09ae-115">Nachdem die Nachricht signiert wurde, werden die Nachricht und die Signatur mit ihren Längen an den Remote Computer gesendet.</span><span class="sxs-lookup"><span data-stu-id="b09ae-115">After the message is signed, the message and the signature with their lengths are sent to the remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="b09ae-116">Der Dateninhalt der [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) -Strukturen wird gesendet, nicht die **secbuffer** -Strukturen selbst und die [**secbufferabsc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b09ae-116">The data contents of the [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures are sent, not the **SecBuffer** structures themselves nor the [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="b09ae-117">Neue **secbuffer** -Strukturen und eine neue **secbufferdesc** -Struktur werden von der empfangenden Anwendung erstellt, um die Signatur zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b09ae-117">New **SecBuffer** structures and a new **SecBufferDesc** structure are created by the receiving application to verify the signature.</span></span>

 

 

 
