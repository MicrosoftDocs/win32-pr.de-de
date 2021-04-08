---
description: Die Aktion RegisterUser registriert die Benutzerinformationen beim Installationsprogramm, um den Benutzer eines Produkts zu identifizieren.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756463"
---
# <a name="registeruser-action"></a><span data-ttu-id="5b681-103">RegisterUser-Aktion</span><span class="sxs-lookup"><span data-stu-id="5b681-103">RegisterUser Action</span></span>

<span data-ttu-id="5b681-104">Die Aktion RegisterUser registriert die Benutzerinformationen beim Installationsprogramm, um den Benutzer eines Produkts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5b681-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5b681-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5b681-105">Sequence Restrictions</span></span>

<span data-ttu-id="5b681-106">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="5b681-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5b681-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="5b681-107">ActionData Messages</span></span>



| <span data-ttu-id="5b681-108">Feld</span><span class="sxs-lookup"><span data-stu-id="5b681-108">Field</span></span> | <span data-ttu-id="5b681-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="5b681-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="5b681-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5b681-110">\[1\]</span></span> | <span data-ttu-id="5b681-111">Registrierte Benutzerinformationen.</span><span class="sxs-lookup"><span data-stu-id="5b681-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5b681-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b681-112">Remarks</span></span>

<span data-ttu-id="5b681-113">Die Aktion "RegisterUser" wird während einer administrativen Installation nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b681-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="5b681-114">Wenn der vom Benutzer eingegebene Produkt Bezeichner nicht durch die [ValidateProductID-Aktion](validateproductid-action.md)überprüft wurde, ist die [**ProductID-**](productid.md) Eigenschaft nicht festgelegt, und diese Aktion führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5b681-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b681-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b681-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b681-116">**User**</span><span class="sxs-lookup"><span data-stu-id="5b681-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="5b681-117">**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="5b681-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="5b681-118">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="5b681-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



