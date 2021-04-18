---
description: Die iupdateserviceregistration-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Iupdateserviceregistration-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344867"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="6d440-103">Iupdateserviceregistration-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d440-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="6d440-104">Die **iupdateserviceregistration** -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6d440-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="6d440-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d440-105">Property</span></span>                                                                                      | <span data-ttu-id="6d440-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d440-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d440-107">**Ispendingregistrationwithau**</span><span class="sxs-lookup"><span data-stu-id="6d440-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="6d440-108">Ruft einen booleschen Wert ab, der angibt, ob der Dienst beim Hinzufügen auch bei automatische Updates registriert wird.</span><span class="sxs-lookup"><span data-stu-id="6d440-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="6d440-109">**RegistrationState**</span><span class="sxs-lookup"><span data-stu-id="6d440-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="6d440-110">Ruft einen [**updateserviceregistrationstate**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) -Wert ab, der den aktuellen Status der Dienst Registrierung angibt.</span><span class="sxs-lookup"><span data-stu-id="6d440-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="6d440-111">**Dienst**</span><span class="sxs-lookup"><span data-stu-id="6d440-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="6d440-112">Ruft einen Zeiger auf eine [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="6d440-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="6d440-113">Diese Eigenschaft ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d440-113">This property is the default property.</span></span>                                    |



 

 

 



