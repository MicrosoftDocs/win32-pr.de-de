---
title: IConfigAsfWriter2 resetmultipassstate-Methode
description: Die resetmultipassstate-Methode setzt den Filter zurück, wenn ein Vorverarbeitungs-Codierungs Durchlauf abgebrochen wird, bevor er abgeschlossen wird.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Resetmultipassstate-Methode, Windows Media-Format
- Resetmultipassstate-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, resetmultipassstate-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390805"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="3a717-106">IConfigAsfWriter2:: resetmultipassstate-Methode</span><span class="sxs-lookup"><span data-stu-id="3a717-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="3a717-107">Die **resetmultipassstate** -Methode setzt den Filter zurück, wenn ein Vorverarbeitungs-Codierungs Durchlauf abgebrochen wird, bevor er abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3a717-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a717-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a717-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="3a717-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a717-109">Parameters</span></span>

<span data-ttu-id="3a717-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3a717-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a717-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a717-111">Return value</span></span>

<span data-ttu-id="3a717-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="3a717-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3a717-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3a717-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3a717-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3a717-114">Return code</span></span>                                                                                         | <span data-ttu-id="3a717-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a717-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="3a717-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a717-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="3a717-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a717-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="3a717-118"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="3a717-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="3a717-119">Der Filter befand sich nicht im beendeten Zustand.</span><span class="sxs-lookup"><span data-stu-id="3a717-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a717-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a717-120">Remarks</span></span>

<span data-ttu-id="3a717-121">Diese Methode muss aufgerufen werden, um den internen Zustand des Filters zurückzusetzen, wenn ein Vorverarbeitungs-Codierungs Durchlauf abgebrochen wird, bevor der Filter ein Ereignis zum **abschließen des Vorgangs "EC \_ Preprocess \_** " empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="3a717-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="3a717-122">Es ist nicht erforderlich, diese Methode aufzurufen, wenn der Vorverarbeitungs-Codierungs Durchlauf ohne Fehler abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3a717-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a717-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a717-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a717-124">[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a717-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

