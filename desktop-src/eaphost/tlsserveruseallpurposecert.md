---
title: Tlsserveruseallpurposecert
description: Der tlsserveruseallpurposecert-Registrierungsschlüssel legt fest, ob alle Zweck Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313812"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="5fdab-103">Tlsserveruseallpurposecert</span><span class="sxs-lookup"><span data-stu-id="5fdab-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="5fdab-104">Der tlsserveruseallpurposecert-Registrierungsschlüssel legt fest, ob alle Zweck Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fdab-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5fdab-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="5fdab-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="5fdab-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fdab-106">Remarks</span></span>

<span data-ttu-id="5fdab-107">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="5fdab-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="5fdab-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5fdab-108">Value</span></span>        | <span data-ttu-id="5fdab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fdab-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdab-110">1</span><span class="sxs-lookup"><span data-stu-id="5fdab-110">1</span></span>            | <span data-ttu-id="5fdab-111">Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder Servers werden für die Peer-Authentifizierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5fdab-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="5fdab-112">Andere Werte</span><span class="sxs-lookup"><span data-stu-id="5fdab-112">Other values</span></span> | <span data-ttu-id="5fdab-113">Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder des Servers sind nicht für die Peer-Authentifizierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5fdab-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="5fdab-114">Wenn dieser Registrierungs Wert nicht vorhanden ist, werden alle Zweck Zertifikate im Zertifikat Speicher des Clients oder des Servers für die EAP-TLS-Authentifizierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5fdab-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fdab-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fdab-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fdab-116">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="5fdab-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




