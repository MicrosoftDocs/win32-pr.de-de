---
description: Ruft eine angegebene Anzahl zufälliger Bytes aus dem System Zufallszahlen-Generator ab.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Systemprng-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344058"
---
# <a name="systemprng-function"></a><span data-ttu-id="33140-103">Systemprng-Funktion</span><span class="sxs-lookup"><span data-stu-id="33140-103">SystemPrng function</span></span>

<span data-ttu-id="33140-104">\[**Systemprng** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="33140-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="33140-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="33140-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="33140-106">Verwenden Sie stattdessen [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span><span class="sxs-lookup"><span data-stu-id="33140-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="33140-107">Die **systemprng** -Funktion Ruft eine angegebene Anzahl zufälliger Bytes aus dem System Zufallszahlen-Generator ab.</span><span class="sxs-lookup"><span data-stu-id="33140-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="33140-108">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="33140-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="33140-109">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="33140-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="33140-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="33140-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="33140-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="33140-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33140-112">*pbrandomdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="33140-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33140-113">Ein Zeiger auf einen Puffer, der die abgerufenen Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="33140-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="33140-114">*cbrandomdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33140-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33140-115">Die Anzahl der abzurufenden Bytes.</span><span class="sxs-lookup"><span data-stu-id="33140-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33140-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33140-116">Return value</span></span>

<span data-ttu-id="33140-117">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="33140-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33140-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33140-118">Requirements</span></span>



| <span data-ttu-id="33140-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33140-119">Requirement</span></span> | <span data-ttu-id="33140-120">Wert</span><span class="sxs-lookup"><span data-stu-id="33140-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33140-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33140-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33140-122">Nur Windows Vista mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33140-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="33140-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33140-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33140-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33140-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="33140-125">DLL</span><span class="sxs-lookup"><span data-stu-id="33140-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33140-126"><dt>Ksecdd.sys unter Windows Server 2008 und Windows Vista mit SP1 </dt> <dt>Cng.sys unter Windows 7 und Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="33140-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 




