---
title: Isdbreachable-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Überprüft, ob die Datenbank erreichbar ist.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Isdbreachable-Methode Remotedesktopdienste
- Isdbreachable-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties Klasse Remotedesktopdienste, isdbreachable-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476689"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="94b69-106">Isdbreachable-Methode der Win32 \_ sessionbrokerserviceproperties-Klasse</span><span class="sxs-lookup"><span data-stu-id="94b69-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="94b69-107">Überprüft, ob die Datenbank erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="94b69-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b69-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b69-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="94b69-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="94b69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94b69-110">"Verbindung mit dem Daten *Bank Konto"* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94b69-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b69-111">Die Verbindungszeichenfolge für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="94b69-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="94b69-112">" *\nsecondarystringredb* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="94b69-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b69-113">Sekundäre Verbindungs Zeichenfolge zur zentralen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="94b69-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="94b69-114">**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94b69-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="94b69-115">*activebrokername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94b69-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b69-116">Name des aktiven Brokers.</span><span class="sxs-lookup"><span data-stu-id="94b69-116">Active broker name.</span></span>

<span data-ttu-id="94b69-117">**Windows Server 2012 R2 und Windows Server 2012:** Dieser Parameter ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94b69-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94b69-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94b69-118">Requirements</span></span>



| <span data-ttu-id="94b69-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94b69-119">Requirement</span></span> | <span data-ttu-id="94b69-120">Wert</span><span class="sxs-lookup"><span data-stu-id="94b69-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b69-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94b69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94b69-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="94b69-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="94b69-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94b69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94b69-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="94b69-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="94b69-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="94b69-125">Namespace</span></span><br/>                | <span data-ttu-id="94b69-126">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="94b69-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="94b69-127">MOF</span><span class="sxs-lookup"><span data-stu-id="94b69-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94b69-128"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="94b69-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="94b69-129">DLL</span><span class="sxs-lookup"><span data-stu-id="94b69-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b69-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b69-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b69-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94b69-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b69-132">**Win32 \_ sessionbrokerserviceproperties**</span><span class="sxs-lookup"><span data-stu-id="94b69-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





