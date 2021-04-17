---
title: "\"Peer-serveruseallpurposecert\""
description: Der Registrierungsschlüssel "papserveruseallpurposecert" bestimmt, ob für die Peer-Authentifizierung alle Zweck Zertifikate verwendet werden.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313835"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="77d8f-103">"Peer-serveruseallpurposecert"</span><span class="sxs-lookup"><span data-stu-id="77d8f-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="77d8f-104">Der Registrierungsschlüssel "papserveruseallpurposecert" bestimmt, ob für die Peer-Authentifizierung alle Zweck Zertifikate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77d8f-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="77d8f-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="77d8f-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="77d8f-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77d8f-106">Remarks</span></span>

<span data-ttu-id="77d8f-107">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="77d8f-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="77d8f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="77d8f-108">Value</span></span>        | <span data-ttu-id="77d8f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77d8f-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d8f-110">1</span><span class="sxs-lookup"><span data-stu-id="77d8f-110">1</span></span>            | <span data-ttu-id="77d8f-111">Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder Servers werden für die Peer-Authentifizierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="77d8f-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="77d8f-112">Andere Werte</span><span class="sxs-lookup"><span data-stu-id="77d8f-112">Other values</span></span> | <span data-ttu-id="77d8f-113">Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder des Servers sind nicht für die Peer-Authentifizierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="77d8f-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="77d8f-114">Wenn dieser Registrierungs Wert nicht vorhanden ist, werden alle Zertifikate im Zertifikat Speicher des Clients oder des Servers für die Peer-Authentifizierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="77d8f-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77d8f-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77d8f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77d8f-116">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="77d8f-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




