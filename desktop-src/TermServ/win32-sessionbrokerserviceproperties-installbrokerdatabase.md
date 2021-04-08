---
title: Installbrokerdatabase-Methode der Win32_SessionBrokerServiceProperties-Klasse
description: Installiert eine Remote Desktop-Verbindungs Broker-Datenbank auf einem zentralen SQL-Server.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Installbrokerdatabase-Methode Remotedesktopdienste
- Installbrokerdatabase-Methode Remotedesktopdienste, Win32_SessionBrokerServiceProperties-Klasse
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, installbrokerdatabase-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740200"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="9b024-106">Installbrokerdatabase-Methode der Win32- \_ Klasse "sessionbrokerserviceproperties"</span><span class="sxs-lookup"><span data-stu-id="9b024-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="9b024-107">Installiert eine Remote Desktop-Verbindungs Broker-Datenbank auf einem zentralen SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="9b024-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b024-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b024-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="9b024-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b024-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b024-110">*newdbfilepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b024-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b024-111">neuer Daten Bank Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="9b024-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="9b024-112">"Configuration Manager-Manager"  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b024-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b024-113">Verbindungs Zeichenfolge zum zentralen Daten Bank Master.</span><span class="sxs-lookup"><span data-stu-id="9b024-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="9b024-114">*centralrdcmsdbname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b024-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b024-115">Name der zentralen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9b024-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b024-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b024-116">Requirements</span></span>



| <span data-ttu-id="9b024-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b024-117">Requirement</span></span> | <span data-ttu-id="9b024-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9b024-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b024-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b024-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b024-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b024-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9b024-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b024-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b024-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b024-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="9b024-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b024-123">Namespace</span></span><br/>                | <span data-ttu-id="9b024-124">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9b024-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9b024-125">MOF</span><span class="sxs-lookup"><span data-stu-id="9b024-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b024-126"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9b024-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b024-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9b024-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b024-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b024-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b024-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b024-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b024-130">**Win32 \_ sessionbrokerserviceproperties**</span><span class="sxs-lookup"><span data-stu-id="9b024-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





