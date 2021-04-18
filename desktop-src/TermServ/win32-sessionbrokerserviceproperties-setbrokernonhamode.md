---
title: Setbrokernonhamode-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Migriert Daten aus Central SQL Server in eine lokale Datenbank. Außerdem wird der Broker Server für die Verwendung der lokalen Datenbank konfiguriert.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Setbrokernonhamode-Methode Remotedesktopdienste
- Setbrokernonhamode-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, setbrokernonhamode-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345292"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="b279f-107">Setbrokernonhamode-Methode der Win32 \_ sessionbrokerserviceproperties-Klasse</span><span class="sxs-lookup"><span data-stu-id="b279f-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="b279f-108">Migriert Daten aus Central SQL Server in eine lokale Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b279f-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="b279f-109">Außerdem wird der Broker Server für die Verwendung der lokalen Datenbank konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b279f-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b279f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b279f-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="b279f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b279f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b279f-112">"Verbindungs Dienst" für " *recentraldbrdcms* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="b279f-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b279f-113">Verbindungs Zeichenfolge zur zentralen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b279f-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b279f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b279f-114">Requirements</span></span>



| <span data-ttu-id="b279f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b279f-115">Requirement</span></span> | <span data-ttu-id="b279f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b279f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b279f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b279f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b279f-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b279f-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b279f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b279f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b279f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b279f-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="b279f-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b279f-121">Namespace</span></span><br/>                | <span data-ttu-id="b279f-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b279f-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b279f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b279f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b279f-124"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b279f-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b279f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b279f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b279f-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b279f-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b279f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b279f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b279f-128">**Win32 \_ sessionbrokerserviceproperties**</span><span class="sxs-lookup"><span data-stu-id="b279f-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





