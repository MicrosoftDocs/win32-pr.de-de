---
description: Die Directory-Methode ruft eine Liste der Dateien des angegebenen Typs aus dem aktuellen Verzeichnis ab.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: Iscardfileaccess::D irectory-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864048"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="94b1e-103">Iscardfileaccess::D irectory-Methode</span><span class="sxs-lookup"><span data-stu-id="94b1e-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="94b1e-104">\[Die **Verzeichnis** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="94b1e-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="94b1e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94b1e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94b1e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="94b1e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="94b1e-107">Die **Directory** -Methode ruft eine Liste der Dateien des angegebenen Typs aus dem aktuellen Verzeichnis ab.</span><span class="sxs-lookup"><span data-stu-id="94b1e-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b1e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b1e-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="94b1e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="94b1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94b1e-110">*filetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94b1e-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b1e-111">Typ der aufzulistenden [*smartcarddateien*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="94b1e-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="94b1e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="94b1e-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="94b1e-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94b1e-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="94b1e-114"><dt>**SC \_ - \_ typverzeichnisse**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="94b1e-115">Nur Verzeichnis Dateien auflisten.</span><span class="sxs-lookup"><span data-stu-id="94b1e-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="94b1e-116"><dt>**SC \_ - \_ Typdateien**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="94b1e-117">Nur elementare Dateien auflisten.</span><span class="sxs-lookup"><span data-stu-id="94b1e-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="94b1e-118"><dt>**SC \_ Geben Sie \_ alle \_ Dateien ein.**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="94b1e-119">Auflisten von Verzeichnis-und elementaren Dateien</span><span class="sxs-lookup"><span data-stu-id="94b1e-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="94b1e-120"><dt>**SC \_ - \_ typverzeichnis \_ Datei**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="94b1e-121">Verzeichnis Datei.</span><span class="sxs-lookup"><span data-stu-id="94b1e-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="94b1e-122"><dt>**SC \_ Type \_ transparent \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="94b1e-123">Transparente elementare Datei.</span><span class="sxs-lookup"><span data-stu-id="94b1e-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="94b1e-124"><dt>**"SC \_ Type \_ Fixed \_ EF"**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="94b1e-125">Lineare, behobene elementare Datei.</span><span class="sxs-lookup"><span data-stu-id="94b1e-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="94b1e-126"><dt>**SC \_ Type \_ zyklische \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="94b1e-127">Zyklische elementare Datei.</span><span class="sxs-lookup"><span data-stu-id="94b1e-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="94b1e-128"><dt>**SC \_ - \_ Typvariable \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="94b1e-129">Lineare Variable (elementare Datei).</span><span class="sxs-lookup"><span data-stu-id="94b1e-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="94b1e-130">*ppfilelist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="94b1e-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94b1e-131">Array von bstrins, das die Liste der Dateien darstellt, die mit dem Spezifizierer in *filetype* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="94b1e-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94b1e-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94b1e-132">Return value</span></span>

<span data-ttu-id="94b1e-133">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="94b1e-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="94b1e-134">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="94b1e-134">Return code</span></span>                                                                                   | <span data-ttu-id="94b1e-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94b1e-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="94b1e-136"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="94b1e-137">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="94b1e-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="94b1e-138"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="94b1e-139">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="94b1e-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="94b1e-140"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="94b1e-141">Diese Methode wurde von der-Schnittstelle nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="94b1e-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="94b1e-142"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="94b1e-143">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="94b1e-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="94b1e-144"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="94b1e-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="94b1e-145">Für *ppfilelist* wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="94b1e-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="94b1e-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94b1e-146">Remarks</span></span>

<span data-ttu-id="94b1e-147">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="94b1e-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="94b1e-148">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="94b1e-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="94b1e-149">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="94b1e-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94b1e-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94b1e-150">Requirements</span></span>



| <span data-ttu-id="94b1e-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94b1e-151">Requirement</span></span> | <span data-ttu-id="94b1e-152">Wert</span><span class="sxs-lookup"><span data-stu-id="94b1e-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94b1e-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94b1e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="94b1e-154">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94b1e-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="94b1e-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94b1e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="94b1e-156">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94b1e-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="94b1e-157">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="94b1e-157">End of client support</span></span><br/>    | <span data-ttu-id="94b1e-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="94b1e-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="94b1e-159">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="94b1e-159">End of server support</span></span><br/>    | <span data-ttu-id="94b1e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="94b1e-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="94b1e-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94b1e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b1e-162">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="94b1e-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
