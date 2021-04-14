---
description: Beschreibt mögliche Computerarchitekturen.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Bilddatei-Computer Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526984"
---
# <a name="image-file-machine-constants"></a><span data-ttu-id="d5d36-103">Bilddatei-Computer Konstanten</span><span class="sxs-lookup"><span data-stu-id="d5d36-103">Image File Machine Constants</span></span>

<span data-ttu-id="d5d36-104">Beschreibt mögliche Computerarchitekturen.</span><span class="sxs-lookup"><span data-stu-id="d5d36-104">Describes possible machine architectures.</span></span> <span data-ttu-id="d5d36-105">Wird in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) und [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5d36-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="d5d36-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**Bild \_ Datei \_ Computer \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d5d36-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-107">0</span><span class="sxs-lookup"><span data-stu-id="d5d36-107">0</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-108">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="d5d36-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_Bilddatei \_ - \_ \_ Zielhost**</span><span class="sxs-lookup"><span data-stu-id="d5d36-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="d5d36-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-111">Interagiert mit dem Host und nicht mit einem WOW64-Gast</span><span class="sxs-lookup"><span data-stu-id="d5d36-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="d5d36-112">Diese Konstante ist ab Windows 10, Version 1607 und Windows Server 2016 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5d36-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**Bild \_ Datei \_ Computer \_ i386**</span><span class="sxs-lookup"><span data-stu-id="d5d36-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="d5d36-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="d5d36-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**Image \_ Datei \_ Computer \_ R3000**</span><span class="sxs-lookup"><span data-stu-id="d5d36-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="d5d36-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-118">MIPS Little--in, 0x160 Big---in</span><span class="sxs-lookup"><span data-stu-id="d5d36-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**Image \_ Datei \_ Computer \_ R4000**</span><span class="sxs-lookup"><span data-stu-id="d5d36-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="d5d36-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-121">MIPS Little-d</span><span class="sxs-lookup"><span data-stu-id="d5d36-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**Image \_ Datei \_ Computer \_ R10000**</span><span class="sxs-lookup"><span data-stu-id="d5d36-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="d5d36-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-124">MIPS Little-d</span><span class="sxs-lookup"><span data-stu-id="d5d36-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**Image \_ Datei \_ Computer \_ WCEMIPSV2**</span><span class="sxs-lookup"><span data-stu-id="d5d36-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="d5d36-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-127">MIPS Little-in WCE v2</span><span class="sxs-lookup"><span data-stu-id="d5d36-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**Bild \_ Datei \_ Computer \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="d5d36-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="d5d36-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-130">Alpha \_ AXP</span><span class="sxs-lookup"><span data-stu-id="d5d36-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**Image \_ Datei \_ Computer \_ SH3**</span><span class="sxs-lookup"><span data-stu-id="d5d36-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="d5d36-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-133">SH3 Little-d</span><span class="sxs-lookup"><span data-stu-id="d5d36-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**Image \_ Datei \_ Computer \_ SH3DSP**</span><span class="sxs-lookup"><span data-stu-id="d5d36-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="d5d36-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="d5d36-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**Image \_ Datei \_ Computer \_ SH3E**</span><span class="sxs-lookup"><span data-stu-id="d5d36-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="d5d36-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-139">SH3E Little-d</span><span class="sxs-lookup"><span data-stu-id="d5d36-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**Image \_ Datei \_ Computer \_ SH4**</span><span class="sxs-lookup"><span data-stu-id="d5d36-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="d5d36-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-142">SH4 Little-d</span><span class="sxs-lookup"><span data-stu-id="d5d36-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**Image \_ Datei \_ Computer \_ SH5**</span><span class="sxs-lookup"><span data-stu-id="d5d36-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="d5d36-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-145">SH5</span><span class="sxs-lookup"><span data-stu-id="d5d36-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**Bild \_ Datei \_ Computer- \_ Arm**</span><span class="sxs-lookup"><span data-stu-id="d5d36-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="d5d36-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-148">Arm-Little-Endian</span><span class="sxs-lookup"><span data-stu-id="d5d36-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**Ziehpunkt für Bild \_ Datei \_ Computer \_**</span><span class="sxs-lookup"><span data-stu-id="d5d36-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="d5d36-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-151">Arm Thumb/Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="d5d36-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**Bilddatei- \_ \_ Computer \_ armnt**</span><span class="sxs-lookup"><span data-stu-id="d5d36-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="d5d36-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-154">Arm-Thumb-2-Little-Endian</span><span class="sxs-lookup"><span data-stu-id="d5d36-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="d5d36-155">Diese Konstante ist ab Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5d36-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**Image \_ Datei \_ Computer \_ AM33**</span><span class="sxs-lookup"><span data-stu-id="d5d36-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="d5d36-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="d5d36-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**Bild \_ Datei \_ Computer \_ powerpc**</span><span class="sxs-lookup"><span data-stu-id="d5d36-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-160">0x01f 0</span><span class="sxs-lookup"><span data-stu-id="d5d36-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-161">IBM PowerPC-Little-Endian</span><span class="sxs-lookup"><span data-stu-id="d5d36-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**Image \_ Datei \_ Computer- \_ powerpcfp**</span><span class="sxs-lookup"><span data-stu-id="d5d36-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-163">0x01f 1</span><span class="sxs-lookup"><span data-stu-id="d5d36-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-164">Powerpcfp</span><span class="sxs-lookup"><span data-stu-id="d5d36-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Bild \_ Datei \_ Computer \_ ia64**</span><span class="sxs-lookup"><span data-stu-id="d5d36-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="d5d36-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="d5d36-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**Image \_ Datei \_ Computer \_ MIPS16**</span><span class="sxs-lookup"><span data-stu-id="d5d36-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="d5d36-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="d5d36-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**Image \_ Datei \_ Computer \_ ALPHA64**</span><span class="sxs-lookup"><span data-stu-id="d5d36-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="d5d36-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="d5d36-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**Bild \_ Datei \_ Computer \_ mipsfpu**</span><span class="sxs-lookup"><span data-stu-id="d5d36-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="d5d36-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="d5d36-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**Image \_ Datei \_ Computer \_ MIPSFPU16**</span><span class="sxs-lookup"><span data-stu-id="d5d36-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="d5d36-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="d5d36-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**Image \_ Datei \_ Computer \_ AXP64**</span><span class="sxs-lookup"><span data-stu-id="d5d36-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="d5d36-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="d5d36-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**der Abbild \_ Datei- \_ Computer- \_ zentrale**</span><span class="sxs-lookup"><span data-stu-id="d5d36-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="d5d36-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-185">Infineon</span><span class="sxs-lookup"><span data-stu-id="d5d36-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**Image \_ Datei \_ Computer \_ CEF**</span><span class="sxs-lookup"><span data-stu-id="d5d36-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-187">0x0cef</span><span class="sxs-lookup"><span data-stu-id="d5d36-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-188">CEF</span><span class="sxs-lookup"><span data-stu-id="d5d36-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**Image \_ Datei \_ Computer \_ EBC**</span><span class="sxs-lookup"><span data-stu-id="d5d36-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-190">0x0ebc</span><span class="sxs-lookup"><span data-stu-id="d5d36-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-191">EFI-Bytecode</span><span class="sxs-lookup"><span data-stu-id="d5d36-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Bild \_ Datei \_ Computer \_ amd64**</span><span class="sxs-lookup"><span data-stu-id="d5d36-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="d5d36-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-194">Amd64 (K8)</span><span class="sxs-lookup"><span data-stu-id="d5d36-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**Image \_ Datei \_ Computer \_ M32R**</span><span class="sxs-lookup"><span data-stu-id="d5d36-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="d5d36-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-197">M32R Little-d</span><span class="sxs-lookup"><span data-stu-id="d5d36-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**Image \_ Datei \_ Computer \_ ARM64**</span><span class="sxs-lookup"><span data-stu-id="d5d36-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-199">0xaa64</span><span class="sxs-lookup"><span data-stu-id="d5d36-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-200">ARM64 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="d5d36-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="d5d36-201">Diese Konstante ist ab Windows 8.1 und Windows Server 2012 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5d36-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5d36-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**Bild \_ Datei \_ Computer- \_ CEE**</span><span class="sxs-lookup"><span data-stu-id="d5d36-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d36-203">0xc0ee</span><span class="sxs-lookup"><span data-stu-id="d5d36-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="d5d36-204">CEE</span><span class="sxs-lookup"><span data-stu-id="d5d36-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d36-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5d36-205">Requirements</span></span>



| <span data-ttu-id="d5d36-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5d36-206">Requirement</span></span> | <span data-ttu-id="d5d36-207">Wert</span><span class="sxs-lookup"><span data-stu-id="d5d36-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d36-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5d36-208">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d36-209">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5d36-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5d36-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5d36-210">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d36-211">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5d36-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5d36-212">Header</span><span class="sxs-lookup"><span data-stu-id="d5d36-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5d36-213"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d36-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




