---
description: Beenden einer SChannel-Verbindung
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Beenden einer SChannel-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749601"
---
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="bc20c-103">Beenden einer SChannel-Verbindung</span><span class="sxs-lookup"><span data-stu-id="bc20c-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="bc20c-104">Wenn ein Client oder Server mit einer Verbindung fertig ist, muss er heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="bc20c-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="bc20c-105">Die andere Partei muss wiederum das Herunterfahren erkennen und die Verbindung löschen.</span><span class="sxs-lookup"><span data-stu-id="bc20c-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="bc20c-106">**So fahren Sie eine SChannel-Verbindung herunter**</span><span class="sxs-lookup"><span data-stu-id="bc20c-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="bc20c-107">Wenden Sie die [**applycontroltoken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) -Funktion an, und geben Sie das SChannel \_ Shutdown-Steuerungs Token an.</span><span class="sxs-lookup"><span data-stu-id="bc20c-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="bc20c-108">Nachdem Sie einen SEK \_ \_ .-Rückgabewert von [**applycontroltoken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)erhalten haben, können Sie die Funktion [**InitializeSecurityContext (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (Clients) oder [**Accept tsecuritycontext (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Server) abrufen, indem Sie leere Puffer übergeben.</span><span class="sxs-lookup"><span data-stu-id="bc20c-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="bc20c-109">Gehen Sie so vor, als ob die Anwendung eine neue Verbindung erstellt hätte, bis die Funktion SEK \_ . I- \_ Kontext \_ abgelaufen oder SEK \_ . OK zurückgibt \_ , um anzugeben, dass die Verbindung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="bc20c-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="bc20c-110">Senden Sie ggf. die endgültigen Ausgabeinformationen an den Remote Anbieter.</span><span class="sxs-lookup"><span data-stu-id="bc20c-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="bc20c-111">Ruft den [**Delta Context-Kontext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) auf, um die von der Verbindung gehaltenen Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bc20c-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="bc20c-112">Erkennen eines herunter Fahrens</span><span class="sxs-lookup"><span data-stu-id="bc20c-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="bc20c-113">Die Funktion [**DecryptMessage (SChannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) gibt Sekunde zurück, \_ Wenn der \_ \_ Nachrichten Absender die Verbindung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="bc20c-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="bc20c-114">Nachdem Sie diesen Rückgabewert erhalten haben, führen Sie das Verfahren zum Herunterfahren einer SChannel-Verbindung weiter oben in diesem Thema aus.</span><span class="sxs-lookup"><span data-stu-id="bc20c-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
