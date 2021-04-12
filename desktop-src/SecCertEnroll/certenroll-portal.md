---
description: Beispiel für ein Zertifikat. Erstellen Sie Anwendungen für die API-Zertifizierung, installieren Sie das SSL-Zertifikat, das Serverzertifikat, und erstellen Sie Zertifikate über Medien wie das Internet oder ein Intranet, die nicht grundsätzlich sicher sind.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: Certificate Enrollment API (Zertifikatregistrierungs-API, in englischer Sprache)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526336"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="6fa6c-104">Certificate Enrollment API (Zertifikatregistrierungs-API, in englischer Sprache)</span><span class="sxs-lookup"><span data-stu-id="6fa6c-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="6fa6c-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="6fa6c-105">Purpose</span></span>

<span data-ttu-id="6fa6c-106">Die Zertifikatregistrierungs-API kann verwendet werden, um eine Client Anwendung zum Anfordern eines Zertifikats und zum Installieren einer Zertifikats Antwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="6fa6c-107">Diese API wird in CertEnroll.dll ab Windows Vista implementiert. Xenroll.dll wird ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6fa6c-108">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="6fa6c-108">Developer audience</span></span>

<span data-ttu-id="6fa6c-109">Die Zertifikatregistrierungs-API dient der Verwendung durch Entwickler von Anwendungen, die es Benutzern ermöglichen, Zertifikate über Medien wie das Internet oder ein Intranet zu erstellen, anzufordern und abzurufen, die von Natur aus nicht sicher sind.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="6fa6c-110">Entwickler sollten mit den Programmiersprachen C und C++, dem Component Object Model (com) und der Windows-basierten Programmierumgebung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="6fa6c-111">Es ist zwar nicht erforderlich, aber es wird empfohlen, die Kryptografie und die Public Key-Infrastruktur zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6fa6c-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="6fa6c-112">Run-time requirements</span></span>

<span data-ttu-id="6fa6c-113">Die Zertifikatregistrierungs-API wird ab Windows Server 2008 und Windows Vista unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="6fa6c-114">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6fa6c-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6fa6c-115">In this section</span></span>



| <span data-ttu-id="6fa6c-116">Thema</span><span class="sxs-lookup"><span data-stu-id="6fa6c-116">Topic</span></span>                                                                                       | <span data-ttu-id="6fa6c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fa6c-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fa6c-118">Informationen zur Zertifikatregistrierungs-API</span><span class="sxs-lookup"><span data-stu-id="6fa6c-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="6fa6c-119">Wichtige Konzepte zu Zertifikat Anforderungen werden erörtert.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="6fa6c-120">Verwenden der Zertifikatregistrierungs-API</span><span class="sxs-lookup"><span data-stu-id="6fa6c-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="6fa6c-121">Verwenden der Zertifikatregistrierungs-API, um die Funktionen von Active Directory Zertifikat Dienste zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="6fa6c-122">Zertifikatregistrierungs-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="6fa6c-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="6fa6c-123">Ausführliche Beschreibungen der Schnittstellen, Enumerationen und anderen Programmier Elemente, die zum Registrieren eines Benutzers oder Computers in einer Zertifikat Hierarchie verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6fa6c-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




