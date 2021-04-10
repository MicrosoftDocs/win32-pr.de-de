---
title: Systemmonitor sqllogsetname (Eigenschaft)
description: Ruft den anzeigen amen des Protokoll Satzes ab oder legt ihn fest.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Sqllogsetname-Eigenschaft (Sysmon)
- Sqllogsetname-Eigenschaft (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, sqllogsetname (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040063"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="2e9b0-106">Systemmonitor:: sqllogsetname (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2e9b0-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="2e9b0-107">Ruft den anzeigen amen des Protokoll Satzes ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9b0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e9b0-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="2e9b0-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2e9b0-109">Property value</span></span>

<span data-ttu-id="2e9b0-110">Anzeige Name des Protokoll Satzes, der einer einzelnen Protokolldatei entspricht, die Binär-oder Textdaten in der SQL-Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e9b0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e9b0-111">Remarks</span></span>

<span data-ttu-id="2e9b0-112">**Vor Windows Vista:** Sie können diese Eigenschaft nicht ändern, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf sysmonsqllog festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9b0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e9b0-113">Requirements</span></span>



| <span data-ttu-id="2e9b0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e9b0-114">Requirement</span></span> | <span data-ttu-id="2e9b0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2e9b0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9b0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e9b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9b0-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e9b0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2e9b0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e9b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9b0-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e9b0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e9b0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2e9b0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e9b0-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2e9b0-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9b0-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e9b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9b0-123">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="2e9b0-124">**Systemmonitor. sqldsnname**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





