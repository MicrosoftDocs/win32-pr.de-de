---
title: Cenum var. CPP
description: In der Beispiel Anbieter Komponente finden Sie die Basis Implementierung für von xxxenenumvariant abgeleitete Klassen in "cenenumvar. cpp". Die zugehörigen Methoden sind in der folgenden Tabelle aufgeführt.
ms.assetid: 6b38bc99-25d4-40af-863a-9cc37f786d9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d361cb7d3e2657a31645fba05aa2e1a23762a3fc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316437"
---
# <a name="cenumvarcpp"></a><span data-ttu-id="8d7b9-104">Cenum var. CPP</span><span class="sxs-lookup"><span data-stu-id="8d7b9-104">CENUMVAR.CPP</span></span>

<span data-ttu-id="8d7b9-105">In der Beispiel Anbieter Komponente finden Sie die Basis Implementierung für von xxxenenumvariant abgeleitete Klassen in "cenenumvar. cpp".</span><span class="sxs-lookup"><span data-stu-id="8d7b9-105">In the example provider component, the base implementation for xxxEnumVariant derived classes can be found in cenumvar.cpp.</span></span> <span data-ttu-id="8d7b9-106">Die zugehörigen Methoden sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-106">Associated methods are listed in the following table.</span></span>



| <span data-ttu-id="8d7b9-107">Methode</span><span class="sxs-lookup"><span data-stu-id="8d7b9-107">Method</span></span>                                          | <span data-ttu-id="8d7b9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d7b9-108">Description</span></span>                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7b9-109">**Csampledsenum Variant:: csampledsenumschlag**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span></span>  | <span data-ttu-id="8d7b9-110">Standardkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-110">Standard constructor.</span></span>                                                                 |
| <span data-ttu-id="8d7b9-111">**Csampledsenum Variant:: ~ csampledsenumschlag**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-111">**CSampleDSEnumVariant::~CSampleDSEnumVariant**</span></span> | <span data-ttu-id="8d7b9-112">Standardedekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-112">Standard destructor.</span></span>                                                                  |
| <span data-ttu-id="8d7b9-113">**Csampledsenumschlag:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-113">**CSampleDSEnumVariant::QueryInterface**</span></span>        | <span data-ttu-id="8d7b9-114">Standard mäßige [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-114">Standard [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) implementation.</span></span> |
| <span data-ttu-id="8d7b9-115">**Csampledsenumschlag:: adressf**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-115">**CSampleDSEnumVariant::AddRef**</span></span>                | <span data-ttu-id="8d7b9-116">Standard mäßige [**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-116">Standard [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) implementation.</span></span>                 |
| <span data-ttu-id="8d7b9-117">**Csampledsenum Variant:: Release**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-117">**CSampleDSEnumVariant::Release**</span></span>               | <span data-ttu-id="8d7b9-118">Standard mäßige [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-118">Standard [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) implementation.</span></span>               |
| <span data-ttu-id="8d7b9-119">**Csampledsenübervariant:: Skip**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-119">**CSampleDSEnumVariant::Skip**</span></span>                  | <span data-ttu-id="8d7b9-120">Standard mäßige **IEnumXXXX:: Skip** -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-120">Standard **IEnumXXXX::Skip** implementation.</span></span>                                          |
| <span data-ttu-id="8d7b9-121">**Csampledsenum Variant:: Reset**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-121">**CSampleDSEnumVariant::Reset**</span></span>                 | <span data-ttu-id="8d7b9-122">Standard **IEnumXXXX:: Reset** -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-122">Standard **IEnumXXXX::Reset** implementation.</span></span>                                         |
| <span data-ttu-id="8d7b9-123">**Csampledsenumschlag:: Clone**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-123">**CSampleDSEnumVariant::Clone**</span></span>                 | <span data-ttu-id="8d7b9-124">Standard mäßige **IEnumXXXX:: Clone** -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-124">Standard **IEnumXXXX::Clone** implementation.</span></span>                                         |



 

 

 