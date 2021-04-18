---
description: Microsoft hat die DPAPI (Data Protection Application Programming Interface) in Windows 2000 eingeführt.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG-DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344871"
---
# <a name="cng-dpapi"></a><span data-ttu-id="06946-103">CNG-DPAPI</span><span class="sxs-lookup"><span data-stu-id="06946-103">CNG DPAPI</span></span>

<span data-ttu-id="06946-104">Microsoft hat die DPAPI (Data Protection Application Programming Interface) in Windows 2000 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="06946-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="06946-105">Die API besteht aus zwei Funktionen: " [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) " und " [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)".</span><span class="sxs-lookup"><span data-stu-id="06946-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="06946-106">DPAPI ist Teil von CryptoAPI und wurde für Entwickler gedacht, die sehr wenig über die Verwendung von Kryptografie wussten.</span><span class="sxs-lookup"><span data-stu-id="06946-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="06946-107">Die beiden Funktionen können verwendet werden, um statische Daten auf einem einzelnen Computer zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="06946-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="06946-108">Cloud Computing erfordert jedoch häufig, dass auf einem Computer verschlüsselte Inhalte auf einem anderen Computer entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="06946-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="06946-109">Daher hat Microsoft ab Windows 8 die Idee erweitert, eine relativ unkomplizierte API zu verwenden, um cloudszenarien abzudecken.</span><span class="sxs-lookup"><span data-stu-id="06946-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="06946-110">Diese neue API mit dem Namen "DPAPI-ng" ermöglicht es Ihnen, geheime Schlüssel (Schlüssel, Kenn Wörter, Schlüsselmaterial) und Nachrichten sicher zu teilen, indem Sie Sie für einen Satz von Prinzipalen schützen, die verwendet werden können, um Sie nach entsprechender Authentifizierung und Autorisierung auf unterschiedlichen Computern zu schützen.</span><span class="sxs-lookup"><span data-stu-id="06946-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="06946-111">Die folgenden Prinzipale werden zurzeit unterstützt:</span><span class="sxs-lookup"><span data-stu-id="06946-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="06946-112">Eine Gruppe in einer Active Directory Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="06946-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="06946-113">Webanmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="06946-113">Web credentials.</span></span>

<span data-ttu-id="06946-114">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="06946-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="06946-115">Schutz Anbieter</span><span class="sxs-lookup"><span data-stu-id="06946-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="06946-116">Schutz Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="06946-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="06946-117">Geschütztes Daten Format</span><span class="sxs-lookup"><span data-stu-id="06946-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="06946-118">DPAPI-ng basiert auf der Cryptography Next Generation (CNG) und umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="06946-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="06946-119">**Ncryptkreateschutzdescriptor**</span><span class="sxs-lookup"><span data-stu-id="06946-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="06946-120">**Ncryptcloseschutzdescriptor**</span><span class="sxs-lookup"><span data-stu-id="06946-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="06946-121">**Ncryptprotectsecret**</span><span class="sxs-lookup"><span data-stu-id="06946-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="06946-122">**Ncryptqueryschutzdescriptor Name**</span><span class="sxs-lookup"><span data-stu-id="06946-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="06946-123">**Ncryptregisterschutzdescriptor Name**</span><span class="sxs-lookup"><span data-stu-id="06946-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="06946-124">**Ncryptstreamclose**</span><span class="sxs-lookup"><span data-stu-id="06946-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="06946-125">**Ncryptstreamopentoprotect**</span><span class="sxs-lookup"><span data-stu-id="06946-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="06946-126">**Ncryptstreamopentounprotect**</span><span class="sxs-lookup"><span data-stu-id="06946-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="06946-127">**Ncryptstreamupdate**</span><span class="sxs-lookup"><span data-stu-id="06946-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="06946-128">**Ncryptunprotectsecret**</span><span class="sxs-lookup"><span data-stu-id="06946-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
