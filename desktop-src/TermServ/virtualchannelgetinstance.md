---
title: Virtualchannelgetinstance-Einstiegspunkt
description: Wird aufgerufen, damit das Plug-in eine Instanz der iwtsplugin-Schnittstelle für alle Plug-Ins erstellt, die von der dll implementiert werden.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Virtualchannelgetinstance-Einstiegspunkt Remotedesktopdienste
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391718"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="148ec-104">Virtualchannelgetinstance-Einstiegspunkt</span><span class="sxs-lookup"><span data-stu-id="148ec-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="148ec-105">Wird aufgerufen, damit das Plug-in eine Instanz der [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle für alle Plug-Ins erstellt, die von der dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="148ec-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="148ec-106">Diese Funktion wird vom Plug-in implementiert und muss nach Namen exportiert werden, damit eine Anwendung die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden kann, um dynamisch mit der Funktion zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="148ec-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="148ec-107">Der Prototyp für diese Funktion ist in keiner öffentlichen Header Datei enthalten, daher müssen Sie Sie genau wie gezeigt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="148ec-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="148ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="148ec-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="148ec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="148ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="148ec-110">*refi-ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="148ec-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="148ec-111">Gibt den Typ der zurück zugebende Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="148ec-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="148ec-112">Dabei muss es sich um **IID \_ iwtsplugin** handeln.</span><span class="sxs-lookup"><span data-stu-id="148ec-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="148ec-113">*pnumubjs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="148ec-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="148ec-114">Die Adresse einer **ulong** -Variablen, die die Anzahl der abgerufenen Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="148ec-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="148ec-115">*ppobjarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="148ec-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="148ec-116">Die Adresse eines Array von Zeigern, das die Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="148ec-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="148ec-117">Wenn dieser Parameter **null** ist, muss die Implementierung die Anzahl der Plug-ins, die von der dll implementiert werden, im *pnumubjs* -Parameter platzieren.</span><span class="sxs-lookup"><span data-stu-id="148ec-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="148ec-118">Dies ermöglicht es dem Aufrufer, das richtige Größen Array für *ppobjarray* zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="148ec-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="148ec-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="148ec-119">Return value</span></span>

<span data-ttu-id="148ec-120">Wenn dieser Einstiegspunkt erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="148ec-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="148ec-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="148ec-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="148ec-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="148ec-122">Requirements</span></span>



| <span data-ttu-id="148ec-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="148ec-123">Requirement</span></span> | <span data-ttu-id="148ec-124">Wert</span><span class="sxs-lookup"><span data-stu-id="148ec-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="148ec-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="148ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="148ec-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="148ec-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="148ec-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="148ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="148ec-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="148ec-128">Windows Server 2008</span></span><br/> |



 

