---
description: Die Zertifikat Dienste unterstützen Zertifizierungsstellen Hierarchien (Certification Authority, ca).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarchien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359442"
---
# <a name="hierarchies"></a><span data-ttu-id="420af-103">Hierarchien</span><span class="sxs-lookup"><span data-stu-id="420af-103">Hierarchies</span></span>

<span data-ttu-id="420af-104">Die Zertifikat Dienste unterstützen Zertifizierungsstellen Hierarchien ( [*Certification Authority*](../secgloss/c-gly.md) , ca).</span><span class="sxs-lookup"><span data-stu-id="420af-104">Certificate Services supports [*certification authority*](../secgloss/c-gly.md) (CA) hierarchies.</span></span> <span data-ttu-id="420af-105">Eine Zertifizierungsstellen [*Hierarchie*](../secgloss/c-gly.md) besteht aus einer Zertifizierungsstelle der obersten Ebene (als Stamm Zertifizierungsstelle bezeichnet) mit einer oder mehreren untergeordneten Zertifizierungsstellen, die von der Stamm Zertifizierungsstelle Zertifikate ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="420af-105">A [*CA hierarchy*](../secgloss/c-gly.md) consists of a top-level CA (called the Root CA) with one or more subordinate CAs which have been issued certificates by the root CA.</span></span> <span data-ttu-id="420af-106">Ein mögliches Szenario der Zertifizierungsstellen Hierarchie wäre in einer Organisation mit einer Stamm Zertifizierungsstelle, die zum Ausstellen von Zertifikaten für mehrere untergeordnete Zertifizierungsstellen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="420af-106">A possible CA hierarchy scenario would be in an organization with one root CA, which was used to issue certificates to several subordinate CAs.</span></span> <span data-ttu-id="420af-107">Die untergeordneten ZS können dann Endentitäts Zertifikate ausstellen, z. b. Zertifikate, die für einen Benutzer ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="420af-107">The subordinate CAs can then issue end-entity certificates, such as certificates issued to a user.</span></span> <span data-ttu-id="420af-108">Das Zertifikat des Benutzers enthält einen Vertrauensstellungs Pfad für die Zertifizierungsstellen Hierarchie, in diesem Fall das Zertifikat für die ausstellende untergeordnete Zertifizierungsstelle und die Stamm Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="420af-108">The user's certificate will contain a trust path for the CA hierarchy, in this case, including the certificate for both the issuing subordinate CA as well as the root CA.</span></span>

 

 
