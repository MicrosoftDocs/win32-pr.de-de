---
title: Win32_TSGatewayServer-Klasse
description: Wird für Server spezifische Vorgänge Remotedesktop Gateway (RD-Gateway) verwendet.
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer-Klasse Remotedesktopdienste
- Win32_TSGatewayServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476383"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="c0802-105">Win32-Klasse "- \_ Gatewayserver"</span><span class="sxs-lookup"><span data-stu-id="c0802-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="c0802-106">Wird für Server spezifische Vorgänge Remotedesktop Gateway (RD-Gateway) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0802-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0802-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0802-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="c0802-108">Member</span><span class="sxs-lookup"><span data-stu-id="c0802-108">Members</span></span>

<span data-ttu-id="c0802-109">Die Win32-Klasse " **\_ zgatewayserver** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0802-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="c0802-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="c0802-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0802-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c0802-111">Methods</span></span>

<span data-ttu-id="c0802-112">Die Win32-Klasse " **\_ zgatewayserver** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c0802-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="c0802-113">Methode</span><span class="sxs-lookup"><span data-stu-id="c0802-113">Method</span></span>                                                                                   | <span data-ttu-id="c0802-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0802-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0802-115">**"Kreateselfsignedcertificate"**</span><span class="sxs-lookup"><span data-stu-id="c0802-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="c0802-116">Erstellt ein selbst signiertes Zertifikat mit einem angegebenen Antragsteller Namen und gibt den Zertifikat Hash als einen out-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="c0802-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="c0802-117">**Exportieren**</span><span class="sxs-lookup"><span data-stu-id="c0802-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="c0802-118">Gibt die RD-Gateway Server-Konfiguration als XML-Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="c0802-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="c0802-119">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="c0802-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="c0802-120">Importiert eine angegebene Konfiguration auf den RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="c0802-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="c0802-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0802-121">Remarks</span></span>

<span data-ttu-id="c0802-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c0802-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c0802-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c0802-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c0802-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0802-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c0802-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c0802-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0802-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0802-126">Requirements</span></span>



| <span data-ttu-id="c0802-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0802-127">Requirement</span></span> | <span data-ttu-id="c0802-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c0802-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0802-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0802-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0802-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0802-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c0802-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0802-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0802-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0802-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c0802-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0802-133">Namespace</span></span><br/>                | <span data-ttu-id="c0802-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c0802-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c0802-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c0802-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0802-136"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="c0802-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0802-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c0802-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0802-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0802-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

