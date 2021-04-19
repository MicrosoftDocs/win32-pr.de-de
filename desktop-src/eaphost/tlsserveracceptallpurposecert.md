---
title: Tlsserverakzeptallpurposecert
description: Der Registrierungsschlüssel "tlsserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die EAP-TLS-Authentifizierung akzeptiert werden.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106338237"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="83254-103">Tlsserverakzeptallpurposecert</span><span class="sxs-lookup"><span data-stu-id="83254-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="83254-104">Der Registrierungsschlüssel "tlsserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die EAP-TLS-Authentifizierung akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="83254-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="83254-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="83254-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="83254-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83254-106">Remarks</span></span>

<span data-ttu-id="83254-107">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="83254-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="83254-108">Wert</span><span class="sxs-lookup"><span data-stu-id="83254-108">Value</span></span>        | <span data-ttu-id="83254-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83254-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83254-110">1</span><span class="sxs-lookup"><span data-stu-id="83254-110">1</span></span>            | <span data-ttu-id="83254-111">Server und Client akzeptieren sämtliche Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="83254-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="83254-112">Andere Werte</span><span class="sxs-lookup"><span data-stu-id="83254-112">Other values</span></span> | <span data-ttu-id="83254-113">Server und Client akzeptieren keine von der anderen Partei gesendeten Zertifikate für die EAP-TLS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="83254-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="83254-114">Wenn dieser Registrierungs Wert nicht vorhanden ist, akzeptieren der Server und der Client alle Zweck Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="83254-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83254-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83254-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83254-116">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="83254-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




