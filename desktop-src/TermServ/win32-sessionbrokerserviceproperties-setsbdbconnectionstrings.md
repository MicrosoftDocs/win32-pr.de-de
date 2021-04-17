---
title: Die Methode "stionbdbconnectionstrings" der Win32_SessionBrokerServiceProperties-Klasse
description: Speichert DB-Verbindungs Zeichenfolgen (Primär und sekundär) in der Registrierung.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "" der Klasse "Win32_SessionBrokerServiceProperties"
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, Methode ' Methode ', ' Methode '
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476686"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="8f9e0-106">Die Methode "" der \_ Klasse "sessionbrokerserviceproperties" der Win32-Klasse</span><span class="sxs-lookup"><span data-stu-id="8f9e0-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="8f9e0-107">Speichert DB-Verbindungs Zeichenfolgen (Primär und sekundär) in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f9e0-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="8f9e0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f9e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9e0-110">"Verbindungs Dienst" für " *recentraldbrdcms* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8f9e0-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9e0-111">Die primäre Verbindungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="8f9e0-112">*secondaryverbindungs-"stringrecentraldbrdcms* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8f9e0-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9e0-113">Die sekundäre Verbindungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f9e0-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f9e0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f9e0-114">Requirements</span></span>



| <span data-ttu-id="8f9e0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f9e0-115">Requirement</span></span> | <span data-ttu-id="8f9e0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8f9e0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9e0-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f9e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9e0-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f9e0-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8f9e0-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f9e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9e0-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8f9e0-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="8f9e0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f9e0-121">Namespace</span></span><br/>                | <span data-ttu-id="8f9e0-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8f9e0-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="8f9e0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="8f9e0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f9e0-124"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="8f9e0-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f9e0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9e0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9e0-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9e0-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8f9e0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f9e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9e0-128">**Win32 \_ sessionbrokerserviceproperties**</span><span class="sxs-lookup"><span data-stu-id="8f9e0-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





