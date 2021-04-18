---
description: Zertifikaten sind Eigenschaften zugeordnet, z. b. Anzeige Name, Beschreibung und zulässige Verwendung, die angezeigt und bearbeitet werden können.
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: Erstellen, anzeigen und Verwalten von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345038"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="2365a-103">Erstellen, anzeigen und Verwalten von Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="2365a-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="2365a-104">[*Zertifikate*](../secgloss/c-gly.md) sind schreibgeschützte Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2365a-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="2365a-105">Der Inhalt eines Zertifikats kann angezeigt, aber nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2365a-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="2365a-106">Zu den Informationen im Zertifikat selbst gehören die Gültigkeits Daten des Zertifikats, der Aussteller, der Betreff und der öffentliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2365a-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="2365a-107">Allerdings verfügen Zertifikate über zugeordnete Eigenschaften, z. b. einen anzeigen Amen, eine Beschreibung und zulässige Verwendungsmöglichkeiten, die angezeigt und bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="2365a-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="2365a-108">In diesem Abschnitt wird das Erstellen von Test Zertifikaten, das Anzeigen von Zertifikaten und das Verwalten von Zertifikaten und anderen Sicherheits Objekten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2365a-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="2365a-109">Die Zertifikate und [*Software Herausgeber Zertifikate*](../secgloss/s-gly.md) (SPCs), die mit Makecert erstellt werden können, sind ausschließlich für Testzwecke vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="2365a-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="2365a-110">Ein Test Stamm [*Zertifikat*](../secgloss/r-gly.md) und ein [*privater Schlüssel*](../secgloss/p-gly.md) für den Test Stamm werden nur zu Testzwecken bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2365a-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="2365a-111">Unabhängige Softwarehersteller müssen ein Zertifikat von GTE, VeriSign, Inc. oder einer anderen Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) abrufen, um Code zu signieren, der an den öffentlichen verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="2365a-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="2365a-112">Dieser Abschnitt schließt folgende Themen ein:</span><span class="sxs-lookup"><span data-stu-id="2365a-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="2365a-113">Verwenden von Makecert</span><span class="sxs-lookup"><span data-stu-id="2365a-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="2365a-114">Verwenden von Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="2365a-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="2365a-115">Verwenden von certmgr</span><span class="sxs-lookup"><span data-stu-id="2365a-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
