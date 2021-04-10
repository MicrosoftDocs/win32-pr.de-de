---
title: MDM_RemoteWipe-Klasse
description: Die MDM- \_ RemoteWipe-Klasse ermöglicht eine Remote Löschung eines Geräts.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- MDM_RemoteWipe-Klasse
- MDM_RemoteWipe-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040141"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="42647-105">MDM- \_ RemoteWipe-Klasse</span><span class="sxs-lookup"><span data-stu-id="42647-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="42647-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="42647-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="42647-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="42647-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="42647-108">Die **MDM- \_ RemoteWipe** -Klasse ermöglicht eine Remote Löschung eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="42647-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="42647-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42647-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42647-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="42647-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="42647-111">Member</span><span class="sxs-lookup"><span data-stu-id="42647-111">Members</span></span>

<span data-ttu-id="42647-112">Die **MDM- \_ RemoteWipe** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="42647-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="42647-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="42647-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="42647-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42647-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42647-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="42647-115">Methods</span></span>

<span data-ttu-id="42647-116">Die **MDM- \_ RemoteWipe** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="42647-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="42647-117">Methode</span><span class="sxs-lookup"><span data-stu-id="42647-117">Method</span></span>                                              | <span data-ttu-id="42647-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42647-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="42647-119">**dowipeer Method**</span><span class="sxs-lookup"><span data-stu-id="42647-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="42647-120">Hiermit wird das Gerät ausgelöst, um die Remote Löschung zu starten.</span><span class="sxs-lookup"><span data-stu-id="42647-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="42647-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42647-121">Properties</span></span>

<span data-ttu-id="42647-122">Die **MDM- \_ RemoteWipe** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42647-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42647-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42647-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42647-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42647-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42647-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42647-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42647-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42647-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42647-127">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="42647-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="42647-128">Bei dieser Klasse ist die Zeichenfolge "RemoteWipe".</span><span class="sxs-lookup"><span data-stu-id="42647-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="42647-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="42647-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42647-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42647-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42647-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42647-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42647-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42647-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42647-133">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="42647-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="42647-134">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="42647-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="42647-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42647-135">Example</span></span>

<span data-ttu-id="42647-136">Im folgenden Beispiel wird veranschaulicht, wie RemoteWipe verwendet und die dowipeer-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="42647-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="42647-137">Dieses Beispiel muss unter "lokaler Systembenutzer" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="42647-137">This example must be executed under local system user.</span></span> <span data-ttu-id="42647-138">Laden Sie hierzu das PsExec-Tool von herunter, und führen Sie es über <https://technet.microsoft.com/sysinternals/bb897553.aspx> `psexec.exe -i -s cmd.exe` eine Eingabeaufforderung mit erhöhten Rechten aus.</span><span class="sxs-lookup"><span data-stu-id="42647-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="42647-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42647-139">Requirements</span></span>



| <span data-ttu-id="42647-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42647-140">Requirement</span></span> | <span data-ttu-id="42647-141">Wert</span><span class="sxs-lookup"><span data-stu-id="42647-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42647-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42647-142">Minimum supported client</span></span><br/> | <span data-ttu-id="42647-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42647-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42647-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42647-144">Minimum supported server</span></span><br/> | <span data-ttu-id="42647-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="42647-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="42647-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="42647-146">Namespace</span></span><br/>                | <span data-ttu-id="42647-147">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="42647-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="42647-148">MOF</span><span class="sxs-lookup"><span data-stu-id="42647-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42647-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="42647-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="42647-150">DLL</span><span class="sxs-lookup"><span data-stu-id="42647-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42647-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42647-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42647-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42647-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42647-153">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="42647-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

