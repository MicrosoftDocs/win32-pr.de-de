---
description: Client-und Server Zertifikate müssen in einem Zertifikat Speicher gespeichert werden, der für den Anwendungsprozess zugänglich ist.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Zertifikatspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042013"
---
# <a name="certificate-stores"></a><span data-ttu-id="d1840-103">Zertifikatspeicher</span><span class="sxs-lookup"><span data-stu-id="d1840-103">Certificate Stores</span></span>

<span data-ttu-id="d1840-104">[*Client*](/windows/desktop/SecGloss/c-gly) -und [*Server Zertifikate*](/windows/desktop/SecGloss/s-gly) müssen in einem [*Zertifikat Speicher*](/windows/desktop/SecGloss/c-gly) gespeichert werden, der für den Anwendungsprozess zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="d1840-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="d1840-105">In der Regel ist dies der My-Speicher, der auch als persönlicher Speicher bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d1840-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="d1840-106">Client Anwendungen, wie z. b. Internet Explorer, verwenden normalerweise den eigenen Speicher des aktuellen Benutzers, während Server wie Internetinformationsdienste (IIS) den systemeigenen Speicher des lokalen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1840-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="d1840-107">Der Stamm Speicher und der [*Zertifizierungs*](/windows/desktop/SecGloss/c-gly) stellen Speicher werden verwendet, wenn SChannel oder eine Anwendung eine Zertifikat Kette erstellt, die an den Remote Computer gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1840-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="d1840-108">Diese Speicher werden verwendet, um eine empfangene Zertifikatskette zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d1840-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="d1840-109">Weitere Informationen finden Sie unter [Durchführen der Authentifizierung mithilfe von SChannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="d1840-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
