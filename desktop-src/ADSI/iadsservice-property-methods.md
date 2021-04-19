---
title: Iadsservice-Eigenschaften Methoden (IADs. h)
description: Lesen und schreiben Sie die in diesem Thema beschriebenen Eigenschaften.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Iadsservice-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341793"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="1d7b9-104">Iadsservice-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="1d7b9-104">IADsService Property Methods</span></span>

<span data-ttu-id="1d7b9-105">Die Eigenschaften Methoden der [**iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice) -Schnittstelle lesen und schreiben die in diesem Thema beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="1d7b9-106">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1d7b9-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1d7b9-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d7b9-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1d7b9-108">**Abhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-108">**Dependencies**</span></span>
<span data-ttu-id="1d7b9-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-110">Array von **BSTR** -Namen für Dienste oder lade Gruppen, die geladen werden müssen, damit dieser Dienst geladen wird.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="1d7b9-111">Die Syntax für den Eintrag lautet "Service:", gefolgt vom Dienstnamen oder "Group:" gefolgt vom Namen der Ladegruppe.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="1d7b9-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-114">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-114">**DisplayName**</span></span>
<span data-ttu-id="1d7b9-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-116">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="1d7b9-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-119">**ErrorControl**</span></span>
<span data-ttu-id="1d7b9-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-121">Die Aktion, die ausgeführt werden soll, wenn dieser Dienst beim Starten fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="1d7b9-122">Die folgenden Werte sind für diese Eigenschaft gültig.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="1d7b9-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>ADS- \_ Dienst \_ Fehler \_ ignorieren \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-124">Der Fehler wird vom Start Programm protokolliert, aber der Startvorgang wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="1d7b9-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>Anzeige \_ Dienst \_ Fehler \_ Normal \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-126">Das Start Programm protokolliert den Fehler und zeigt ein Meldungs Feld an, setzt den Startvorgang jedoch fort.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="1d7b9-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>ADS- \_ Dienst \_ Fehler \_ schwerwiegender \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-128">Das Start Programm protokolliert den Fehler.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-128">The startup program logs the error.</span></span> <span data-ttu-id="1d7b9-129">Wenn die zuletzt bekannte, gute Konfiguration gestartet wurde, wird der Startvorgang fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="1d7b9-130">Andernfalls wird das System mit der zuletzt bekannten, guten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="1d7b9-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>Anzeige \_ Dienst \_ Fehler \_ kritisch \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-132">Das Start Programm protokolliert den Fehler, sofern möglich.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="1d7b9-133">Wenn die zuletzt bekannte, gute Konfiguration gestartet wird, tritt beim Startvorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="1d7b9-134">Andernfalls wird das System mit der letzten als funktionierend bekannten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="1d7b9-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-136">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-137">**Host Computer**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-137">**HostComputer**</span></span>
<span data-ttu-id="1d7b9-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-139">Die ADsPath-Zeichenfolge des Hosts dieses Diensts.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="1d7b9-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-141">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="1d7b9-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-144">Name der Gruppe der Lade Reihenfolge, in der dieser Dienst Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="1d7b9-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-146">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-147">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-147">**Path**</span></span>
<span data-ttu-id="1d7b9-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-149">Pfad und Dateiname für die ausführbare Datei dieses Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="1d7b9-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-151">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-152">**ServiceAccountName**</span></span>
<span data-ttu-id="1d7b9-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-154">Der Name des Kontos, das dieser Dienst verwendet, um sich beim Start zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="1d7b9-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-156">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-157">**Serviceaccountpath**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="1d7b9-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-159">Der Pfad des Kontos, das durch die **serviceaccountpath** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="1d7b9-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-161">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-162">**ServiceType**</span></span>
<span data-ttu-id="1d7b9-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-164">Die Beschreibung, wie sich ein Dienst auf dem Host Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="1d7b9-165">Diese Eigenschaft kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="1d7b9-166">ADS \_ \_ -Dienst Kernel \_ Treiber \* \* \* \* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="1d7b9-167">ADS- \_ Dienst \_ Datei \_ System \_ Treiber \* \* \* \* (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="1d7b9-168">Eigener Prozess des ADS- \_ Dienstanbieter \_ \_ \* \* \* \* (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="1d7b9-169">ADS- \_ Dienst \_ Freigabe \_ Prozess \* \* \* \* (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="1d7b9-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-171">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-172">**Starttyp**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-172">**StartType**</span></span>
<span data-ttu-id="1d7b9-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-174">Bestimmt, wie der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-174">Determines how to start the service.</span></span> <span data-ttu-id="1d7b9-175">Die folgenden Werte sind für diese Eigenschaft gültig.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="1d7b9-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>Start des ADS- \_ Dienst \_ \_ Starts \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-177">Der Dienst ist ein Gerätetreiber, der vom System Lade Modul gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="1d7b9-178">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="1d7b9-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>Anzeigen des \_ Dienst \_ System \_ Starts \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-180">Der Dienst ist ein Gerätetreiber, der von der **IoInitSystem** -Funktion gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="1d7b9-181">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="1d7b9-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>Automatischer Start des ADS- \_ Dienstanbieter \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-183">Der Dienst wird automatisch vom Dienststeuerungs-Manager beim Systemstart gestartet.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="1d7b9-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>Start des ADS \_ Service \_ Demand \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-185">Der Dienst wird vom Dienststeuerungs-Manager gestartet, wenn ein Prozess die [**Start Service**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="1d7b9-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>ADS- \_ Dienst \_ deaktiviert \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1d7b9-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1d7b9-187">Der Dienst kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-187">The service cannot be started.</span></span> <span data-ttu-id="1d7b9-188">Der Versuch, den Dienst zu starten, führt dazu, dass der Fehlercode **Fehler \_ Dienst \_ deaktiviert** ist.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="1d7b9-189">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-190">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-191">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-191">**StartupParameters**</span></span>
<span data-ttu-id="1d7b9-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-193">Parameter, die beim Start an den Dienst übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="1d7b9-194">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-195">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d7b9-196">**Version**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-196">**Version**</span></span>
<span data-ttu-id="1d7b9-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1d7b9-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="1d7b9-198">Version des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="1d7b9-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1d7b9-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d7b9-200">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="1d7b9-201">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d7b9-201">Examples</span></span>

<span data-ttu-id="1d7b9-202">Im folgenden Codebeispiel wird gezeigt, wie alle verfügbaren Systemdienste, die auf dem Host Computer ausgeführt werden, "MyMachine", sowie der Speicherort für die ausführbaren Dateien der Dienste aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="1d7b9-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d7b9-203">Requirements</span></span>



| <span data-ttu-id="1d7b9-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d7b9-204">Requirement</span></span> | <span data-ttu-id="1d7b9-205">Wert</span><span class="sxs-lookup"><span data-stu-id="1d7b9-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7b9-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-206">Minimum supported client</span></span><br/> | <span data-ttu-id="1d7b9-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d7b9-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d7b9-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-208">Minimum supported server</span></span><br/> | <span data-ttu-id="1d7b9-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d7b9-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d7b9-210">Header</span><span class="sxs-lookup"><span data-stu-id="1d7b9-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d7b9-211"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d7b9-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="1d7b9-212">DLL</span><span class="sxs-lookup"><span data-stu-id="1d7b9-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d7b9-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d7b9-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d7b9-214">IID</span><span class="sxs-lookup"><span data-stu-id="1d7b9-214">IID</span></span><br/>                      | <span data-ttu-id="1d7b9-215">IID \_ iadsservice ist als 68af66e0-31ca-11CF-a98a-00aa006bc149 definiert.</span><span class="sxs-lookup"><span data-stu-id="1d7b9-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1d7b9-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d7b9-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7b9-217">**Iadsservice**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="1d7b9-218">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="1d7b9-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

