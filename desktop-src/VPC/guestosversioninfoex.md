---
title: Guestosversioninfoex-Struktur (vpccominterfaces. h)
description: Enthält Informationen zur Betriebssystemversion für das Gast Betriebssystem.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Guestosversioninfoex-Struktur virtueller PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104277"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="7df80-104">Guestosversioninfoex-Struktur</span><span class="sxs-lookup"><span data-stu-id="7df80-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="7df80-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7df80-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7df80-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7df80-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7df80-107">Enthält Informationen zur Betriebssystemversion für das Gast Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="7df80-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df80-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7df80-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="7df80-109">Member</span><span class="sxs-lookup"><span data-stu-id="7df80-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7df80-110">**dwOSVersionInfoSize**</span><span class="sxs-lookup"><span data-stu-id="7df80-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-111">Die Größe dieser Datenstruktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7df80-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="7df80-112">Legen Sie diesen Member auf fest `sizeof(GUESTOSVERSIONINFOEX)` .</span><span class="sxs-lookup"><span data-stu-id="7df80-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-113">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="7df80-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-114">Die Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="7df80-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-115">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="7df80-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-116">Die Nebenversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="7df80-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-117">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="7df80-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-118">Die Buildnummer.</span><span class="sxs-lookup"><span data-stu-id="7df80-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-119">**dwPlatformId**</span><span class="sxs-lookup"><span data-stu-id="7df80-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-120">Die Betriebssystem Plattform.</span><span class="sxs-lookup"><span data-stu-id="7df80-120">The operating system platform.</span></span> <span data-ttu-id="7df80-121">Dieser Member kann ein " **ver \_ Platform \_ Win32 \_ NT** " (2) sein.</span><span class="sxs-lookup"><span data-stu-id="7df80-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="7df80-122">**szCSDVersion**</span><span class="sxs-lookup"><span data-stu-id="7df80-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-123">Eine mit NULL endenden Zeichenfolge, z. b. "Service Pack 3", die das neueste Service Pack angibt, das auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7df80-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="7df80-124">Wenn kein Service Pack installiert wurde, ist die Zeichenfolge leer.</span><span class="sxs-lookup"><span data-stu-id="7df80-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-125">**wServicePackMajor**</span><span class="sxs-lookup"><span data-stu-id="7df80-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-126">Die Hauptversionsnummer des neuesten installierten Service Packs.</span><span class="sxs-lookup"><span data-stu-id="7df80-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-127">**wServicePackMinor**</span><span class="sxs-lookup"><span data-stu-id="7df80-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-128">Die neben Versionsnummer des neuesten installierten Service Packs.</span><span class="sxs-lookup"><span data-stu-id="7df80-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="7df80-129">**wSuiteMask**</span><span class="sxs-lookup"><span data-stu-id="7df80-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-130">Eine Bitmaske, die die im System verfügbaren Produkt Suites identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7df80-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="7df80-131">Dieser Member kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="7df80-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="7df80-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7df80-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="7df80-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7df80-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="7df80-134"><dt>**Ver \_ Suite \_ BackOffice**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="7df80-135">Microsoft BackOffice-Komponenten werden installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="7df80-136"><dt>**Ver \_ \_Blatt "Sammlung**</dt> " <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="7df80-137">Windows Server 2003, Web Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="7df80-138"><dt>**Ver \_ Suite \_ Compute \_ Server**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="7df80-139">Windows Server 2003, Compute Cluster Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="7df80-140"><dt>**Ver \_ Suite \_ Datacenter**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="7df80-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="7df80-142"><dt>**Ver \_ Suite \_ Enterprise**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="7df80-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="7df80-144">Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7df80-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="7df80-145"><dt>**Ver \_ Suite \_ embeddnt**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="7df80-146">Windows XP Embedded ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="7df80-147"><dt>**Ver \_ Suite \_ Personal**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="7df80-148">Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="7df80-149"><dt>**Ver \_ Suite \_ singleuserts**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="7df80-150">Remotedesktop wird unterstützt, es wird jedoch nur eine interaktive Sitzung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7df80-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="7df80-151">Dieser Wert wird festgelegt, es sei denn, das System wird im Anwendungsserver Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7df80-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="7df80-152"><dt>**Ver \_ Suite \_ SmallBusiness**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="7df80-153">Microsoft Small Business Server wurde auf dem System installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7df80-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="7df80-154">Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7df80-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="7df80-155"><dt>**Ver \_ \_SmallBusiness \_ restricted Suite**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="7df80-156">Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz in Kraft installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="7df80-157">Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7df80-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="7df80-158"><dt>**Ver \_ Suite \_ Storage \_ Server**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="7df80-159">Windows Storage Server 2003 R2 oder Windows Storage Server 2003ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="7df80-160"><dt>**Ver \_ Suite- \_ Terminal**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="7df80-161">Terminal Dienste sind installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-161">Terminal Services is installed.</span></span> <span data-ttu-id="7df80-162">Dieser Wert ist immer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7df80-162">This value is always set.</span></span><br/> <span data-ttu-id="7df80-163">Wenn das **ver \_ Suite- \_ Terminal** festgelegt ist, aber **ver \_ Suite \_ singleuserts** nicht festgelegt ist, wird das System im Anwendungsserver Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7df80-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="7df80-164"><dt>**Ver \_ Suite- \_ WH- \_ Server**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="7df80-165">Windows Home Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="7df80-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="7df80-166">**wProductType**</span><span class="sxs-lookup"><span data-stu-id="7df80-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-167">Weitere Informationen zum System.</span><span class="sxs-lookup"><span data-stu-id="7df80-167">Any additional information about the system.</span></span> <span data-ttu-id="7df80-168">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7df80-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="7df80-169">Wert</span><span class="sxs-lookup"><span data-stu-id="7df80-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="7df80-170">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7df80-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="7df80-171"><dt>**Ver \_ NT- \_ Domänen \_ Controller**</dt> <dt>0x0000002</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="7df80-172">Das System ist ein Domänen Controller, und das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7df80-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="7df80-173"><dt>**Ver \_ NT \_ Server**</dt> <dt>0x0000003</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="7df80-174">Das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7df80-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="7df80-175">Beachten Sie, dass ein Server, der auch ein Domänen Controller ist, als **ver- \_ NT- \_ Domänen \_ Controller**, nicht als **ver-NT- \_ \_ Server** gemeldet</span><span class="sxs-lookup"><span data-stu-id="7df80-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="7df80-176"><dt>**Ver \_ NT- \_ Arbeits**</dt> Station <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="7df80-177">Das Betriebssystem ist Windows 7, Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7df80-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="7df80-178">**wReserved**</span><span class="sxs-lookup"><span data-stu-id="7df80-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="7df80-179">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7df80-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7df80-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7df80-180">Requirements</span></span>



| <span data-ttu-id="7df80-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7df80-181">Requirement</span></span> | <span data-ttu-id="7df80-182">Wert</span><span class="sxs-lookup"><span data-stu-id="7df80-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df80-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7df80-183">Minimum supported client</span></span><br/> | <span data-ttu-id="7df80-184">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7df80-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7df80-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7df80-185">Minimum supported server</span></span><br/> | <span data-ttu-id="7df80-186">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7df80-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7df80-187">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7df80-187">End of client support</span></span><br/>    | <span data-ttu-id="7df80-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7df80-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7df80-189">Produkt</span><span class="sxs-lookup"><span data-stu-id="7df80-189">Product</span></span><br/>                  | <span data-ttu-id="7df80-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7df80-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7df80-191">Header</span><span class="sxs-lookup"><span data-stu-id="7df80-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df80-192"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7df80-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df80-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7df80-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df80-194">**Ivmguestos:: getosversioninfo**</span><span class="sxs-lookup"><span data-stu-id="7df80-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

