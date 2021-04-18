---
title: Iconfigasfwriter-Methode "konfigurifisingprofile"
description: Die Methode "Konfigurations Methode" ist die empfohlene Vorgehensweise zum Festlegen eines Profils. Er konfiguriert den Filter zum Schreiben einer ASF-Datei auf Grundlage des angegebenen Anwendungs definierten Profils.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Konfigurieren von Windows Media-Format für die Methode "Konfigurations Methode"
- Konfigurations Methode für das Windows Media-Format (Windows Media Format), iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, Methode "konfigurifiterusingprofile"
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338083"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="da44c-107">Iconfigasfwriter:: konfiguriert refilterusingprofile-Methode</span><span class="sxs-lookup"><span data-stu-id="da44c-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="da44c-108">Die Methode " **Konfigurations** Methode" ist die empfohlene Vorgehensweise zum Festlegen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="da44c-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="da44c-109">Er konfiguriert den Filter zum Schreiben einer ASF-Datei auf Grundlage des angegebenen Anwendungs definierten Profils.</span><span class="sxs-lookup"><span data-stu-id="da44c-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="da44c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="da44c-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="da44c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="da44c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da44c-112">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da44c-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da44c-113">Zeiger auf die [**iwmprofile**](iwmprofile.md) -Schnittstelle im Anwendungs definierten Profil.</span><span class="sxs-lookup"><span data-stu-id="da44c-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da44c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da44c-114">Return value</span></span>

<span data-ttu-id="da44c-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="da44c-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="da44c-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da44c-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="da44c-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="da44c-117">Return code</span></span>                                                                                         | <span data-ttu-id="da44c-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da44c-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="da44c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="da44c-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="da44c-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da44c-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="da44c-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="da44c-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="da44c-122">Der **iwmprofile** -Schnittstellen Zeiger ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="da44c-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="da44c-123"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="da44c-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="da44c-124">Das Diagramm wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="da44c-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="da44c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da44c-125">Remarks</span></span>

<span data-ttu-id="da44c-126">Bei erfolgreicher Ausführung bewirkt diese Methode, dass **ein \_ \_ geändertes Ereignis des EC-Diagramms** an die Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="da44c-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="da44c-127">Verwenden Sie diese Methode, um den Writer mit einem benutzerdefinierten Windows Media 9-Serien Profil zu konfigurieren, das Sie mithilfe der Methoden des SDK für den Windows Media-Format erstellt (oder aus einer vorhandenen PRX-Datei geladen haben).</span><span class="sxs-lookup"><span data-stu-id="da44c-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="da44c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da44c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="da44c-129">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da44c-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

