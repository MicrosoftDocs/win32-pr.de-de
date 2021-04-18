---
title: Iwmdrmlicense getoutputschutzlevels-Methode
description: Die getoutputschutzlevels-Methode ruft Informationen zu allen Ausgabe Schutz Ebenen (opls) ab, die der Lizenz zugewiesen sind.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Getoutputschutzlevels-Methode Windows Media-Format
- Getoutputschutzlevels-Methode, Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getoutputschutzlevels-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338225"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="eef1f-106">Iwmdrmlicense:: getoutputschutzlevels-Methode</span><span class="sxs-lookup"><span data-stu-id="eef1f-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="eef1f-107">Die **getoutputschutzlevels** -Methode ruft Informationen zu allen Ausgabe Schutz Ebenen (opls) ab, die der Lizenz zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="eef1f-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef1f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eef1f-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="eef1f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eef1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef1f-110">*popls* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eef1f-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eef1f-111">Zeiger auf eine [**WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen**](wmdrm-output-protection-levels.md) -Struktur, die die OPL-Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="eef1f-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef1f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eef1f-112">Return value</span></span>

<span data-ttu-id="eef1f-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="eef1f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eef1f-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="eef1f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eef1f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eef1f-115">Return code</span></span>                                                                          | <span data-ttu-id="eef1f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eef1f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="eef1f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eef1f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="eef1f-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eef1f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eef1f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eef1f-119">Remarks</span></span>

<span data-ttu-id="eef1f-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="eef1f-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="eef1f-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eef1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef1f-122">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eef1f-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





