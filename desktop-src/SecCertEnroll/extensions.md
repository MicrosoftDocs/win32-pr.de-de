---
description: Das X. 509 Version 3-Zertifikat Format identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Erweiterungen (Zertifikatregistrierungs-API)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362832"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="8cabf-103">Erweiterungen (Zertifikatregistrierungs-API)</span><span class="sxs-lookup"><span data-stu-id="8cabf-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="8cabf-104">Das X. 509 Version 3-Zertifikat Format identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="8cabf-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="8cabf-105">Die Erweiterungen bieten erweiterte Informationen zu Schlüssel Verwendung, Zertifikat Richtlinien und-Einschränkungen, Alternativen namens Formularen und mehr.</span><span class="sxs-lookup"><span data-stu-id="8cabf-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="8cabf-106">Mit der [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle können Sie einen Erweiterungs Wert definieren.</span><span class="sxs-lookup"><span data-stu-id="8cabf-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="8cabf-107">Viele der allgemeinen Erweiterungen können mithilfe von vordefinierten Schnittstellen erstellt werden, die von **IX509Extension** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8cabf-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="8cabf-108">Eine Auflistung von Erweiterungen wird einer Zertifikat Anforderung hinzugefügt, indem die Auflistung in die Anforderungs Attribute eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8cabf-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="8cabf-109">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="8cabf-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8cabf-110">Unterstützte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8cabf-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="8cabf-111">PKCS \# 10-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8cabf-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="8cabf-112">CMC-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8cabf-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



