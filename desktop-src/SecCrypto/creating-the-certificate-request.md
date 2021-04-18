---
description: Beim Erstellen einer Zertifikat Anforderung werden bestimmte Informationen von der anfordernden Person gesammelt.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Erstellen der Zertifikat Anforderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347137"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="0ff9e-103">Erstellen der Zertifikat Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ff9e-103">Creating the Certificate Request</span></span>

<span data-ttu-id="0ff9e-104">Beim Erstellen einer Zertifikat Anforderung werden bestimmte Informationen von der anfordernden Person gesammelt.</span><span class="sxs-lookup"><span data-stu-id="0ff9e-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="0ff9e-105">Dies erfolgt in der Regel über eine Art von Benutzeroberfläche (User Interface, UI), obwohl die Informationen direkt aus einer Datenbank abgerufen werden können, ohne dass eine Benutzeroberfläche erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0ff9e-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="0ff9e-106">Die erforderliche Ebene der Informationen wird durch die Richtlinie der Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ff9e-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="0ff9e-107">Ein Beispiel für die erforderlichen Informationen könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="0ff9e-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="0ff9e-108">Allgemeiner Name</span><span class="sxs-lookup"><span data-stu-id="0ff9e-108">Common Name</span></span>
-   <span data-ttu-id="0ff9e-109">Einheits Name</span><span class="sxs-lookup"><span data-stu-id="0ff9e-109">Unit Name</span></span>
-   <span data-ttu-id="0ff9e-110">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="0ff9e-110">Company Name</span></span>
-   <span data-ttu-id="0ff9e-111">City</span><span class="sxs-lookup"><span data-stu-id="0ff9e-111">City</span></span>
-   <span data-ttu-id="0ff9e-112">State</span><span class="sxs-lookup"><span data-stu-id="0ff9e-112">State</span></span>
-   <span data-ttu-id="0ff9e-113">Land/Region</span><span class="sxs-lookup"><span data-stu-id="0ff9e-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="0ff9e-114">Die-Schnittstelle ist so konzipiert, dass für jede Xenroll-Instanz eine einzelne Anforderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ff9e-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="0ff9e-115">Eine separate Xenroll-Instanz muss erstellt werden, um jede [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ff9e-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="0ff9e-116">Informationen zur Verwendung der Zertifikat Registrierungs Steuerung zum Anfordern eines Zertifikats in bestimmten Programmiersprachen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0ff9e-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="0ff9e-117">Anforderungs Beispiel in C++</span><span class="sxs-lookup"><span data-stu-id="0ff9e-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="0ff9e-118">Anforderungs Beispiel in VBScript</span><span class="sxs-lookup"><span data-stu-id="0ff9e-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
