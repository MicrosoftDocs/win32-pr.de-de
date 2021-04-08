---
description: Erstellen einer sicheren Verbindung mithilfe von SChannel
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Erstellen einer sicheren Verbindung mithilfe von SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757291"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="f0a98-103">Erstellen einer sicheren Verbindung mithilfe von SChannel</span><span class="sxs-lookup"><span data-stu-id="f0a98-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="f0a98-104">Das SChannel- [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) ermöglicht den Zugriff auf vier [*Sicherheitsprotokolle*](/windows/desktop/SecGloss/s-gly):</span><span class="sxs-lookup"><span data-stu-id="f0a98-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="f0a98-105">Transport Layer Security (TLS 1,2)</span><span class="sxs-lookup"><span data-stu-id="f0a98-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="f0a98-106">Transport Layer Security (TLS 1,1)</span><span class="sxs-lookup"><span data-stu-id="f0a98-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="f0a98-107">Transport Layer Security (TLS 1,0)</span><span class="sxs-lookup"><span data-stu-id="f0a98-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="f0a98-108">Secure Sockets Layer (SSL 3,0)</span><span class="sxs-lookup"><span data-stu-id="f0a98-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="f0a98-109">Secure Sockets Layer (SSL 2,0)</span><span class="sxs-lookup"><span data-stu-id="f0a98-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="f0a98-110">Die PCT-und SSL 2,0-Protokolle wurden durch das TLS-Protokoll ersetzt und sollten nicht für die neue Entwicklung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0a98-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="f0a98-111">**So richten Sie eine sichere Verbindung zwischen einem Client und einem Server ein**</span><span class="sxs-lookup"><span data-stu-id="f0a98-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="f0a98-112">Anfordern von SChannel-Anmelde Informationen (Abrufen von[SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen)</span><span class="sxs-lookup"><span data-stu-id="f0a98-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="f0a98-113">Erstellen eines SChannel-Sicherheits Kontexts ([Erstellen eines SChannel-Sicherheits Kontexts](creating-an-schannel-security-context.md)).</span><span class="sxs-lookup"><span data-stu-id="f0a98-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="f0a98-114">Nachdem eine Verbindung hergestellt wurde, können Sie Informationen zu ihren Attributen abrufen.</span><span class="sxs-lookup"><span data-stu-id="f0a98-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="f0a98-115">Weitere Informationen finden Sie unter [Informationen zu SChannel-Verbindungen](getting-information-about-schannel-connections.md).</span><span class="sxs-lookup"><span data-stu-id="f0a98-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="f0a98-116">Wenn Sie nach dem Herstellen einer Verbindung die Sicherheitsanforderungen Ihrer Anwendung ändern oder die Verbindung verloren geht, können Sie die Verbindung erneut aushandeln.</span><span class="sxs-lookup"><span data-stu-id="f0a98-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="f0a98-117">Weitere Informationen finden Sie unter [Aushandeln einer SChannel-Verbindung](renegotiating-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f0a98-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="f0a98-118">Wenn Sie mit der Verwendung einer SChannel-Verbindung fertig sind, müssen Sie die erforderliche Bereinigung ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0a98-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="f0a98-119">Weitere Informationen finden Sie unter Herunterfahren [einer SChannel-Verbindung](shutting-down-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f0a98-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="f0a98-120">Informationen zu den mit dem Platform Software Development Kit (SDK) gelieferten Beispielen, die das SChannel- [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly)veranschaulichen, finden Sie in den PSDK-Beispielen mithilfe von Schannel.</span><span class="sxs-lookup"><span data-stu-id="f0a98-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0a98-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0a98-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a98-122">Angeben von SChannel-Chiffren und Verschlüsselungs stärken</span><span class="sxs-lookup"><span data-stu-id="f0a98-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
