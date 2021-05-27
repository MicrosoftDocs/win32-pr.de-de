---
title: D1104 – Möglicher Verlust
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Die Factory wurde freigegeben, aber die daraus erstellte Schnittstelle ist noch aktiv. Es ist zwar gültig, Ressourcen nach der Freigabe der Factory freizugeben, aber diese Bedingung kann auf einen Speicherverlust hindeuten.
keywords:
- D1104 Possible Leak Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548675"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="ef9ed-105">D1104: Möglicher Verlust</span><span class="sxs-lookup"><span data-stu-id="ef9ed-105">D1104: Possible Leak</span></span>

<span data-ttu-id="ef9ed-106">Die \[ *Factory* \] wurde veröffentlicht, aber die von ihr erstellte \[ *Schnittstellenschnittstelle* \] ist noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="ef9ed-107">Es ist zwar gültig, Ressourcen nach der Freigabe der Factory freizugeben, aber diese Bedingung kann auf einen Speicherverlust hindeuten.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="ef9ed-108">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="ef9ed-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="ef9ed-109"><span id="factory"></span><span id="FACTORY"></span>*Fabrik*</span><span class="sxs-lookup"><span data-stu-id="ef9ed-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="ef9ed-110">Die Adresse der Factory, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="ef9ed-111"><span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*</span><span class="sxs-lookup"><span data-stu-id="ef9ed-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="ef9ed-112">Die Adresse der Schnittstelle, die in der *Factory* erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="ef9ed-113">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="ef9ed-113">Error Level</span></span> | <span data-ttu-id="ef9ed-114">Information</span><span class="sxs-lookup"><span data-stu-id="ef9ed-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="ef9ed-115">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="ef9ed-115">Possible Causes</span></span>

<span data-ttu-id="ef9ed-116">Die Factory wurde freigegeben, aber die daraus erstellte Schnittstelle ist noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




