---
description: Exportiert eine Momentaufnahme Sammlung virtueller Computersysteme in eine Datei. Die Momentaufnahme Sammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Exportsnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215377"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="fc278-104">Exportsnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="fc278-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="fc278-105">Exportiert eine Momentaufnahme Sammlung virtueller Computersysteme in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="fc278-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="fc278-106">Die Momentaufnahme Sammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.</span><span class="sxs-lookup"><span data-stu-id="fc278-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc278-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc278-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fc278-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc278-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc278-109">*Snapshotcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc278-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc278-110">Ein Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die zu exportierende Momentaufnahme Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc278-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="fc278-111">*Exportdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc278-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc278-112">Der voll qualifizierte Pfad des Verzeichnisses, in das die virtuelle System Sammlung exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc278-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="fc278-113">Wenn die Eigenschaft " **kreatevmexportsubdirectory** " im *exportsettingdata* -Parameter auf " **true** " festgelegt ist, kann dieses Verzeichnis für den Export mehrerer virtueller System Sammlungen wieder verwendet werden. bei dieser Methode werden die einzelnen Definitionen der virtuellen System Sammlung in einem separaten Unterverzeichnis unter diesem Pfad abgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc278-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="fc278-114">*Exportsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc278-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc278-115">Eine Instanz von [**MSVM \_ collectionsnapshotexportsettingdata**](msvm-collectionsnapshotexportsettingdata.md) , die die Einstellungen für den Export Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc278-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="fc278-116">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fc278-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc278-117">Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc278-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="fc278-118">Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fc278-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc278-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc278-119">Return value</span></span>

<span data-ttu-id="fc278-120">Wenn diese Methode synchron ausgeführt wird, wird 0 zurückgegeben, wenn Sie erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc278-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="fc278-121">Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der Auftrags Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="fc278-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="fc278-122">Jeder andere Rückgabewert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="fc278-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc278-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc278-123">Requirements</span></span>



| <span data-ttu-id="fc278-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc278-124">Requirement</span></span> | <span data-ttu-id="fc278-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fc278-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc278-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc278-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc278-127">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc278-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fc278-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc278-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc278-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fc278-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fc278-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc278-130">Namespace</span></span><br/>                | <span data-ttu-id="fc278-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc278-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc278-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fc278-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc278-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fc278-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc278-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fc278-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc278-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc278-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc278-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc278-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc278-137">**MSVM \_ collectionsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="fc278-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




