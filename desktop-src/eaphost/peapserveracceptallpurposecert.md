---
title: "\"Peer-serveraccept tallpurposecert\""
description: Der Registrierungsschlüssel "papserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die Peer-Authentifizierung akzeptiert werden.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106339034"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="46a36-103">"Peer-serveraccept tallpurposecert"</span><span class="sxs-lookup"><span data-stu-id="46a36-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="46a36-104">Der Registrierungsschlüssel "papserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die Peer-Authentifizierung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="46a36-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="46a36-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="46a36-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="46a36-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46a36-106">Remarks</span></span>

<span data-ttu-id="46a36-107">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="46a36-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="46a36-108">Wert</span><span class="sxs-lookup"><span data-stu-id="46a36-108">Value</span></span>        | <span data-ttu-id="46a36-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46a36-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a36-110">1</span><span class="sxs-lookup"><span data-stu-id="46a36-110">1</span></span>            | <span data-ttu-id="46a36-111">Server und Client akzeptieren sämtliche Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="46a36-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="46a36-112">Andere Werte</span><span class="sxs-lookup"><span data-stu-id="46a36-112">Other values</span></span> | <span data-ttu-id="46a36-113">Server und Client akzeptieren keine von der anderen Partei gesendeten Zertifikate für die EAP-TLS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="46a36-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="46a36-114">Wenn dieser Registrierungs Wert nicht vorhanden ist, akzeptieren der Server und der Client sämtliche Zertifikate, die von der anderen Partei für die Peer-Authentifizierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="46a36-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a36-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46a36-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a36-116">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="46a36-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




