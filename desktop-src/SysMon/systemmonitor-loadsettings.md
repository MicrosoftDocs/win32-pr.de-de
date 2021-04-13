---
title: Systemmonitor. LoadSettings-Methode
description: Fügt dem System Monitor die Indikatoren in der HTML-Vorlagen Datei hinzu.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- LoadSettings-Methode (Sysmon)
- LoadSettings-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", LoadSettings-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391937"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="8219e-106">Systemmonitor. LoadSettings-Methode</span><span class="sxs-lookup"><span data-stu-id="8219e-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="8219e-107">Fügt dem System Monitor die Indikatoren in der HTML-Vorlagen Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="8219e-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8219e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8219e-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="8219e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8219e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8219e-110">*Settingsfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8219e-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8219e-111">HTML-Zeichenfolge, die die Zähler angibt, die dem System Monitor hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8219e-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8219e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8219e-112">Return value</span></span>

<span data-ttu-id="8219e-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8219e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8219e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8219e-114">Remarks</span></span>

<span data-ttu-id="8219e-115">Um die aktuellen Leistungsindikatoren im System Monitor in einer HTML-Datei zu speichern, wenden Sie die Methode [**Systemmonitor. SaveAs**](systemmonitor-saveas.md) an.</span><span class="sxs-lookup"><span data-stu-id="8219e-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8219e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8219e-116">Requirements</span></span>



| <span data-ttu-id="8219e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8219e-117">Requirement</span></span> | <span data-ttu-id="8219e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8219e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8219e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8219e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8219e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8219e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8219e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8219e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8219e-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8219e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8219e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8219e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8219e-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8219e-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8219e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8219e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8219e-126">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="8219e-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





