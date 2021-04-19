---
title: Methode "iwmdrmlicentmanagement" backuplicenses (wmdrmsdk. h)
description: Die backuplicenses-Methode erstellt eine Sicherung der Lizenzen im lokalen Lizenz Speicher.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Backuplicenses-Methode (Windows Media-Format)
- Backuplicenses-Methode Windows Media-Format, iwmdrmlicensmanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, backuplicenses-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360405"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="16c27-106">Iwmdrmlicensmanagement:: backuplicenses-Methode</span><span class="sxs-lookup"><span data-stu-id="16c27-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="16c27-107">Die **backuplicenses** -Methode erstellt eine Sicherung der Lizenzen im lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="16c27-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c27-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="16c27-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="16c27-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16c27-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c27-110">*bstraubackupdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16c27-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c27-111">Der UNC-Pfad des Speicher Orts, an dem die Lizenzen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="16c27-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="16c27-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16c27-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c27-113">Flags, die die zu verwendenden Sicherungs Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="16c27-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="16c27-114">Das einzige Flag, das derzeit unterstützt wird, ist die WMDRM- \_ Sicherung \_ überschreiben, bei der die Methode zum Überschreiben vorhandener Sicherungsdateien im Verzeichnis konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="16c27-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="16c27-115">*ppunkcancelationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="16c27-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16c27-116">Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="16c27-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="16c27-117">Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16c27-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c27-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16c27-118">Return value</span></span>

<span data-ttu-id="16c27-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="16c27-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="16c27-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="16c27-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="16c27-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="16c27-121">Return code</span></span>                                                                          | <span data-ttu-id="16c27-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16c27-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="16c27-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16c27-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="16c27-124">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16c27-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16c27-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16c27-125">Remarks</span></span>

<span data-ttu-id="16c27-126">Diese Methode wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16c27-126">This method executes asynchronously.</span></span> <span data-ttu-id="16c27-127">Sie wird unmittelbar nach dem Aufruf von zurückgegeben und generiert dann eine Reihe von **mewmdrmlicencbackupprogress** -Ereignissen, gefolgt von einem **mewmdrmlicenabcomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="16c27-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="16c27-128">Der Wert jedes **mewmdrmlicencbackupprogress** -Ereignisses, das durch Aufrufen von **imfmediaevent:: GetValue** abgerufen wird, ist ein **IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="16c27-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="16c27-129">Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle zum Abrufen einer Instanz der [**iwmdrmlicenanbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="16c27-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="16c27-130">Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="16c27-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="16c27-131">Nicht alle Lizenzen dürfen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="16c27-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="16c27-132">Diese Methode sichert nur Lizenzen, die dies zulassen.</span><span class="sxs-lookup"><span data-stu-id="16c27-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c27-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16c27-133">Requirements</span></span>



| <span data-ttu-id="16c27-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16c27-134">Requirement</span></span> | <span data-ttu-id="16c27-135">Wert</span><span class="sxs-lookup"><span data-stu-id="16c27-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16c27-136">Header</span><span class="sxs-lookup"><span data-stu-id="16c27-136">Header</span></span><br/>  | <dl> <span data-ttu-id="16c27-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="16c27-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="16c27-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16c27-138">Library</span></span><br/> | <dl> <span data-ttu-id="16c27-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16c27-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c27-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16c27-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c27-141">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="16c27-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





