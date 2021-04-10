---
description: Aktiviert oder deaktiviert das Lesen und Schreiben von Datenträger Sektoren.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Funktion "sveenablerawaccessw"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860903"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="1885f-103">Funktion "sveenablerawaccessw"</span><span class="sxs-lookup"><span data-stu-id="1885f-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="1885f-104">Aktiviert oder deaktiviert das Lesen und Schreiben von Datenträger Sektoren.</span><span class="sxs-lookup"><span data-stu-id="1885f-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1885f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1885f-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="1885f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1885f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1885f-107">*Volumename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1885f-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1885f-108">Ein eindeutiger Bezeichner für das Datenträger Volume.</span><span class="sxs-lookup"><span data-stu-id="1885f-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="1885f-109">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1885f-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1885f-110">Wenn der Wert **true** ist, wird der Zugriff auf das rohvolume ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="1885f-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="1885f-111">Wenn der Wert **false** ist, ist kein Zugriff auf das rohvolume zulässig.</span><span class="sxs-lookup"><span data-stu-id="1885f-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="1885f-112">Wenn der rohzugriff bereits aktiviert wurde, dieser Wert jedoch **false** ist, wird das Volume erneut bereitgestellt und erneut überprüft.</span><span class="sxs-lookup"><span data-stu-id="1885f-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1885f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1885f-113">Return value</span></span>

<span data-ttu-id="1885f-114">Diese Funktion gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1885f-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1885f-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1885f-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="1885f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1885f-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1885f-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1885f-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="1885f-118">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1885f-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1885f-119"><dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1885f-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="1885f-120">Aktiviert ist **false** , und das Volume war nicht bereits im RAW-Zugriffsmodus.</span><span class="sxs-lookup"><span data-stu-id="1885f-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="1885f-121"><dt>**E \_ AccessDenied**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="1885f-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="1885f-122">Das Volume kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="1885f-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="1885f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1885f-123">Requirements</span></span>



| <span data-ttu-id="1885f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1885f-124">Requirement</span></span> | <span data-ttu-id="1885f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1885f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1885f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1885f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1885f-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1885f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1885f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1885f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1885f-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1885f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1885f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1885f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1885f-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1885f-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




