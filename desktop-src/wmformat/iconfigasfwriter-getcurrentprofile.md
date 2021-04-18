---
title: Iconfigasfwriter getcurrentprofile-Methode
description: Die getcurrentprofile-Methode ruft das Anwendungs definierte Profil ab.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Getcurrentprofile-Methode Windows Media-Format
- Getcurrentprofile-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getcurrentprofile-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338069"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="e7699-106">Iconfigasfwriter:: getcurrentprofile-Methode</span><span class="sxs-lookup"><span data-stu-id="e7699-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="e7699-107">Die **getcurrentprofile** -Methode ruft das Anwendungs definierte Profil ab.</span><span class="sxs-lookup"><span data-stu-id="e7699-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7699-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7699-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="e7699-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7699-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7699-110">*ppprofile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7699-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7699-111">Adresse eines Zeigers, der die [**iwmprofile**](iwmprofile.md) -Schnittstelle des Anwendungs definierten Profils empfängt.</span><span class="sxs-lookup"><span data-stu-id="e7699-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7699-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7699-112">Return value</span></span>

<span data-ttu-id="e7699-113">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e7699-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e7699-114">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7699-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7699-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7699-115">Remarks</span></span>

<span data-ttu-id="e7699-116">Wenn die Methode erfolgreich ausgeführt wird, weist der zurückgegebene **iwmprofile** -Zeiger einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="e7699-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="e7699-117">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="e7699-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7699-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7699-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7699-119">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7699-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 