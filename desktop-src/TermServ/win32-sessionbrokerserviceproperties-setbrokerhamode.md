---
title: Setbrokerhamode-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Migriert Daten aus einer lokalen wid-Datenbank in die neue SQL Server-basierte Datenbank. Außerdem wird der Broker Server für die Verwendung des zentralen SQL Server konfiguriert.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Setbrokerhamode-Methode Remotedesktopdienste
- Setbrokerhamode-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, setbrokerhamode-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103671"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="9ffe7-107">Setbrokerhamode-Methode der Win32- \_ Klasse "sessionbrokerserviceproperties"</span><span class="sxs-lookup"><span data-stu-id="9ffe7-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="9ffe7-108">Migriert Daten aus einer lokalen wid-Datenbank in die neue SQL Server-basierte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="9ffe7-109">Außerdem wird der Broker Server für die Verwendung des zentralen SQL Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffe7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ffe7-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="9ffe7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ffe7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ffe7-112">"Verbindungs Dienst" für " *recentraldbrdcms* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="9ffe7-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffe7-113">Verbindungs Zeichenfolge zur zentralen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="9ffe7-114">*secondaryverbindungs-"stringrecentraldbrdcms* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="9ffe7-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffe7-115">Sekundäre Verbindungs Zeichenfolge zur zentralen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="9ffe7-116">**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="9ffe7-117">*brokerdnsrrname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ffe7-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffe7-118">DNS-Broker Name.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="9ffe7-119">*activebrokername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ffe7-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffe7-120">Name des aktiven Brokers.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-120">Active broker name.</span></span>

<span data-ttu-id="9ffe7-121">**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ffe7-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ffe7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ffe7-122">Requirements</span></span>



| <span data-ttu-id="9ffe7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ffe7-123">Requirement</span></span> | <span data-ttu-id="9ffe7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9ffe7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffe7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ffe7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffe7-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ffe7-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ffe7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ffe7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffe7-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ffe7-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="9ffe7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ffe7-129">Namespace</span></span><br/>                | <span data-ttu-id="9ffe7-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9ffe7-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9ffe7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9ffe7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ffe7-132"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9ffe7-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ffe7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9ffe7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ffe7-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ffe7-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffe7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ffe7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffe7-136">**Win32 \_ sessionbrokerserviceproperties**</span><span class="sxs-lookup"><span data-stu-id="9ffe7-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





