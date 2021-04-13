---
description: Erläutert, wie Zertifikat Dienste Zertifikat Anforderungen verarbeiten.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Verarbeiten von Zertifikat Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561427"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="e80e2-103">Verarbeiten von Zertifikat Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e80e2-103">Processing Certificate Requests</span></span>

<span data-ttu-id="e80e2-104">Die Zertifikat Dienste führen die folgenden Schritte aus, wenn eine [*Zertifikat Anforderung*](../secgloss/c-gly.md)verarbeitet wird:</span><span class="sxs-lookup"><span data-stu-id="e80e2-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="e80e2-105">Anforderungs Empfang.</span><span class="sxs-lookup"><span data-stu-id="e80e2-105">Request reception.</span></span>

    <span data-ttu-id="e80e2-106">Die [*Zertifikat Anforderung*](../secgloss/c-gly.md) wird vom Client an eine Vermittler Anwendung gesendet, die Sie in eine PKCS \# 10-Format Anforderung formatiert und an die Server-Engine übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e80e2-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="e80e2-107">Genehmigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e80e2-107">Request approval.</span></span>

    <span data-ttu-id="e80e2-108">Die Server-Engine Ruft das- [Richtlinien Modul](policy-modules.md)auf, das Anforderungs Eigenschaften abfragt, entscheidet, ob die Anforderung autorisiert ist oder nicht, und legt optionale Zertifikat Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="e80e2-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="e80e2-109">Zertifikats Bildung.</span><span class="sxs-lookup"><span data-stu-id="e80e2-109">Certificate formation.</span></span>

    <span data-ttu-id="e80e2-110">Wenn die Anforderung genehmigt ist, übernimmt die Server-Engine die Anforderung und alle Eigenschaften, die vom Richtlinien Modul angefordert werden, und erstellt ein umfassendes Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="e80e2-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="e80e2-111">Zertifikat Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="e80e2-111">Certificate publication.</span></span>

    <span data-ttu-id="e80e2-112">Die Server-Engine speichert das abgeschlossene Zertifikat in der Datenbank der Zertifikat Dienste und benachrichtigt die Vermittler Anwendung über den Anforderungs Status.</span><span class="sxs-lookup"><span data-stu-id="e80e2-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="e80e2-113">Wenn das Beendigungs [Modul](exit-modules.md) dies angefordert hat, wird es vom Servermodul über ein Zertifikat Ausstellungs Ereignis benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="e80e2-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="e80e2-114">Dadurch kann das Beendigungs Modul weitere Vorgänge ausführen, wie z. b. das Veröffentlichen des Zertifikats in einem externen zertifikatrepository (z. b. einem Verzeichnisdienst).</span><span class="sxs-lookup"><span data-stu-id="e80e2-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="e80e2-115">Zwischenzeitlich erhält der Vermittler das veröffentlichte Zertifikat von den Zertifikat Diensten und übergibt es an den Client.</span><span class="sxs-lookup"><span data-stu-id="e80e2-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="e80e2-116">In der folgenden Abbildung wird gezeigt, wie eine [*Zertifikat Anforderung*](../secgloss/c-gly.md) von Zertifikat Diensten verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e80e2-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![Verarbeiten einer Zertifikat Anforderung](images/certflow.png)

 

 
