---
description: Das folgende Beispiel zeigt den Code zum empfangen und Überprüfen einer signierten Nachricht. In diesem Beispiel werden der Signatur Puffer und seine Größe in signaturebuffer und signaturebuffersize sowie der Nachrichten Puffer und seine Größe in MessageBuffer und messagebuffersize empfangen.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Überprüfen einer Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebf62be707efcbd3ab3a5eca5345261ca1a0fde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343169"
---
# <a name="verifying-a-message"></a><span data-ttu-id="0f18c-104">Überprüfen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="0f18c-104">Verifying a Message</span></span>

<span data-ttu-id="0f18c-105">Das folgende Beispiel zeigt den Code zum empfangen und Überprüfen einer signierten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0f18c-105">The following example shows code to receive and verify a signed message.</span></span> <span data-ttu-id="0f18c-106">In diesem Beispiel werden der Signatur Puffer und seine Größe in signaturebuffer und signaturebuffersize sowie der Nachrichten Puffer und seine Größe in MessageBuffer und messagebuffersize empfangen.</span><span class="sxs-lookup"><span data-stu-id="0f18c-106">The example receives the signature buffer and its size in SignatureBuffer and SignatureBufferSize and the message buffer and its size in MessageBuffer and MessageBufferSize.</span></span>

<span data-ttu-id="0f18c-107">Im Beispiel wird davon ausgegangen, dass eine **sechandle** -Variable namens phcontext und eine **Socketstruktur** mit dem Namen s initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f18c-107">The example assumes that a **SecHandle** variable named phContext and a **SOCKET** structure named s are initialized.</span></span> <span data-ttu-id="0f18c-108">Informationen zu den Deklarationen und Initiierungen dieser Variablen finden [Sie unter Verwenden von SSPI mit einem Windows Sockets-Client](using-sspi-with-a-windows-sockets-client.md) und [Verwenden von SSPI mit einem Windows Sockets-Server](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="0f18c-108">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="0f18c-109">Dieser Code enthält Aufrufe von Funktionen in Secur32. lib, die in den Linkbibliotheken enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="0f18c-109">This code includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



