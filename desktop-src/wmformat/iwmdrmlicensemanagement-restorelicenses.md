---
title: Iwmdrmlicenabmanagement restorelicenses-Methode (wmdrmsdk. h)
description: Die restorelicenses-Methode stellt Lizenzen aus einer Lizenz Sicherung wieder her, die durch Aufrufen der backuplicenses-Methode erstellt wurde.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Restorelicenses-Methode Windows Media-Format
- Restorelicenses-Methode, Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, restorelicenses-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370060"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="8acf7-106">Iwmdrmlicenabmanagement:: restorelicenses-Methode</span><span class="sxs-lookup"><span data-stu-id="8acf7-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="8acf7-107">Die **restorelicenses** -Methode stellt Lizenzen aus einer Lizenz Sicherung wieder her, die durch Aufrufen der [**backuplicenses**](iwmdrmlicensemanagement-backuplicenses.md) -Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8acf7-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8acf7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8acf7-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="8acf7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8acf7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8acf7-110">*bstraubackupdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8acf7-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8acf7-111">Der UNC-Pfad des Speicher Orts, von dem die Lizenzen wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8acf7-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="8acf7-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8acf7-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8acf7-113">Flags, die die zu verwendenden Wiederherstellungsoptionen angeben.</span><span class="sxs-lookup"><span data-stu-id="8acf7-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="8acf7-114">Das einzige Flag, das derzeit unterstützt wird, ist WMDRM \_ Restore \_ Individual, das die Methode konfiguriert, um bei Bedarf eine Individualisierung im Rahmen der Wiederherstellung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8acf7-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="8acf7-115">*ppunkcancelationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8acf7-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8acf7-116">Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8acf7-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="8acf7-117">Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8acf7-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8acf7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8acf7-118">Return value</span></span>

<span data-ttu-id="8acf7-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8acf7-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8acf7-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8acf7-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8acf7-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8acf7-121">Return code</span></span>                                                                          | <span data-ttu-id="8acf7-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8acf7-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8acf7-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8acf7-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8acf7-124">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8acf7-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8acf7-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8acf7-125">Remarks</span></span>

<span data-ttu-id="8acf7-126">Diese Methode wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8acf7-126">This method executes asynchronously.</span></span> <span data-ttu-id="8acf7-127">Sie wird unmittelbar nach dem Aufruf von zurückgegeben und generiert dann eine Reihe von **mewmdrmlicenserestoreprogress** -Ereignissen, gefolgt von einem **mewmdrmlicenserestorecomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8acf7-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="8acf7-128">Der Wert jedes **mewmdrmlicenserestoreprogress** -Ereignisses, das durch Aufrufen von **imfmediaevent:: GetValue** abgerufen wird, ist ein **IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8acf7-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="8acf7-129">Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle zum Abrufen einer Instanz der [**iwmdrmlicenanbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="8acf7-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="8acf7-130">Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="8acf7-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="8acf7-131">Die Sicherung kann vom lokalen Computer oder von einem anderen Computer erfolgen.</span><span class="sxs-lookup"><span data-stu-id="8acf7-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acf7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8acf7-132">Requirements</span></span>



| <span data-ttu-id="8acf7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8acf7-133">Requirement</span></span> | <span data-ttu-id="8acf7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="8acf7-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8acf7-135">Header</span><span class="sxs-lookup"><span data-stu-id="8acf7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8acf7-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8acf7-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8acf7-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8acf7-137">Library</span></span><br/> | <dl> <span data-ttu-id="8acf7-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8acf7-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8acf7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8acf7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acf7-140">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8acf7-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





