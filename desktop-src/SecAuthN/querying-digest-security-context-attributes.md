---
description: Die QueryContextAttributes (Digest)-Funktion stellt Informationen über die aktuellen Einstellungen eines Sicherheits Kontexts bereit.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Abfragen von Digest-Sicherheitskontext Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959644"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="325d9-103">Abfragen von Digest-Sicherheitskontext Attributen</span><span class="sxs-lookup"><span data-stu-id="325d9-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="325d9-104">Die [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) -Funktion stellt Informationen über die aktuellen Einstellungen eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="325d9-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="325d9-105">Microsoft Digest unterstützt das Abfragen der folgenden Sicherheitskontext Attribute.</span><span class="sxs-lookup"><span data-stu-id="325d9-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="325d9-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="325d9-106">Attribute</span></span>                   | <span data-ttu-id="325d9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="325d9-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="325d9-108">Informationen zum secpkg- \_ attr- \_ Schlüssel \_</span><span class="sxs-lookup"><span data-stu-id="325d9-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="325d9-109">Informationen in Bezug auf die verwendeten Signatur-und Verschlüsselungsalgorithmen.</span><span class="sxs-lookup"><span data-stu-id="325d9-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="325d9-110">Informationen zum secpkg- \_ attr- \_ Paket \_</span><span class="sxs-lookup"><span data-stu-id="325d9-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="325d9-111">Allgemeine Informationen zu Microsoft Digest, z. b. die maximale Tokengröße, die vom [*Sicherheitspaket*](../secgloss/s-gly.md)zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="325d9-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="325d9-112">secpkg- \_ attr- \_ Größen</span><span class="sxs-lookup"><span data-stu-id="325d9-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="325d9-113">Die maximal zulässige Größe für Nachrichten bezogene Daten, z. b. Signaturen.</span><span class="sxs-lookup"><span data-stu-id="325d9-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
