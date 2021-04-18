---
description: Initialisiert den optionalen Komponenten-Manager.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Ocinitialize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371022"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="43e62-103">Ocinitialize-Funktion</span><span class="sxs-lookup"><span data-stu-id="43e62-103">OcInitialize function</span></span>

<span data-ttu-id="43e62-104">Initialisiert den optionalen Komponenten-Manager.</span><span class="sxs-lookup"><span data-stu-id="43e62-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43e62-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="43e62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43e62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e62-107">*Rückrufe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43e62-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e62-108">Ein Zeiger auf eine [**OCM \_ - \_ Clientrückrufe**](ocm-client-callbacks.md) -Struktur, die die Rückruf Funktionen angibt, die vom OC-Manager zum Ausführen verschiedener Aufgaben verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43e62-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="43e62-109">*Masterocinfname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43e62-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e62-110">Der Pfad der "OC. inf"-Master Datei.</span><span class="sxs-lookup"><span data-stu-id="43e62-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="43e62-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="43e62-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e62-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="43e62-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="43e62-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**Ocinit \_ Forcenewinf** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="43e62-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="43e62-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**Ocinit \_ Killsubcomps** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="43e62-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="43e62-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**Ocinit \_ Runquiet** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="43e62-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="43e62-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**Ocinit \_ Languageaware** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="43e62-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="43e62-117">*ShowError* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43e62-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43e62-118">Wenn die Funktion fehlschlägt, gibt dieser Parameter an, ob eine Fehlermeldung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="43e62-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="43e62-119">*Protokollieren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43e62-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e62-120">Ein Handle für das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="43e62-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e62-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43e62-121">Return value</span></span>

<span data-ttu-id="43e62-122">Die-Funktion gibt den OC Manager-Kontextwert zurück.</span><span class="sxs-lookup"><span data-stu-id="43e62-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43e62-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43e62-123">Remarks</span></span>

<span data-ttu-id="43e62-124">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="43e62-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e62-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43e62-125">Requirements</span></span>



| <span data-ttu-id="43e62-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43e62-126">Requirement</span></span> | <span data-ttu-id="43e62-127">Wert</span><span class="sxs-lookup"><span data-stu-id="43e62-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43e62-128">DLL</span><span class="sxs-lookup"><span data-stu-id="43e62-128">DLL</span></span><br/> | <dl> <span data-ttu-id="43e62-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43e62-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e62-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43e62-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e62-131">**OCM- \_ Client \_ Rückrufe**</span><span class="sxs-lookup"><span data-stu-id="43e62-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="43e62-132">**Okbeenden**</span><span class="sxs-lookup"><span data-stu-id="43e62-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 
