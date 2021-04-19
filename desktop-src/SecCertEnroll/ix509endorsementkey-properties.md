---
description: Die IX509EndorsementKey-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: IX509EndorsementKey-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362319"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="f613e-103">IX509EndorsementKey-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f613e-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="f613e-104">Die [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f613e-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f613e-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f613e-105">In this section</span></span>



| <span data-ttu-id="f613e-106">Thema</span><span class="sxs-lookup"><span data-stu-id="f613e-106">Topic</span></span>                                                                        | <span data-ttu-id="f613e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f613e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f613e-108">**Längeneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f613e-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="f613e-109">Die Bitlänge des Endorsement Key.</span><span class="sxs-lookup"><span data-stu-id="f613e-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="f613e-110">Sie können nur auf diese Eigenschaft zugreifen, nachdem die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f613e-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="f613e-111">**Geöffnete Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f613e-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="f613e-112">Gibt an, ob die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode erfolgreich aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f613e-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f613e-113">**ProviderName-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f613e-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="f613e-114">Der Name des Verschlüsselungsanbieters.</span><span class="sxs-lookup"><span data-stu-id="f613e-114">The name of the encryption provider.</span></span> <span data-ttu-id="f613e-115">Der Standardwert ist der Kryptografieanbieter der Microsoft-Plattform.</span><span class="sxs-lookup"><span data-stu-id="f613e-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="f613e-116">Sie müssen die [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) -Eigenschaft festlegen, bevor Sie die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f613e-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="f613e-117">Sie können die **providerName** -Eigenschaft nicht ändern, nachdem Sie die **Open** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="f613e-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




