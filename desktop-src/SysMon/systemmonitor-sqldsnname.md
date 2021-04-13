---
title: Systemmonitor sqldsnname (Eigenschaft)
description: Ruft den ODBC-Datenquellen Namen (DSN) ab oder legt ihn fest.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Sqldsnname-Eigenschaft (Sysmon)
- Sqldsnname-Eigenschaft (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, sqldsnname (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391496"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="55b11-106">Systemmonitor:: sqldsnname (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="55b11-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="55b11-107">Ruft den ODBC-Datenquellen Namen (DSN) ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="55b11-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="55b11-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="55b11-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="55b11-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="55b11-109">Property value</span></span>

<span data-ttu-id="55b11-110">Der ODBC-Datenquellen Name, der auf eine Datenbank verweist, die die richtigen Perfmon-Tabellen enthält.</span><span class="sxs-lookup"><span data-stu-id="55b11-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="55b11-111">Das Format ist SQL: DSN.</span><span class="sxs-lookup"><span data-stu-id="55b11-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b11-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55b11-112">Remarks</span></span>

<span data-ttu-id="55b11-113">Verwenden Sie das MMC-Snap-in "Perfmon. msc", um die SQL-Protokolldatei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="55b11-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="55b11-114">Die Counter-Protokolle befinden sich unter **Leistungsprotokolle und-Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="55b11-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="55b11-115">Um ein SQL-Protokoll anzugeben, klicken Sie mit der rechten Maustaste auf die von Ihnen erstellte Protokolldatei, und wählen Sie im Menü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="55b11-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="55b11-116">Wählen Sie auf der Eigenschaften Seite **Protokolldateien** im Dropdown-Listenfeld **Protokoll Dateityp** die Option **SQL-Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="55b11-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="55b11-117">**Vor Windows Vista:** Sie können diese Eigenschaft nicht ändern, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonsqllog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="55b11-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="55b11-118">Sie müssen zuerst den Namen angeben und dann **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonsqllog** festlegen.</span><span class="sxs-lookup"><span data-stu-id="55b11-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b11-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55b11-119">Requirements</span></span>



| <span data-ttu-id="55b11-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55b11-120">Requirement</span></span> | <span data-ttu-id="55b11-121">Wert</span><span class="sxs-lookup"><span data-stu-id="55b11-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55b11-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55b11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55b11-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55b11-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="55b11-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55b11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55b11-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55b11-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55b11-126">DLL</span><span class="sxs-lookup"><span data-stu-id="55b11-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b11-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="55b11-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b11-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55b11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b11-129">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="55b11-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="55b11-130">**Systemmonitor. sqllogsetname**</span><span class="sxs-lookup"><span data-stu-id="55b11-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





