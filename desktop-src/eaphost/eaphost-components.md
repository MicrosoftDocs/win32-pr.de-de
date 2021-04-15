---
title: Komponenten von EAPHost
description: Erfahren Sie mehr über die drei Komponenten der EAPHost-Authentifizierung. Anzeigen zusätzlicher verfügbarer Ressourcen für die Verwendung der EAPHost-Authentifizierung.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474261"
---
# <a name="components-of-eaphost"></a><span data-ttu-id="74907-104">Komponenten von EAPHost</span><span class="sxs-lookup"><span data-stu-id="74907-104">Components of EAPHost</span></span>

<span data-ttu-id="74907-105">In diesem Thema werden die drei Komponenten der EAPHost-Authentifizierung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="74907-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="74907-106">EAPHost-Komponenten</span><span class="sxs-lookup"><span data-stu-id="74907-106">EAPHost Components</span></span>

<span data-ttu-id="74907-107">Die EAPHost-Authentifizierung verfügt über die folgenden drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="74907-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="74907-108">Der Supplicant, der die Authentifizierungsanforderungen übernimmt.</span><span class="sxs-lookup"><span data-stu-id="74907-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="74907-109">Die EAP-Methoden des Peer (oder Clients), die die spezifischen EAP-Methoden implementieren und die Authentifizierungs Sitzung auf Clientseite verwalten.</span><span class="sxs-lookup"><span data-stu-id="74907-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="74907-110">Die EAP-Methoden des Authenticator (oder des Servers), die die Serverseite des EAP-Protokolls implementieren.</span><span class="sxs-lookup"><span data-stu-id="74907-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="74907-111">Die Supplicant-APIs werden direkt von einer Anwendung aufgerufen, die über EAPHost authentifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74907-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="74907-112">Dabei handelt es sich jedoch um Funktionsprototypen, die für einen bestimmten EAP-Authentifizierungstyp implementiert werden müssen, z. b. das Microsoft Challenge Handshake Authentication-Protokoll, Version 2,0 (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="74907-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="74907-113">Wenn Sie eine Anwendung erstellen, die EAPHost für die Authentifizierung verwendet, lesen Sie die API-Referenz für den [EAPHost-Supplicant](eap-host-supplicant-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="74907-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="74907-114">Wenn Sie eine neue EAP-Authentifizierungsmethode erstellen, die von EAPHost verwaltet werden soll, lesen Sie die API-Referenz für die [EAPHost-Peer Methode](eap-host-peer-method-api-reference.md) und die [APIs der EAPHost-Authenticator-Methode](eaphost-authenticator-method-apis.md).</span><span class="sxs-lookup"><span data-stu-id="74907-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="74907-115">Beachten Sie, dass Sie Implementierungen dieser APIs erstellen, die in einer neuen DLL verfügbar gemacht werden, die EAPHost lädt, anstatt Sie direkt Aufrufs auszuführen.</span><span class="sxs-lookup"><span data-stu-id="74907-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




