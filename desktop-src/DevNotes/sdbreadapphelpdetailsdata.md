---
Description: Ruft Daten aus der AppHelp-Detail Datenbank ab.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Sdbreadapphelpdetailsdata-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949812"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="f162a-103">Sdbreadapphelpdetailsdata-Funktion</span><span class="sxs-lookup"><span data-stu-id="f162a-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="f162a-104">Ruft Daten aus der AppHelp-Detail Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="f162a-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="f162a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f162a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="f162a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f162a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f162a-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f162a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f162a-108">Ein Handle für die AppHelp-Detail Datenbank, "AppHelp. sdb".</span><span class="sxs-lookup"><span data-stu-id="f162a-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="f162a-109">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f162a-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f162a-110">Eine [**AppHelp- \_ Daten**](apphelp-data.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f162a-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f162a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f162a-111">Return value</span></span>

<span data-ttu-id="f162a-112">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="f162a-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f162a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f162a-113">Requirements</span></span>



| <span data-ttu-id="f162a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f162a-114">Requirement</span></span> | <span data-ttu-id="f162a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f162a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f162a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f162a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f162a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f162a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f162a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f162a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f162a-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f162a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f162a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f162a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f162a-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f162a-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




