---
description: Exportiert eine Verweis Punkt Auflistung in eine Datei. In der resultierenden Datei werden die Verweis Punkt Auflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen beibehalten.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Exportreferencepoint-Methode der Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362769"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="66f66-104">Exportreferencepoint-Methode der MSVM \_ collectionreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="66f66-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="66f66-105">Exportiert eine Verweis Punkt Auflistung in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="66f66-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="66f66-106">In der resultierenden Datei werden die Verweis Punkt Auflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="66f66-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66f66-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="66f66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66f66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f66-109">*Referencepointcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66f66-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f66-110">Ein Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die zu exportierende Verweis Punkt Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="66f66-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="66f66-111">*Exportdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66f66-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f66-112">Der voll qualifizierte Pfad des Verzeichnisses, in das die Verweis Punkt Auflistung exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="66f66-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="66f66-113">*Exportsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66f66-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f66-114">Eine Instanz von [**MSVM \_ collectionreferencepointexportsettingdata**](msvm-collectionreferencepointexportsettingdata.md) , die die Einstellungen für den Export Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="66f66-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="66f66-115">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="66f66-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66f66-116">Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66f66-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="66f66-117">Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="66f66-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f66-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66f66-118">Return value</span></span>

<span data-ttu-id="66f66-119">Wenn diese Methode synchron ausgeführt wird, wird 0 zurückgegeben, wenn Sie erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66f66-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="66f66-120">Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der Auftrags Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="66f66-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="66f66-121">Jeder andere Rückgabewert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="66f66-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f66-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66f66-122">Requirements</span></span>



| <span data-ttu-id="66f66-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66f66-123">Requirement</span></span> | <span data-ttu-id="66f66-124">Wert</span><span class="sxs-lookup"><span data-stu-id="66f66-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f66-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66f66-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66f66-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66f66-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="66f66-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66f66-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66f66-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="66f66-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="66f66-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="66f66-129">Namespace</span></span><br/>                | <span data-ttu-id="66f66-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="66f66-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="66f66-131">MOF</span><span class="sxs-lookup"><span data-stu-id="66f66-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66f66-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="66f66-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66f66-133">DLL</span><span class="sxs-lookup"><span data-stu-id="66f66-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66f66-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66f66-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66f66-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66f66-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f66-136">**MSVM \_ collectionreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="66f66-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




