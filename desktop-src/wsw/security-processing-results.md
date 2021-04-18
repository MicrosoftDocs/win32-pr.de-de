---
title: Ergebnisse der Sicherheits Verarbeitung
description: Auf einem sicheren Kanal werden nur die Nachrichten, die erfolgreich Sicherheitsüberprüfungen bestanden haben, an die Anwendung übermittelt.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Sicherheitsverarbeitungs Ergebnisse Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106340948"
---
# <a name="security-processing-results"></a><span data-ttu-id="4d577-106">Ergebnisse der Sicherheits Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="4d577-106">Security Processing Results</span></span>

<span data-ttu-id="4d577-107">Auf einem sicheren Kanal werden nur die Nachrichten, die erfolgreich Sicherheitsüberprüfungen bestanden haben, an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4d577-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="4d577-108">Für diese Nachrichten werden einige Ergebnisse aus der Sicherheitsüberprüfung als Nachrichten Eigenschaften angefügt, und die Anwendung kann diese Eigenschaften extrahieren und untersuchen, um zusätzliche Schritte auszuführen, z. b. Autorisierungs Überprüfungen.</span><span class="sxs-lookup"><span data-stu-id="4d577-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="4d577-109">Die Funktion [**wsgetmessageproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) kann verwendet werden, um alle sicherheitsbezogenen Eigenschaften abzurufen, die in der [**WS- \_ Nachrichten eigen schafts- \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4d577-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="4d577-110">**Wsgetmessageproperty** gibt einen Fehler für Abfragen zurück, die Sicherheitseigenschaften anfordern, die nicht für den auf dem Kanal verwendeten Sicherheitstyp gelten.</span><span class="sxs-lookup"><span data-stu-id="4d577-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="4d577-111">Die Nachricht ist weiterhin Besitzer der von der Abfragefunktion zurückgegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d577-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="4d577-112">Die folgenden API-Elemente werden mit den Ergebnissen der Sicherheits Verarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d577-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="4d577-113">Enumeration</span><span class="sxs-lookup"><span data-stu-id="4d577-113">Enumeration</span></span>                                                                | <span data-ttu-id="4d577-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d577-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d577-115">**WS- \_ Sicherheits \_ Token-Eigenschaften- \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="4d577-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="4d577-116">Definiert die Schlüssel für die Felder und Eigenschaften, die aus einem Sicherheits Token extrahiert werden können.</span><span class="sxs-lookup"><span data-stu-id="4d577-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="4d577-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="4d577-117">Function</span></span>                                                         | <span data-ttu-id="4d577-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d577-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="4d577-119">**Wsgetsecuritytoken-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4d577-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="4d577-120">Extrahiert ein Feld oder eine Eigenschaft aus einem Sicherheits Token.</span><span class="sxs-lookup"><span data-stu-id="4d577-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="4d577-121">Handle</span><span class="sxs-lookup"><span data-stu-id="4d577-121">Handle</span></span>                                       | <span data-ttu-id="4d577-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d577-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4d577-123">WS- \_ Sicherheits \_ Token</span><span class="sxs-lookup"><span data-stu-id="4d577-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="4d577-124">Ein undurchsichtiges handle, das ein Sicherheits Token darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d577-124">An opaque handle representing a security token.</span></span> |



 

 

 




