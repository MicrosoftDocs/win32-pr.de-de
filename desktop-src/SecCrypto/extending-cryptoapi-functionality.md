---
description: Die Zukunft der Kryptografie und der sicheren Kommunikation kann nicht leicht vorhergesagt werden.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Erweitern der kryptoapi-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960700"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="aa0f7-103">Erweitern der kryptoapi-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="aa0f7-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="aa0f7-104">Die Zukunft der [*Kryptografie*](../secgloss/c-gly.md) und der sicheren Kommunikation kann nicht leicht vorhergesagt werden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="aa0f7-105">Möglicherweise werden neue Zertifikat Typen angezeigt, verschiedene Zertifikat Erweiterungen können häufig verwendet werden, und es können neue Nachrichten Typen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="aa0f7-106">Daher ist die Erweiterbarkeit Teil des Entwurfs wichtiger [*CryptoAPI*](../secgloss/c-gly.md) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="aa0f7-107">Die folgenden Abschnitte enthalten Übersichten zur Verwendung von OIDs zum Erweitern von CryptoAPI-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="aa0f7-108">Thema</span><span class="sxs-lookup"><span data-stu-id="aa0f7-108">Topic</span></span>                                                                              | <span data-ttu-id="aa0f7-109">Inhalte</span><span class="sxs-lookup"><span data-stu-id="aa0f7-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa0f7-110">OID-Übersicht</span><span class="sxs-lookup"><span data-stu-id="aa0f7-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="aa0f7-111">Grundlegende Konzepte von OID.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="aa0f7-112">Erstellen der neuen Funktionalität</span><span class="sxs-lookup"><span data-stu-id="aa0f7-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="aa0f7-113">Erstellen von OIDs und Funktionen zum Erweitern der Verwendung vorhandener APIs.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="aa0f7-114">Registrieren der neuen Funktionalität</span><span class="sxs-lookup"><span data-stu-id="aa0f7-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="aa0f7-115">Einrichten neuer OID-bezogener Funktionen.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="aa0f7-116">Installieren der neuen Funktionalität</span><span class="sxs-lookup"><span data-stu-id="aa0f7-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="aa0f7-117">Installieren von OID-Funktionen im Speicher, um die Leistung zu verbessern</span><span class="sxs-lookup"><span data-stu-id="aa0f7-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="aa0f7-118">Erweitern der certopsstore-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="aa0f7-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="aa0f7-119">Erweitern der [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) -Funktionalität mithilfe installier barer oder registrierter Zertifikat Speicher Anbieter-Funktion.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
