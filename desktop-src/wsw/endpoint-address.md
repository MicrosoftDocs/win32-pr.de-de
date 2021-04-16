---
title: Endpunktadresse
description: Eine Endpunkt Adresse stellt die Adresse eines Dienstanbieter im Netzwerk dar.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Endpunkt Adresse Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104553922"
---
# <a name="endpoint-address"></a><span data-ttu-id="2b96a-106">Endpunktadresse</span><span class="sxs-lookup"><span data-stu-id="2b96a-106">Endpoint Address</span></span>

<span data-ttu-id="2b96a-107">Eine Endpunkt Adresse stellt die Adresse eines Dienstanbieter im Netzwerk dar.</span><span class="sxs-lookup"><span data-stu-id="2b96a-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="2b96a-108">Wenn Sie einen [Kanal](channel.md)öffnen, indem Sie die [**wsopenchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) -Funktion aufrufen, müssen Sie die Endpunkt Adresse des Dienstanbieter bereitstellen, mit dem Sie kommunizieren möchten, sowie den Kanal angeben, den Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="2b96a-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="2b96a-109">Eine Endpunkt Adresse besteht aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="2b96a-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="2b96a-110">eine [URL](url.md)</span><span class="sxs-lookup"><span data-stu-id="2b96a-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="2b96a-111">ein Satz von Headern (optional)</span><span class="sxs-lookup"><span data-stu-id="2b96a-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="2b96a-112">ein Satz von Erweiterungen (optional)</span><span class="sxs-lookup"><span data-stu-id="2b96a-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="2b96a-113">eine optionale [Identität](endpoint-identity.md) , die die Sicherheitsidentität des Diensts darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b96a-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="2b96a-114">Wenn eine Nachricht adressiert wird, wird die URL zum "to"-Header der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2b96a-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="2b96a-115">Alle Header, die Teil der Endpunkt Adresse sind, werden ebenfalls der Nachricht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b96a-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![Diagramm, das anzeigt, dass Endpunkt Adress Header zu einer Nachricht hinzugefügt werden.](images/endpointaddress.png)

<span data-ttu-id="2b96a-117">Kanäle adressiert automatisch alle gesendeten Nachrichten mithilfe der [**WS- \_ Endpunkt \_ Adress**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) Struktur, die an [**wsopkanchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b96a-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="2b96a-118">Sie können auch die [**wsaddressmessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) -Funktion verwenden, um dieses Standardverhalten zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2b96a-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="2b96a-119">Wenn die [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) als Parameter übergeben wird, erstellen die [**wsopenchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) -und [**wsopenserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) -Funktionen eine Kopie des **WS- \_ Endpunkt \_ Adress** Parameters im Arbeitsspeicher, und ihre Größe ist auf 65536 Bytes begrenzt.</span><span class="sxs-lookup"><span data-stu-id="2b96a-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="2b96a-120">[**Wsaddressmessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) weist diese Einschränkung nicht auf, da es nicht erforderlich ist, eine Kopie des **WS- \_ Endpunkt \_ Adress** Parameters zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b96a-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="2b96a-121">Die Erweiterungen, die im Feld **Erweiterungen** der [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) angegeben werden, werden nicht für die Adressierung der Nachricht verwendet. stattdessen handelt es sich um einen Erweiterbarkeits Mechanismus, der verwendet werden kann, um zusätzliche Informationen (z. b. Metadaten) über den Dienst bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2b96a-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="2b96a-122">Allgemeine Erweiterungen können mit der [**wsleseendpointadressssextension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) -Funktion gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="2b96a-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="2b96a-123">Das optionale Identitäts Feld der Endpunkt Adresse kann z. b. den DNS-Namen des Computers enthalten, auf dem der Dienst ausgeführt wird, oder den UPN des Windows-Kontos, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b96a-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="2b96a-124">Das Identitäts Feld wird nicht zur Adressierung der Nachricht verwendet, kann jedoch zum Abrufen eines Sicherheits Tokens für den Dienst (z. b. zum Abrufen eines Kerberos-Tickets für den UPN des Ziels) und zum Überprüfen der Identität der Dienst Antworten verwendet werden (z</span><span class="sxs-lookup"><span data-stu-id="2b96a-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="2b96a-125">Endpunkt Adressen können mithilfe der [Serialisierung](serialization.md) gelesen und geschrieben werden, wobei der WS-Endpunkt- **\_ \_ \_ Adresstyp** Enumerationswert vom [**WS- \_ Typ**](/windows/desktop/api/WebServices/ne-webservices-ws_type)ist.</span><span class="sxs-lookup"><span data-stu-id="2b96a-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="2b96a-126">Hinweis Wenn Sie eine Endpunkt Adresse serialisieren möchten, müssen Sie die Version der Spezifikation kennen, die für die Adressierungs Header verwendet wird, wie in der Enumeration der [**WS- \_ Adressierungs \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b96a-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




