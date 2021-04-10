---
description: Die iinstallationresult-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Iinstallationresult-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041790"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="8b28d-103">Iinstallationresult-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b28d-103">IInstallationResult Properties</span></span>

<span data-ttu-id="8b28d-104">Die [**iinstallationresult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b28d-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="8b28d-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8b28d-105">Property</span></span>                                                     | <span data-ttu-id="8b28d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b28d-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b28d-107">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b28d-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="8b28d-108">Ruft das **HRESULT** der Ausnahme ab, sofern vorhanden, das während der Installation ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8b28d-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="8b28d-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="8b28d-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="8b28d-110">Ruft einen booleschen Wert ab, der angibt, ob der Computer neu gestartet werden muss, um die Installation oder die Installation eines Updates abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8b28d-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="8b28d-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="8b28d-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="8b28d-112">Ruft einen [**operationresultcode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) -Wert ab, der das Ergebnis eines Vorgangs bei einem Update angibt.</span><span class="sxs-lookup"><span data-stu-id="8b28d-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



