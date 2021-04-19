---
title: IConfigAsfWriter2 GetParam-Methode
description: Die GetParam-Methode ruft den aktuellen Wert des angegebenen Filter Konfigurations Parameters ab.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- GetParam-Methode Windows Media-Format
- GetParam-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, GetParam-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339508"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="1f141-106">IConfigAsfWriter2:: GetParam-Methode</span><span class="sxs-lookup"><span data-stu-id="1f141-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="1f141-107">Die **GetParam** -Methode ruft den aktuellen Wert des angegebenen Filter Konfigurations Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="1f141-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f141-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f141-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="1f141-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f141-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f141-110">*dwparam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f141-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f141-111">Gibt den Parameter an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f141-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="1f141-112">Dabei muss es sich um einen Wert handeln, der in der Enumeration [ \_ am \_ asfschreiterconfig-Parameter \_ ](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f141-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1f141-113">*pdwParam1* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f141-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f141-114">Ein Zeiger auf eine Variable, die den Wert des in *dwparam* angegebenen Parameters abruft.</span><span class="sxs-lookup"><span data-stu-id="1f141-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="1f141-115">*pdwParam2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f141-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f141-116">Nicht verwendet, muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="1f141-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f141-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f141-117">Return value</span></span>

<span data-ttu-id="1f141-118">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="1f141-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="1f141-119">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f141-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f141-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f141-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f141-121">[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1f141-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1f141-122">**IConfigAsfWriter2:: SetParam**</span><span class="sxs-lookup"><span data-stu-id="1f141-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 