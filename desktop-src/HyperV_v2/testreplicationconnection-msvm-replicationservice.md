---
description: Überprüft, ob die Replikation vom aktuellen Host System für das angegebene Wiederherstellungs System aktiviert werden kann.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Testreplicationconnection-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342825"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="ab5c9-103">Testreplicationconnection-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab5c9-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="ab5c9-104">Überprüft, ob die Replikation vom aktuellen Host System für das angegebene Wiederherstellungs System aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab5c9-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ab5c9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab5c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab5c9-107">*Wiederherstellungsconnectionpoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5c9-108">Der Name des Verbindungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-108">The name of the connection point.</span></span> <span data-ttu-id="ab5c9-109">Bei einem Wiederherstellungs Cluster ist dies der Name des Broker-Cap.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="ab5c9-110">Bei einem eigenständigen Wiederherstellungs Server handelt es sich hierbei um den Namen des Host Systems.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="ab5c9-111">*Wiederherstellserverportnummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5c9-112">Die Portnummer des Wiederherstellungs Verbindungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="ab5c9-113">*AuthenticationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5c9-114">Das Wiederherstellungs Authentifizierungsschema.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-114">The recovery authentication scheme.</span></span> <span data-ttu-id="ab5c9-115">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="ab5c9-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="ab5c9-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrierte Authentifizierung** (1)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab5c9-117">Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="ab5c9-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikat basierte Authentifizierung** (2)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ab5c9-119">Zertifikat basierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ab5c9-120">*Certifi-ethumschlag-Druck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5c9-121">Der Zertifikat Fingerabdruck, der verwendet werden soll, wenn der *AuthenticationType* -Parameter eine Zertifikat basierte Authentifizierung ist.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="ab5c9-122">*Bypassproxyserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5c9-123">Umgehen Sie den Proxy Server beim Herstellen einer Verbindung mit dem Replikat Server.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="ab5c9-124">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5c9-125">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab5c9-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab5c9-126">Return value</span></span>

<span data-ttu-id="ab5c9-127">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ab5c9-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ab5c9-128">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-129">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-130">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="ab5c9-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-131">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-132">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-133">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="ab5c9-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-135">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-136">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-137">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="ab5c9-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-138">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="ab5c9-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-139">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="ab5c9-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-140">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ab5c9-141">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="ab5c9-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ab5c9-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab5c9-142">Requirements</span></span>



| <span data-ttu-id="ab5c9-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab5c9-143">Requirement</span></span> | <span data-ttu-id="ab5c9-144">Wert</span><span class="sxs-lookup"><span data-stu-id="ab5c9-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5c9-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5c9-146">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab5c9-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab5c9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5c9-148">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab5c9-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab5c9-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab5c9-149">Namespace</span></span><br/>                | <span data-ttu-id="ab5c9-150">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ab5c9-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ab5c9-151">MOF</span><span class="sxs-lookup"><span data-stu-id="ab5c9-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab5c9-152"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab5c9-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab5c9-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ab5c9-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab5c9-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab5c9-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab5c9-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab5c9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5c9-156">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="ab5c9-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

