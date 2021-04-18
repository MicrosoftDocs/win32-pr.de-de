---
title: Delta Type bdbconnectionstring-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Löscht DB-Verbindungs Zeichenfolgen (primär oder sekundär) aus der Registrierung.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Delta Type bdbconnectionstring-Methode Remotedesktopdienste
- Delta Type bdbconnectionstring-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, Delta Timeout-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340585"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="a877e-106">Delta Type bdbconnectionstring-Methode der Win32 \_ sessionbrokerserviceproperties-Klasse</span><span class="sxs-lookup"><span data-stu-id="a877e-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="a877e-107">Löscht DB-Verbindungs Zeichenfolgen (primär oder sekundär) aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a877e-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="a877e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a877e-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="a877e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a877e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a877e-110">*Issecondaryconfig-Zeichenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a877e-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a877e-111">**True** gibt an, dass die sekundäre Verbindungs Zeichenfolge entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a877e-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="a877e-112">**False** gibt an, dass die primäre Verbindungs Zeichenfolge entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a877e-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a877e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a877e-113">Requirements</span></span>



| <span data-ttu-id="a877e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a877e-114">Requirement</span></span> | <span data-ttu-id="a877e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a877e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a877e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a877e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a877e-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a877e-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a877e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a877e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a877e-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a877e-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="a877e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a877e-120">Namespace</span></span><br/>                | <span data-ttu-id="a877e-121">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a877e-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="a877e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="a877e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a877e-123"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="a877e-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a877e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a877e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a877e-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a877e-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a877e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a877e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a877e-127">**Win32 \_ sessionbrokerserviceproperties**</span><span class="sxs-lookup"><span data-stu-id="a877e-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





