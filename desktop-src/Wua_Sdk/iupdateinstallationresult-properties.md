---
description: Die iupdateingestallationresult-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Iupdateingestallationresult-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214730"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="cc80d-103">Iupdateingestallationresult-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc80d-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="cc80d-104">Die [**iupdateingestallationresult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc80d-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="cc80d-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc80d-105">Property</span></span>                                                           | <span data-ttu-id="cc80d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc80d-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc80d-107">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc80d-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="cc80d-108">Ruft den **HRESULT** -Ausnahme Wert ab, der während des Vorgangs bei einem Update ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="cc80d-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="cc80d-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="cc80d-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="cc80d-110">Ruft einen booleschen Wert ab, der angibt, ob auf einem Computer ein Systemneustart erforderlich ist, um die Installation eines Updates abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cc80d-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="cc80d-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="cc80d-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="cc80d-112">Ruft einen [**operationresultcode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) -Wert ab, der das Ergebnis eines Vorgangs bei einem Update angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80d-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



