---
title: Sicherheitskontext
description: Sicherheits Kontexte ermöglichen die Einrichtung eines Nachrichten Sicherheits Kontexts gemäß WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- 'Sicherheitskontext: Native Webdienste'
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316790"
---
# <a name="security-context"></a><span data-ttu-id="b837e-106">Sicherheitskontext</span><span class="sxs-lookup"><span data-stu-id="b837e-106">Security Context</span></span>

<span data-ttu-id="b837e-107">Sicherheits Kontexte ermöglichen die Einrichtung eines Nachrichten Sicherheits Kontexts gemäß WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="b837e-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="b837e-108">Dieser Kontext kann dann verwendet werden, um Nachrichten als Alternative zur One-Shot-Sicherheit zu sichern, bei der die Anmelde Informationen für jede Anforderung übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b837e-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="b837e-109">Der etablierte Sicherheitskontext ist eine effizientere Methode zum Sichern von Nachrichten, wenn mehrere Nachrichten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="b837e-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="b837e-110">Sicherheits Kontexte erfordern das vorhanden sein von Bootstrap-Sicherheits Anmelde Informationen, die zum Sichern der im Kontext gesendeten Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b837e-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="b837e-111">Zu diesem Zweck können die [**WS \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), die [**WS \_ XML \_ Token \_ Message- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)und [**WS \_ username \_ Message \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) Binding-Strukturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b837e-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="b837e-112">Sicherheits Kontexte sind ein Nachrichten Sicherheits Feature, das mithilfe von Nachrichten Sicherheits Bindungen konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="b837e-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="b837e-113">Client</span><span class="sxs-lookup"><span data-stu-id="b837e-113">Client</span></span>

<span data-ttu-id="b837e-114">Auf der Clientseite ist der Sicherheitskontext an einen bestimmten Kanal gebunden.</span><span class="sxs-lookup"><span data-stu-id="b837e-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="b837e-115">Sie wird mithilfe der [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b837e-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="b837e-116">Das Verhalten und die Lebensdauer des Kontexts werden vom Kanal bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b837e-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="b837e-117">Wenn die erste Nachricht auf dem Kanal gesendet wird, wird der Sicherheitskontext eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b837e-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="b837e-118">Danach wird der Kontext proaktiv in einem konfigurierbaren Intervall erneuert.</span><span class="sxs-lookup"><span data-stu-id="b837e-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="b837e-119">Wenn der Server einen Fehler zurückgibt, der angibt, dass der Kontext erneuert werden muss, wird der Kontext erneuert, wenn die nächste Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b837e-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="b837e-120">Wenn sich der Kanal im geöffneten Zustand befindet, wird der Kontext durch eine Abbruch Meldung abgebrochen, wenn der Kanal geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b837e-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="b837e-121">Server</span><span class="sxs-lookup"><span data-stu-id="b837e-121">Server</span></span>

<span data-ttu-id="b837e-122">Auf dem-Server wird ein Sicherheitskontext auf die gleiche Weise wie auf dem Client konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b837e-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="b837e-123">Es ist jedoch nicht an einen bestimmten Kanal gebunden.</span><span class="sxs-lookup"><span data-stu-id="b837e-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="b837e-124">Stattdessen können alle Kanäle, die für den Listener erstellt werden, der über den [**WS \_ Security \_ context \_ Message- \_ \_ Bindungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) Satz verfügt, Nachrichten mit einem beliebigen Sicherheitskontext empfangen, der auf Kanälen dieses Listener eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="b837e-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="b837e-125">Wenn eine Nachricht in einem Kanal eingeht, der Sicherheits Kontexte unterstützt, kann der von dieser Nachricht verwendete Kontext durch Aufrufen der [**wsgetmessageproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) -Funktion mit dem [**WS- \_ Nachrichten Eigenschaften- \_ \_ Sicherheits \_ Kontext**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b837e-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="b837e-126">Der abgerufene Wert kann mit [**wsrevokesecuritycontext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) und [**wsgetsecuritycontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b837e-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="b837e-127">Metadaten</span><span class="sxs-lookup"><span data-stu-id="b837e-127">Metadata</span></span>

<span data-ttu-id="b837e-128">Die Sicherheitskontext-Einschränkungs Struktur des [**WS- \_ Sicherheits \_ Kontexts \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) wird zum Extrahieren der Sicherheitskontext Richtlinie aus den Metadaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b837e-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="b837e-129">Weitere Informationen finden Sie unter [Metadatenimport](metadata-import.md).</span><span class="sxs-lookup"><span data-stu-id="b837e-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="b837e-130">Die folgenden API-Elemente werden mit Sicherheits Kontexten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b837e-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="b837e-131">Enumeration</span><span class="sxs-lookup"><span data-stu-id="b837e-131">Enumeration</span></span>                                                                    | <span data-ttu-id="b837e-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b837e-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="b837e-133">**WS- \_ Sicherheits \_ Kontext-Eigenschaften- \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="b837e-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="b837e-134">Identifiziert eine Eigenschaft eines Sicherheitskontext Objekts.</span><span class="sxs-lookup"><span data-stu-id="b837e-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="b837e-135">Funktion</span><span class="sxs-lookup"><span data-stu-id="b837e-135">Function</span></span>                                                             | <span data-ttu-id="b837e-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b837e-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b837e-137">**Wsgetsecuritycontextproperty**</span><span class="sxs-lookup"><span data-stu-id="b837e-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="b837e-138">Ruft eine Eigenschaft des angegebenen Sicherheits Kontexts ab.</span><span class="sxs-lookup"><span data-stu-id="b837e-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="b837e-139">**Wsrevokesecuritycontext**</span><span class="sxs-lookup"><span data-stu-id="b837e-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="b837e-140">Widerruft einen Sicherheitskontext.</span><span class="sxs-lookup"><span data-stu-id="b837e-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="b837e-141">Handle</span><span class="sxs-lookup"><span data-stu-id="b837e-141">Handle</span></span>                                           | <span data-ttu-id="b837e-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b837e-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="b837e-143">WS- \_ Sicherheits \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="b837e-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="b837e-144">Ein nicht transparenter Typ, mit dem auf ein Sicherheitskontext Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b837e-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="b837e-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="b837e-145">Structure</span></span>                                                               | <span data-ttu-id="b837e-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b837e-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="b837e-147">**WS- \_ Sicherheits \_ Kontext \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="b837e-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="b837e-148">Definiert eine Eigenschaft eines [WS- \_ Sicherheits \_ Kontexts](ws-security-context.md).</span><span class="sxs-lookup"><span data-stu-id="b837e-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 




