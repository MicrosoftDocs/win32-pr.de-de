---
title: Systemanbieter
description: Aktivieren Sie die Ereignisse des Systemablaufverfolgungsanbieters mit EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387799"
---
# <a name="system-providers"></a><span data-ttu-id="9a78d-103">Systemanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-103">System Providers</span></span>
 
<span data-ttu-id="9a78d-104">Ab Windows 10 SDK-Build 20348 können die Ereignisse des Systemablaufverfolgungsanbieters auf die gleiche Weise aktiviert werden wie andere ETW-Anbieter mit [EnableTraceEx2.](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)</span><span class="sxs-lookup"><span data-stu-id="9a78d-104">Beginning in Windows 10 SDK build 20348, the System Trace Provider's events can be enabled in the same way that other ETW providers are, with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).</span></span>  <span data-ttu-id="9a78d-105">Die verschiedenen Flags und [Gruppenmasken,](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) die dem Systemablaufverfolgungsanbieter zugeordnet sind, wurden neuen Ablaufverfolgungsanbietern zugeordnet, die als Systemanbieter bezeichnet werden, und übereinstimmenden Schlüsselwörtern.</span><span class="sxs-lookup"><span data-stu-id="9a78d-105">The different flags and [group masks](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associated with the System Trace Provider have been mapped to new trace providers, called System Providers, and matching keywords.</span></span>  
 
<span data-ttu-id="9a78d-106">Wie beim direkten Aktivieren des Systemablaufverfolgungsanbieters können die Systemanbieter nur durch eine Sitzung aktiviert werden, für die [der EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9a78d-106">Like enabling the System Trace Provider directly, the System Providers can only be enabled by a session with the [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) set.</span></span>

## <a name="system-provider-reference"></a><span data-ttu-id="9a78d-107">Systemanbieterreferenz</span><span class="sxs-lookup"><span data-stu-id="9a78d-107">System Provider reference</span></span>

* [<span data-ttu-id="9a78d-108">System-ALPC-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-108">System ALPC Provider</span></span>](#system-alpc-provider)
* [<span data-ttu-id="9a78d-109">Systemkonfigurationsanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-109">System Config Provider</span></span>](#system-config-provider)
* [<span data-ttu-id="9a78d-110">System-CPU-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-110">System CPU Provider</span></span>](#system-cpu-provider)
* [<span data-ttu-id="9a78d-111">System Hypervisor Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-111">System Hypervisor Provider</span></span>](#system-hypervisor-provider)
* [<span data-ttu-id="9a78d-112">Systemunterbrechungsanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-112">System Interrupt Provider</span></span>](#system-interrupt-provider)
* [<span data-ttu-id="9a78d-113">System-E/A-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-113">System IO Provider</span></span>](#system-io-provider)
* [<span data-ttu-id="9a78d-114">System-E/A-Filteranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-114">System IO Filter Provider</span></span>](#system-io-filter-provider)
* [<span data-ttu-id="9a78d-115">Systemsperranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-115">System Lock Provider</span></span>](#system-lock-provider)
* [<span data-ttu-id="9a78d-116">Systemspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-116">System Memory Provider</span></span>](#system-memory-provider)
* [<span data-ttu-id="9a78d-117">Systemobjektanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-117">System Object Provider</span></span>](#system-object-provider)
* [<span data-ttu-id="9a78d-118">System Power Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-118">System Power Provider</span></span>](#system-power-provider)
* [<span data-ttu-id="9a78d-119">Systemprozessanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-119">System Process Provider</span></span>](#system-process-provider)
* [<span data-ttu-id="9a78d-120">Systemprofilanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-120">System Profile Provider</span></span>](#system-profile-provider)
* [<span data-ttu-id="9a78d-121">Systemregistrierungsanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-121">System Registry Provider</span></span>](#system-registry-provider)
* [<span data-ttu-id="9a78d-122">Systemplaneranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-122">System Scheduler Provider</span></span>](#system-scheduler-provider)
* [<span data-ttu-id="9a78d-123">System Syscall Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-123">System Syscall Provider</span></span>](#system-syscall-provider)
* [<span data-ttu-id="9a78d-124">System Timer Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-124">System Timer Provider</span></span>](#system-timer-provider)
 
### <a name="system-alpc-provider"></a><span data-ttu-id="9a78d-125">System-ALPC-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-125">System ALPC Provider</span></span>

<span data-ttu-id="9a78d-126">Stellt Ereignisse im Zusammenhang mit dem ALPC-System bereit.</span><span class="sxs-lookup"><span data-stu-id="9a78d-126">Provides events related to the ALPC system.</span></span>

<span data-ttu-id="9a78d-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span><span class="sxs-lookup"><span data-stu-id="9a78d-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span></span>

| <span data-ttu-id="9a78d-128">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-128">Keyword</span></span> | <span data-ttu-id="9a78d-129">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-129">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-130">SYSTEM_ALPC_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-130">SYSTEM_ALPC_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span><span class="sxs-lookup"><span data-stu-id="9a78d-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span></span> |
 
### <a name="system-config-provider"></a><span data-ttu-id="9a78d-132">Systemkonfigurationsanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-132">System Config Provider</span></span> 

<span data-ttu-id="9a78d-133">Stellt Systemkonfigurationsereignisse bereit.</span><span class="sxs-lookup"><span data-stu-id="9a78d-133">Provides system configuration events.</span></span>

<span data-ttu-id="9a78d-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span><span class="sxs-lookup"><span data-stu-id="9a78d-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span></span>

| <span data-ttu-id="9a78d-135">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-135">Keyword</span></span> | <span data-ttu-id="9a78d-136">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-136">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-137">SYSTEM_CONFIG_KW_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="9a78d-137">SYSTEM_CONFIG_KW_SYSTEM</span></span> | <span data-ttu-id="9a78d-138">PERF_SYSCFG_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="9a78d-138">PERF_SYSCFG_SYSTEM</span></span> |
| <span data-ttu-id="9a78d-139">SYSTEM_CONFIG_KW_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="9a78d-139">SYSTEM_CONFIG_KW_GRAPHICS</span></span> | <span data-ttu-id="9a78d-140">PERF_SYSCFG_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="9a78d-140">PERF_SYSCFG_GRAPHICS</span></span> |
| <span data-ttu-id="9a78d-141">SYSTEM_CONFIG_KW_STORAGE</span><span class="sxs-lookup"><span data-stu-id="9a78d-141">SYSTEM_CONFIG_KW_STORAGE</span></span> | <span data-ttu-id="9a78d-142">PERF_SYSCFG_STORAGE</span><span class="sxs-lookup"><span data-stu-id="9a78d-142">PERF_SYSCFG_STORAGE</span></span> |
| <span data-ttu-id="9a78d-143">SYSTEM_CONFIG_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="9a78d-143">SYSTEM_CONFIG_KW_NETWORK</span></span> | <span data-ttu-id="9a78d-144">PERF_SYSCFG_NETWORK</span><span class="sxs-lookup"><span data-stu-id="9a78d-144">PERF_SYSCFG_NETWORK</span></span> |
| <span data-ttu-id="9a78d-145">SYSTEM_CONFIG_KW_SERVICES</span><span class="sxs-lookup"><span data-stu-id="9a78d-145">SYSTEM_CONFIG_KW_SERVICES</span></span> | <span data-ttu-id="9a78d-146">PERF_SYSCFG_SERVICES</span><span class="sxs-lookup"><span data-stu-id="9a78d-146">PERF_SYSCFG_SERVICES</span></span> |
| <span data-ttu-id="9a78d-147">SYSTEM_CONFIG_KW_PNP</span><span class="sxs-lookup"><span data-stu-id="9a78d-147">SYSTEM_CONFIG_KW_PNP</span></span> | <span data-ttu-id="9a78d-148">PERF_SYSCFG_PNP</span><span class="sxs-lookup"><span data-stu-id="9a78d-148">PERF_SYSCFG_PNP</span></span> |
| <span data-ttu-id="9a78d-149">SYSTEM_CONFIG_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-149">SYSTEM_CONFIG_KW_OPTICAL</span></span> | <span data-ttu-id="9a78d-150">PERF_SYSCFG_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-150">PERF_SYSCFG_OPTICAL</span></span> |
 
### <a name="system-cpu-provider"></a><span data-ttu-id="9a78d-151">System-CPU-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-151">System CPU Provider</span></span> 

<span data-ttu-id="9a78d-152">Stellt Ereignisse bereit, die sich auf die CPU beziehen.</span><span class="sxs-lookup"><span data-stu-id="9a78d-152">Provides events related to the CPU.</span></span>

<span data-ttu-id="9a78d-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span><span class="sxs-lookup"><span data-stu-id="9a78d-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span></span>

| <span data-ttu-id="9a78d-154">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-154">Keyword</span></span> | <span data-ttu-id="9a78d-155">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-155">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-156">SYSTEM_CPU_KW_CONFIG</span><span class="sxs-lookup"><span data-stu-id="9a78d-156">SYSTEM_CPU_KW_CONFIG</span></span> | <span data-ttu-id="9a78d-157">PERF_CPU_CONFIG</span><span class="sxs-lookup"><span data-stu-id="9a78d-157">PERF_CPU_CONFIG</span></span> |
| <span data-ttu-id="9a78d-158">SYSTEM_CPU_KW_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="9a78d-158">SYSTEM_CPU_KW_CACHE_FLUSH</span></span> | <span data-ttu-id="9a78d-159">PERF_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="9a78d-159">PERF_CACHE_FLUSH</span></span> |
| <span data-ttu-id="9a78d-160">SYSTEM_CPU_KW_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="9a78d-160">SYSTEM_CPU_KW_SPEC_CONTROL</span></span> | <span data-ttu-id="9a78d-161">PERF_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="9a78d-161">PERF_SPEC_CONTROL</span></span> |
 
### <a name="system-hypervisor-provider"></a><span data-ttu-id="9a78d-162">System Hypervisor Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-162">System Hypervisor Provider</span></span> 

<span data-ttu-id="9a78d-163">Stellt Ereignisse bereit, die sich auf den Hypervisor beziehen.</span><span class="sxs-lookup"><span data-stu-id="9a78d-163">Provides events relating to the hypervisor.</span></span>

<span data-ttu-id="9a78d-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span><span class="sxs-lookup"><span data-stu-id="9a78d-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span></span>

| <span data-ttu-id="9a78d-165">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-165">Keyword</span></span> | <span data-ttu-id="9a78d-166">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-166">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-167">SYSTEM_HYPERVISOR_KW_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9a78d-167">SYSTEM_HYPERVISOR_KW_PROFILE</span></span> | <span data-ttu-id="9a78d-168">PERF_HV_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9a78d-168">PERF_HV_PROFILE</span></span> |
| <span data-ttu-id="9a78d-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span></span> | <span data-ttu-id="9a78d-170">PERF_HV_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-170">PERF_HV_CALLOUTS</span></span> |
| <span data-ttu-id="9a78d-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9a78d-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span></span> | <span data-ttu-id="9a78d-172">PERF_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9a78d-172">PERF_VTL_CHANGE</span></span> |
 
### <a name="system-interrupt-provider"></a><span data-ttu-id="9a78d-173">Systemunterbrechungsanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-173">System Interrupt Provider</span></span> 

<span data-ttu-id="9a78d-174">Stellt Ereignisse im Zusammenhang mit DPCs und Interrupts bereit.</span><span class="sxs-lookup"><span data-stu-id="9a78d-174">Provides events relating to DPCs and interrupts.</span></span>

<span data-ttu-id="9a78d-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span><span class="sxs-lookup"><span data-stu-id="9a78d-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span></span>

| <span data-ttu-id="9a78d-176">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-176">Keyword</span></span> | <span data-ttu-id="9a78d-177">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-177">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-178">SYSTEM_INTERRUPT_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-178">SYSTEM_INTERRUPT_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="9a78d-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span></span> |
| <span data-ttu-id="9a78d-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="9a78d-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span></span> | <span data-ttu-id="9a78d-181">PERF_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="9a78d-181">PERF_CLOCK_INTERRUPT</span></span> |
| <span data-ttu-id="9a78d-182">SYSTEM_INTERRUPT_KW_DPC</span><span class="sxs-lookup"><span data-stu-id="9a78d-182">SYSTEM_INTERRUPT_KW_DPC</span></span> | <span data-ttu-id="9a78d-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span><span class="sxs-lookup"><span data-stu-id="9a78d-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span></span> |
| <span data-ttu-id="9a78d-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="9a78d-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span></span> | <span data-ttu-id="9a78d-185">PERF_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="9a78d-185">PERF_DPC_QUEUE</span></span> |
| <span data-ttu-id="9a78d-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="9a78d-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span></span> | <span data-ttu-id="9a78d-187">PERF_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="9a78d-187">PERF_WDF_DPC</span></span> |
| <span data-ttu-id="9a78d-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="9a78d-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span></span> | <span data-ttu-id="9a78d-189">PERF_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="9a78d-189">PERF_WDF_INTERRUPT</span></span> |
| <span data-ttu-id="9a78d-190">SYSTEM_INTERRUPT_KW_IPI</span><span class="sxs-lookup"><span data-stu-id="9a78d-190">SYSTEM_INTERRUPT_KW_IPI</span></span> | <span data-ttu-id="9a78d-191">PERF_IPI</span><span class="sxs-lookup"><span data-stu-id="9a78d-191">PERF_IPI</span></span> |
 
 
### <a name="system-io-provider"></a><span data-ttu-id="9a78d-192">System-E/A-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-192">System IO Provider</span></span> 

<span data-ttu-id="9a78d-193">Stellt Ereignisse im Zusammenhang mit mehreren Arten von E/A bereit, einschließlich Datenträger, Cache und Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9a78d-193">Provides events relating to multiple kinds of IO including disk, cache, and network.</span></span>

<span data-ttu-id="9a78d-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span><span class="sxs-lookup"><span data-stu-id="9a78d-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span></span>

| <span data-ttu-id="9a78d-195">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-195">Keyword</span></span> | <span data-ttu-id="9a78d-196">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-196">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-197">SYSTEM_IO_KW_DISK</span><span class="sxs-lookup"><span data-stu-id="9a78d-197">SYSTEM_IO_KW_DISK</span></span> | <span data-ttu-id="9a78d-198">EVENT_TRACE_FLAG_DISK_IO</span><span class="sxs-lookup"><span data-stu-id="9a78d-198">EVENT_TRACE_FLAG_DISK_IO</span></span> |
| <span data-ttu-id="9a78d-199">SYSTEM_IO_KW_DISK_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-199">SYSTEM_IO_KW_DISK_INIT</span></span> | <span data-ttu-id="9a78d-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span></span> |
| <span data-ttu-id="9a78d-201">SYSTEM_IO_KW_FILENAME</span><span class="sxs-lookup"><span data-stu-id="9a78d-201">SYSTEM_IO_KW_FILENAME</span></span> | <span data-ttu-id="9a78d-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="9a78d-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span></span> |
| <span data-ttu-id="9a78d-203">SYSTEM_IO_KW_SPLIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-203">SYSTEM_IO_KW_SPLIT</span></span> | <span data-ttu-id="9a78d-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span><span class="sxs-lookup"><span data-stu-id="9a78d-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span></span> |
| <span data-ttu-id="9a78d-205">SYSTEM_IO_KW_FILE</span><span class="sxs-lookup"><span data-stu-id="9a78d-205">SYSTEM_IO_KW_FILE</span></span> | <span data-ttu-id="9a78d-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="9a78d-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span></span> |
| <span data-ttu-id="9a78d-207">SYSTEM_IO_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-207">SYSTEM_IO_KW_OPTICAL</span></span> | <span data-ttu-id="9a78d-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span></span> |
| <span data-ttu-id="9a78d-209">SYSTEM_IO_KW_OPTICAL_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-209">SYSTEM_IO_KW_OPTICAL_INIT</span></span> | <span data-ttu-id="9a78d-210">PERF_OPTICAL_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-210">PERF_OPTICAL_IO_INIT</span></span> |
| <span data-ttu-id="9a78d-211">SYSTEM_IO_KW_DRIVERS</span><span class="sxs-lookup"><span data-stu-id="9a78d-211">SYSTEM_IO_KW_DRIVERS</span></span> | <span data-ttu-id="9a78d-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span><span class="sxs-lookup"><span data-stu-id="9a78d-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span></span> |
| <span data-ttu-id="9a78d-213">SYSTEM_IO_KW_CC</span><span class="sxs-lookup"><span data-stu-id="9a78d-213">SYSTEM_IO_KW_CC</span></span> | <span data-ttu-id="9a78d-214">PERF_CC</span><span class="sxs-lookup"><span data-stu-id="9a78d-214">PERF_CC</span></span> |
| <span data-ttu-id="9a78d-215">SYSTEM_IO_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="9a78d-215">SYSTEM_IO_KW_NETWORK</span></span> | <span data-ttu-id="9a78d-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span><span class="sxs-lookup"><span data-stu-id="9a78d-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span></span> |

<span data-ttu-id="9a78d-217">Hinweis: Wenn Sie das Schlüsselwort SYSTEM_IO_KW_DRIVERS aktivieren, werden auch SYSTEM_IO_KW_FILENAME automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9a78d-217">Note: Enabling the SYSTEM_IO_KW_DRIVERS keyword will automatically enable SYSTEM_IO_KW_FILENAME as well.</span></span>  <span data-ttu-id="9a78d-218">Die SYSTEM_IO_KW_FILENAME wird auch automatisch aktiviert, wenn der Systemspeicheranbieter mit dem Schlüsselwort SYSTEM_MEMORY_KW_MEMORY aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a78d-218">The SYSTEM_IO_KW_FILENAME is also automatically turned on when the System Memory Provider is enabled with the SYSTEM_MEMORY_KW_MEMORY keyword.</span></span>
 
### <a name="system-io-filter-provider"></a><span data-ttu-id="9a78d-219">System-E/A-Filteranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-219">System IO Filter Provider</span></span> 

<span data-ttu-id="9a78d-220">Stellt Ereignisse im Zusammenhang mit der E/A-Filterung bereit, einschließlich Zeitsteuerung und Fehlern.</span><span class="sxs-lookup"><span data-stu-id="9a78d-220">Provides events related to IO filtering including timing and failures.</span></span>

<span data-ttu-id="9a78d-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span><span class="sxs-lookup"><span data-stu-id="9a78d-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span></span>

| <span data-ttu-id="9a78d-222">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-222">Keyword</span></span> | <span data-ttu-id="9a78d-223">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-223">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-224">SYSTEM_IOFILTER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-224">SYSTEM_IOFILTER_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-225">PERF_FLT_IO</span><span class="sxs-lookup"><span data-stu-id="9a78d-225">PERF_FLT_IO</span></span> |
| <span data-ttu-id="9a78d-226">SYSTEM_IOFILTER_KW_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-226">SYSTEM_IOFILTER_KW_INIT</span></span> | <span data-ttu-id="9a78d-227">PERF_FLT_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="9a78d-227">PERF_FLT_IO_INIT</span></span> |
| <span data-ttu-id="9a78d-228">SYSTEM_IOFILTER_KW_FASTIO</span><span class="sxs-lookup"><span data-stu-id="9a78d-228">SYSTEM_IOFILTER_KW_FASTIO</span></span> | <span data-ttu-id="9a78d-229">PERF_FLT_FASTIO</span><span class="sxs-lookup"><span data-stu-id="9a78d-229">PERF_FLT_FASTIO</span></span> |
| <span data-ttu-id="9a78d-230">SYSTEM_IOFILTER_KW_FAILURE</span><span class="sxs-lookup"><span data-stu-id="9a78d-230">SYSTEM_IOFILTER_KW_FAILURE</span></span> | <span data-ttu-id="9a78d-231">PERF_FLT_IO_FAILURE</span><span class="sxs-lookup"><span data-stu-id="9a78d-231">PERF_FLT_IO_FAILURE</span></span> |
 
### <a name="system-lock-provider"></a><span data-ttu-id="9a78d-232">Systemsperranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-232">System Lock Provider</span></span> 

<span data-ttu-id="9a78d-233">Stellt Ereignisse im Zusammenhang mit Kernelsperrmechanismen bereit.</span><span class="sxs-lookup"><span data-stu-id="9a78d-233">Provides events relating to kernel locking mechanisms.</span></span>

<span data-ttu-id="9a78d-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span><span class="sxs-lookup"><span data-stu-id="9a78d-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span></span>

| <span data-ttu-id="9a78d-235">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-235">Keyword</span></span> | <span data-ttu-id="9a78d-236">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-236">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-237">SYSTEM_LOCK_KW_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="9a78d-237">SYSTEM_LOCK_KW_SPINLOCK</span></span> | <span data-ttu-id="9a78d-238">PERF_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="9a78d-238">PERF_SPINLOCK</span></span> |
| <span data-ttu-id="9a78d-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="9a78d-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span></span> | <span data-ttu-id="9a78d-240">PERF_SPINLOCK_CNTRS</span><span class="sxs-lookup"><span data-stu-id="9a78d-240">PERF_SPINLOCK_CNTRS</span></span> |
| <span data-ttu-id="9a78d-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span></span> | <span data-ttu-id="9a78d-242">PERF_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-242">PERF_SYNC_OBJECTS</span></span> |
 
### <a name="system-memory-provider"></a><span data-ttu-id="9a78d-243">Systemspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-243">System Memory Provider</span></span> 

<span data-ttu-id="9a78d-244">Stellt Ereignisse bereit, die sich auf den Speicher-Manager beziehen.</span><span class="sxs-lookup"><span data-stu-id="9a78d-244">Provides events relating to the memory manager.</span></span>

<span data-ttu-id="9a78d-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span><span class="sxs-lookup"><span data-stu-id="9a78d-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span></span>

| <span data-ttu-id="9a78d-246">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-246">Keyword</span></span> | <span data-ttu-id="9a78d-247">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-247">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-248">SYSTEM_MEMORY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-248">SYSTEM_MEMORY_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-249">PERF_MEMORY</span><span class="sxs-lookup"><span data-stu-id="9a78d-249">PERF_MEMORY</span></span> |
| <span data-ttu-id="9a78d-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span></span> | <span data-ttu-id="9a78d-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span></span> |
| <span data-ttu-id="9a78d-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span></span> | <span data-ttu-id="9a78d-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span></span> |
| <span data-ttu-id="9a78d-254">SYSTEM_MEMORY_KW_POOL</span><span class="sxs-lookup"><span data-stu-id="9a78d-254">SYSTEM_MEMORY_KW_POOL</span></span> | <span data-ttu-id="9a78d-255">PERF_POOL</span><span class="sxs-lookup"><span data-stu-id="9a78d-255">PERF_POOL</span></span> |
| <span data-ttu-id="9a78d-256">SYSTEM_MEMORY_KW_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="9a78d-256">SYSTEM_MEMORY_KW_MEMINFO</span></span> | <span data-ttu-id="9a78d-257">PERF_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="9a78d-257">PERF_MEMINFO</span></span> |
| <span data-ttu-id="9a78d-258">SYSTEM_MEMORY_KW_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="9a78d-258">SYSTEM_MEMORY_KW_PFSECTION</span></span> | <span data-ttu-id="9a78d-259">PERF_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="9a78d-259">PERF_PFSECTION</span></span> |
| <span data-ttu-id="9a78d-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="9a78d-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span></span> | <span data-ttu-id="9a78d-261">PERF_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="9a78d-261">PERF_MEMINFO_WS</span></span> |
| <span data-ttu-id="9a78d-262">SYSTEM_MEMORY_KW_HEAP</span><span class="sxs-lookup"><span data-stu-id="9a78d-262">SYSTEM_MEMORY_KW_HEAP</span></span> | <span data-ttu-id="9a78d-263">PERF_HEAP</span><span class="sxs-lookup"><span data-stu-id="9a78d-263">PERF_HEAP</span></span> |
| <span data-ttu-id="9a78d-264">SYSTEM_MEMORY_KW_WS</span><span class="sxs-lookup"><span data-stu-id="9a78d-264">SYSTEM_MEMORY_KW_WS</span></span> | <span data-ttu-id="9a78d-265">PERF_WS</span><span class="sxs-lookup"><span data-stu-id="9a78d-265">PERF_WS</span></span> |
| <span data-ttu-id="9a78d-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="9a78d-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span></span> | <span data-ttu-id="9a78d-267">PERF_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="9a78d-267">PERF_CONTMEM_GEN</span></span> |
| <span data-ttu-id="9a78d-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="9a78d-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span></span> | <span data-ttu-id="9a78d-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="9a78d-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span></span> |
| <span data-ttu-id="9a78d-270">SYSTEM_MEMORY_KW_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="9a78d-270">SYSTEM_MEMORY_KW_FOOTPRINT</span></span> | <span data-ttu-id="9a78d-271">PERF_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="9a78d-271">PERF_FOOTPRINT</span></span> |
| <span data-ttu-id="9a78d-272">SYSTEM_MEMORY_KW_SESSION</span><span class="sxs-lookup"><span data-stu-id="9a78d-272">SYSTEM_MEMORY_KW_SESSION</span></span> | <span data-ttu-id="9a78d-273">PERF_SESSION</span><span class="sxs-lookup"><span data-stu-id="9a78d-273">PERF_SESSION</span></span> |
| <span data-ttu-id="9a78d-274">SYSTEM_MEMORY_KW_REFSET</span><span class="sxs-lookup"><span data-stu-id="9a78d-274">SYSTEM_MEMORY_KW_REFSET</span></span> | <span data-ttu-id="9a78d-275">PERF_REFSET</span><span class="sxs-lookup"><span data-stu-id="9a78d-275">PERF_REFSET</span></span> |
| <span data-ttu-id="9a78d-276">SYSTEM_MEMORY_KW_VAMAP</span><span class="sxs-lookup"><span data-stu-id="9a78d-276">SYSTEM_MEMORY_KW_VAMAP</span></span> | <span data-ttu-id="9a78d-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span><span class="sxs-lookup"><span data-stu-id="9a78d-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span></span> |

<span data-ttu-id="9a78d-278">Hinweise:</span><span class="sxs-lookup"><span data-stu-id="9a78d-278">Notes:</span></span> 
* <span data-ttu-id="9a78d-279">Wenn Sie das Schlüsselwort SYSTEM_MEMORY_KW_MEMORY aktivieren, wird SYSTEM_IO_KW_FILENAME automatisch auch auf dem System-E/A-Anbieter aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9a78d-279">Enabling the SYSTEM_MEMORY_KW_MEMORY keyword will automatically enable SYSTEM_IO_KW_FILENAME on the System IO Provider as well.</span></span>
* <span data-ttu-id="9a78d-280">Die vom SYSTEM_MEMORY_KW_POOL aktivierten Ereignisse unterstützen einen Pooltagfilter, um Ereignisse selektiv nur für bestimmte Pooltags zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9a78d-280">The events enabled by the SYSTEM_MEMORY_KW_POOL support a Pool Tag Filter, to selectively write events only for certain pool tags.</span></span>  <span data-ttu-id="9a78d-281">Dies wird als [schematisierter Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) für den Systemspeicheranbieter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9a78d-281">This is configured as a [Schematized Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) on the System Memory Provider.</span></span>  <span data-ttu-id="9a78d-282">Der PoolTag-Filter wird wie folgt erstellt:</span><span class="sxs-lookup"><span data-stu-id="9a78d-282">The PoolTag filter is constructed as follows:</span></span>

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* <span data-ttu-id="9a78d-283">Die [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) sollte initialisiert werden, wobei id auf SYSTEM_MEMORY_POOL_FILTER_ID und das Größenfeld auf die Größe von Header plus den verwendeten Teil des PoolTags-Arrays festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9a78d-283">The [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) should be initialized with Id set to SYSTEM_MEMORY_POOL_FILTER_ID and the size field set to the size of Header plus the used portion of the PoolTags array.</span></span>  

* <span data-ttu-id="9a78d-284">Jedes Pooltag ist eine 4-stellige Zeichenfolge, die als ULONG im Filter gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9a78d-284">Each Pool Tag is a 4 character string that is stored as a ULONG in the filter.</span></span>  
 
 
### <a name="system-object-provider"></a><span data-ttu-id="9a78d-285">Systemobjektanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-285">System Object Provider</span></span> 

<span data-ttu-id="9a78d-286">Stellt Ereignisse bereit, die sich auf den Objekt-Manager beziehen.</span><span class="sxs-lookup"><span data-stu-id="9a78d-286">Provides events relating to the Object Manager.</span></span>

<span data-ttu-id="9a78d-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span><span class="sxs-lookup"><span data-stu-id="9a78d-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span></span>

| <span data-ttu-id="9a78d-288">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-288">Keyword</span></span> | <span data-ttu-id="9a78d-289">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-289">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-290">SYSTEM_OBJECT_KW_HANDLE</span><span class="sxs-lookup"><span data-stu-id="9a78d-290">SYSTEM_OBJECT_KW_HANDLE</span></span> | <span data-ttu-id="9a78d-291">PERF_OB_HANDLE</span><span class="sxs-lookup"><span data-stu-id="9a78d-291">PERF_OB_HANDLE</span></span> |
| <span data-ttu-id="9a78d-292">SYSTEM_OBJECT_KW_OBJECT</span><span class="sxs-lookup"><span data-stu-id="9a78d-292">SYSTEM_OBJECT_KW_OBJECT</span></span> | <span data-ttu-id="9a78d-293">PERF_OB_OBJECT</span><span class="sxs-lookup"><span data-stu-id="9a78d-293">PERF_OB_OBJECT</span></span> |
 
### <a name="system-power-provider"></a><span data-ttu-id="9a78d-294">System Power Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-294">System Power Provider</span></span> 

<span data-ttu-id="9a78d-295">Stellt Ereignisse bereit, die sich auf den Energiezustand des Systems beziehen.</span><span class="sxs-lookup"><span data-stu-id="9a78d-295">Provides events relating to the system's power state.</span></span>

<span data-ttu-id="9a78d-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span><span class="sxs-lookup"><span data-stu-id="9a78d-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span></span>

| <span data-ttu-id="9a78d-297">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-297">Keyword</span></span> | <span data-ttu-id="9a78d-298">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-298">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-299">SYSTEM_POWER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-299">SYSTEM_POWER_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-300">PERF_POWER</span><span class="sxs-lookup"><span data-stu-id="9a78d-300">PERF_POWER</span></span> |
| <span data-ttu-id="9a78d-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="9a78d-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span></span> | <span data-ttu-id="9a78d-302">PERF_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="9a78d-302">PERF_HIBER_RUNDOWN</span></span> |
| <span data-ttu-id="9a78d-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a78d-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span></span> | <span data-ttu-id="9a78d-304">PERF_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a78d-304">PERF_PROCESSOR_IDLE</span></span> |
| <span data-ttu-id="9a78d-305">SYSTEM_POWER_KW_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="9a78d-305">SYSTEM_POWER_KW_IDLE_SELECTION</span></span> | <span data-ttu-id="9a78d-306">PERF_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="9a78d-306">PERF_IDLE_SELECTION</span></span> |
| <span data-ttu-id="9a78d-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="9a78d-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span></span> | <span data-ttu-id="9a78d-308">PERF_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="9a78d-308">PERF_PPM_EXIT_LATENCY</span></span> |
 
### <a name="system-process-provider"></a><span data-ttu-id="9a78d-309">Systemprozessanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-309">System Process Provider</span></span> 

<span data-ttu-id="9a78d-310">Stellt Ereignisse im Zusammenhang mit dem Prozess einschließlich Lebensdauerinformationen, Bildladeereignissen und threadbezogenen Ereignissen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a78d-310">Provides events relating to the process, including lifetime information, image load events, and thread related events.</span></span>

<span data-ttu-id="9a78d-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span><span class="sxs-lookup"><span data-stu-id="9a78d-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span></span>

| <span data-ttu-id="9a78d-312">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-312">Keyword</span></span> | <span data-ttu-id="9a78d-313">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-313">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-314">SYSTEM_PROCESS_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-314">SYSTEM_PROCESS_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span><span class="sxs-lookup"><span data-stu-id="9a78d-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span></span> |
| <span data-ttu-id="9a78d-316">SYSTEM_PROCESS_KW_INSWAP</span><span class="sxs-lookup"><span data-stu-id="9a78d-316">SYSTEM_PROCESS_KW_INSWAP</span></span> | <span data-ttu-id="9a78d-317">PERF_PROCESS_INSWAP</span><span class="sxs-lookup"><span data-stu-id="9a78d-317">PERF_PROCESS_INSWAP</span></span> |
| <span data-ttu-id="9a78d-318">SYSTEM_PROCESS_KW_FREEZE</span><span class="sxs-lookup"><span data-stu-id="9a78d-318">SYSTEM_PROCESS_KW_FREEZE</span></span> | <span data-ttu-id="9a78d-319">PERF_PROCESS_FREEZE</span><span class="sxs-lookup"><span data-stu-id="9a78d-319">PERF_PROCESS_FREEZE</span></span> |
| <span data-ttu-id="9a78d-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span><span class="sxs-lookup"><span data-stu-id="9a78d-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span></span> | <span data-ttu-id="9a78d-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="9a78d-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span></span> |
| <span data-ttu-id="9a78d-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="9a78d-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span></span> | <span data-ttu-id="9a78d-323">PERF_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="9a78d-323">PERF_WAKE_COUNTER</span></span> |
| <span data-ttu-id="9a78d-324">SYSTEM_PROCESS_KW_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="9a78d-324">SYSTEM_PROCESS_KW_WAKE_DROP</span></span> | <span data-ttu-id="9a78d-325">PERF_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="9a78d-325">PERF_WAKE_DROP</span></span> |
| <span data-ttu-id="9a78d-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="9a78d-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span></span> | <span data-ttu-id="9a78d-327">PERF_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="9a78d-327">PERF_WAKE_EVENT</span></span> |
| <span data-ttu-id="9a78d-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span></span> | <span data-ttu-id="9a78d-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="9a78d-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span></span> |
| <span data-ttu-id="9a78d-330">SYSTEM_PROCESS_KW_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="9a78d-330">SYSTEM_PROCESS_KW_DBGPRINT</span></span> | <span data-ttu-id="9a78d-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="9a78d-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span></span> |
| <span data-ttu-id="9a78d-332">SYSTEM_PROCESS_KW_JOB</span><span class="sxs-lookup"><span data-stu-id="9a78d-332">SYSTEM_PROCESS_KW_JOB</span></span> | <span data-ttu-id="9a78d-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span><span class="sxs-lookup"><span data-stu-id="9a78d-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span></span> |
| <span data-ttu-id="9a78d-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="9a78d-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span></span> | <span data-ttu-id="9a78d-335">PERF_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="9a78d-335">PERF_WORKER_THREAD</span></span> |
| <span data-ttu-id="9a78d-336">SYSTEM_PROCESS_KW_THREAD</span><span class="sxs-lookup"><span data-stu-id="9a78d-336">SYSTEM_PROCESS_KW_THREAD</span></span> | <span data-ttu-id="9a78d-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span><span class="sxs-lookup"><span data-stu-id="9a78d-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span></span> |
| <span data-ttu-id="9a78d-338">SYSTEM_PROCESS_KW_LOADER</span><span class="sxs-lookup"><span data-stu-id="9a78d-338">SYSTEM_PROCESS_KW_LOADER</span></span> | <span data-ttu-id="9a78d-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span><span class="sxs-lookup"><span data-stu-id="9a78d-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span></span> |
 
### <a name="system-profile-provider"></a><span data-ttu-id="9a78d-340">Systemprofilanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-340">System Profile Provider</span></span> 

<span data-ttu-id="9a78d-341">Stellt Profilerstellungsereignisse zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a78d-341">Provides profiling events.</span></span>

<span data-ttu-id="9a78d-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span><span class="sxs-lookup"><span data-stu-id="9a78d-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span></span>

| <span data-ttu-id="9a78d-343">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-343">Keyword</span></span> | <span data-ttu-id="9a78d-344">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-344">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-345">SYSTEM_PROFILE_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-345">SYSTEM_PROFILE_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9a78d-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span></span> |
| <span data-ttu-id="9a78d-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9a78d-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span></span> | <span data-ttu-id="9a78d-348">PERF_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9a78d-348">PERF_PMC_PROFILE</span></span> |
 
### <a name="system-registry-provider"></a><span data-ttu-id="9a78d-349">Systemregistrierungsanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-349">System Registry Provider</span></span> 

<span data-ttu-id="9a78d-350">Stellt Ereignisse im Zusammenhang mit der Registrierung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a78d-350">Provides events relating to the registry.</span></span>

<span data-ttu-id="9a78d-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span><span class="sxs-lookup"><span data-stu-id="9a78d-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span></span>

| <span data-ttu-id="9a78d-352">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-352">Keyword</span></span> | <span data-ttu-id="9a78d-353">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-353">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-354">SYSTEM_REGISTRY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-354">SYSTEM_REGISTRY_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="9a78d-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span></span> |
| <span data-ttu-id="9a78d-356">SYSTEM_REGISTRY_KW_HIVE</span><span class="sxs-lookup"><span data-stu-id="9a78d-356">SYSTEM_REGISTRY_KW_HIVE</span></span> | <span data-ttu-id="9a78d-357">PERF_REG_HIVE</span><span class="sxs-lookup"><span data-stu-id="9a78d-357">PERF_REG_HIVE</span></span> |
| <span data-ttu-id="9a78d-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9a78d-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span></span> | <span data-ttu-id="9a78d-359">PERF_REG_NOTIF</span><span class="sxs-lookup"><span data-stu-id="9a78d-359">PERF_REG_NOTIF</span></span> |
 
### <a name="system-scheduler-provider"></a><span data-ttu-id="9a78d-360">Systemplaneranbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-360">System Scheduler Provider</span></span> 

<span data-ttu-id="9a78d-361">Stellt Ereignisse im Zusammenhang mit dem Planer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a78d-361">Provides events relating to the scheduler.</span></span>

<span data-ttu-id="9a78d-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span><span class="sxs-lookup"><span data-stu-id="9a78d-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span></span>

| <span data-ttu-id="9a78d-363">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-363">Keyword</span></span> | <span data-ttu-id="9a78d-364">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-364">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="9a78d-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span></span> | <span data-ttu-id="9a78d-366">PERF_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="9a78d-366">PERF_XSCHEDULER</span></span> |
| <span data-ttu-id="9a78d-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="9a78d-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span></span> | <span data-ttu-id="9a78d-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="9a78d-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span></span> |
| <span data-ttu-id="9a78d-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="9a78d-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span></span> | <span data-ttu-id="9a78d-370">PERF_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="9a78d-370">PERF_KERNEL_QUEUE</span></span> |
| <span data-ttu-id="9a78d-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="9a78d-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span></span> | <span data-ttu-id="9a78d-372">PERF_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="9a78d-372">PERF_SHOULD_YIELD</span></span> |
| <span data-ttu-id="9a78d-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="9a78d-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span></span> | <span data-ttu-id="9a78d-374">PERF_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="9a78d-374">PERF_ANTI_STARVATION</span></span> |
| <span data-ttu-id="9a78d-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="9a78d-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span></span> | <span data-ttu-id="9a78d-376">PERF_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="9a78d-376">PERF_LOAD_BALANCER</span></span> |
| <span data-ttu-id="9a78d-377">SYSTEM_SCHEDULER_KW_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="9a78d-377">SYSTEM_SCHEDULER_KW_AFFINITY</span></span> | <span data-ttu-id="9a78d-378">PERF_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="9a78d-378">PERF_AFFINITY</span></span> |
| <span data-ttu-id="9a78d-379">SYSTEM_SCHEDULER_KW_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="9a78d-379">SYSTEM_SCHEDULER_KW_PRIORITY</span></span> | <span data-ttu-id="9a78d-380">PERF_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="9a78d-380">PERF_PRIORITY</span></span> |
| <span data-ttu-id="9a78d-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="9a78d-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span></span> | <span data-ttu-id="9a78d-382">PERF_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="9a78d-382">PERF_IDEAL_PROCESSOR</span></span> |
| <span data-ttu-id="9a78d-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span><span class="sxs-lookup"><span data-stu-id="9a78d-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span></span> | <span data-ttu-id="9a78d-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span><span class="sxs-lookup"><span data-stu-id="9a78d-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span></span> |
 
### <a name="system-syscall-provider"></a><span data-ttu-id="9a78d-385">System Syscall Provider</span><span class="sxs-lookup"><span data-stu-id="9a78d-385">System Syscall Provider</span></span> 

<span data-ttu-id="9a78d-386">Stellt Ereignisse mit Informationen zu Systemaufrufen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a78d-386">Provides events with information about system calls.</span></span>

<span data-ttu-id="9a78d-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span><span class="sxs-lookup"><span data-stu-id="9a78d-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span></span>

| <span data-ttu-id="9a78d-388">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-388">Keyword</span></span> | <span data-ttu-id="9a78d-389">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-389">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-390">SYSTEM_SYSCALL_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-390">SYSTEM_SYSCALL_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span><span class="sxs-lookup"><span data-stu-id="9a78d-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span></span> |
 
### <a name="system-timer-provider"></a><span data-ttu-id="9a78d-392">Systemzeitgeberanbieter</span><span class="sxs-lookup"><span data-stu-id="9a78d-392">System Timer Provider</span></span> 

<span data-ttu-id="9a78d-393">Stellt Ereignisse im Zusammenhang mit Timern im Kernel zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a78d-393">Provides events relating to timers in the kernel.</span></span>

<span data-ttu-id="9a78d-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span><span class="sxs-lookup"><span data-stu-id="9a78d-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span></span>

| <span data-ttu-id="9a78d-395">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9a78d-395">Keyword</span></span> | <span data-ttu-id="9a78d-396">Entsprechende Legacyflags und -gruppen</span><span class="sxs-lookup"><span data-stu-id="9a78d-396">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="9a78d-397">SYSTEM_TIMER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="9a78d-397">SYSTEM_TIMER_KW_GENERAL</span></span> | <span data-ttu-id="9a78d-398">PERF_TIMER</span><span class="sxs-lookup"><span data-stu-id="9a78d-398">PERF_TIMER</span></span> |
| <span data-ttu-id="9a78d-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="9a78d-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span></span> | <span data-ttu-id="9a78d-400">PERF_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="9a78d-400">PERF_CLOCK_TIMER</span></span> |
 
## <a name="remarks"></a><span data-ttu-id="9a78d-401">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a78d-401">Remarks</span></span>

<span data-ttu-id="9a78d-402">Dieser neue Aktivierungsmechanismus ist zusätzlich zu den bereits vorhandenen Methoden zum Aktivieren dieser Ereignisse vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9a78d-402">This new enablement mechanism is in addition to the pre-existing methods for enabling these events.</span></span>  <span data-ttu-id="9a78d-403">Jeglicher Code, der zuvor funktioniert hat, wird weiterhin verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a78d-403">Any code that used to work, will continue to do so.</span></span>
 
<span data-ttu-id="9a78d-404">Die vom Systemablaufverfolgungsanbieter generierten Ereignisse ändern sich aufgrund dieser neuen Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="9a78d-404">The events generated by the System Trace Provider are not changing due to this new feature.</span></span>  <span data-ttu-id="9a78d-405">Dies bedeutet, dass die ausgegebenen Ereignisse nicht als von den einzelnen Systemanbietern ausgegeben markiert sind.</span><span class="sxs-lookup"><span data-stu-id="9a78d-405">This means that the outputted events are not marked as being emitted from the individual system providers.</span></span>
 
<span data-ttu-id="9a78d-406">Weitere Informationen zur Anbieter-GUID und Schlüsselwortdefinitionen finden Sie unter [evntrace.h](/windows/win32/api/evntrace/).</span><span class="sxs-lookup"><span data-stu-id="9a78d-406">For more information on provider GUID and keyword definitions see [evntrace.h](/windows/win32/api/evntrace/).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a78d-407">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a78d-407">See Also</span></span>

[<span data-ttu-id="9a78d-408">Konfigurieren und Starten einer SystemTraceProvider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="9a78d-408">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)

[<span data-ttu-id="9a78d-409">evntrace.h-Header</span><span class="sxs-lookup"><span data-stu-id="9a78d-409">evntrace.h header</span></span>](/windows/win32/api/evntrace/)