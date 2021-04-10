---
title: INapComponentConfig2 invokeuiformachine-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) nach Bedarf implementiert, um die Remote Konfiguration direkt auf dem angegebenen Computer zu verwalten. Mit dieser Methode wird eine Benutzeroberfläche der Konfigurations Verwaltung gestartet.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Invokeuiformachine-Methode NAP
- Invokeuiformachine-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2 Interface NAP, invokeuiformachine-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103539"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="b6beb-107">INapComponentConfig2:: invokeuiformachine-Methode</span><span class="sxs-lookup"><span data-stu-id="b6beb-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="b6beb-108">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b6beb-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b6beb-109">Die **invokeuiformachine** -Methode wird von System Integritätsprüfungen (SHVs) nach Bedarf implementiert, um die Remote Konfiguration direkt auf dem angegebenen Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b6beb-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="b6beb-110">Mit dieser Methode wird eine Benutzeroberfläche der Konfigurations Verwaltung gestartet.</span><span class="sxs-lookup"><span data-stu-id="b6beb-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6beb-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6beb-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="b6beb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6beb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6beb-113">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6beb-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6beb-114">Ein Handle für das übergeordnete Fenster oder Besitzer Fenster.</span><span class="sxs-lookup"><span data-stu-id="b6beb-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="b6beb-115">Ein gültiges Fenster Handle muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b6beb-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="b6beb-116">*MachineName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6beb-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6beb-117">Ein Zeiger auf eine [**zählzeichenfolge**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , die den Computernamen des NAP-Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="b6beb-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6beb-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6beb-118">Return value</span></span>

<span data-ttu-id="b6beb-119">Gibt \_ bei Erfolg S OK oder einen der standardmäßigen Windows-Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="b6beb-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6beb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6beb-120">Requirements</span></span>



| <span data-ttu-id="b6beb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6beb-121">Requirement</span></span> | <span data-ttu-id="b6beb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b6beb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6beb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6beb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b6beb-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b6beb-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b6beb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6beb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b6beb-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6beb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b6beb-127">Header</span><span class="sxs-lookup"><span data-stu-id="b6beb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6beb-128"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6beb-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6beb-129">IDL</span><span class="sxs-lookup"><span data-stu-id="b6beb-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6beb-130"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6beb-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6beb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6beb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6beb-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="b6beb-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





