---
description: Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: DEVICEDIALOGDATA2-Struktur (wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042283"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="f3860-103">DEVICEDIALOGDATA2-Struktur</span><span class="sxs-lookup"><span data-stu-id="f3860-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="f3860-104">Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f3860-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3860-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3860-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="f3860-106">Member</span><span class="sxs-lookup"><span data-stu-id="f3860-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3860-107">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="f3860-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f3860-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f3860-109">Gibt die Größe dieser Struktur in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="f3860-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-110">**piwiaitemroot**</span><span class="sxs-lookup"><span data-stu-id="f3860-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-111">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f3860-111">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

</dd> <dd>

<span data-ttu-id="f3860-112">Verweist auf eine [_ *IWiaItem2* \*](-wia-iwiaitem2.md) -Schnittstelle, die das gültige Stamm Element in der Anwendungs Elementstruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3860-112">Points to an [_ *IWiaItem2*\*](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="f3860-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f3860-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f3860-115">Gibt einen Satz von Flags an, die den Vorgang des Dialog Felds steuern.</span><span class="sxs-lookup"><span data-stu-id="f3860-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="f3860-116">Kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f3860-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="f3860-117">Flag</span><span class="sxs-lookup"><span data-stu-id="f3860-117">Flag</span></span>                                 | <span data-ttu-id="f3860-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f3860-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3860-119">0</span><span class="sxs-lookup"><span data-stu-id="f3860-119">0</span></span>                                    | <span data-ttu-id="f3860-120">Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="f3860-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="f3860-121">WIA- \_ Geräte \_ Dialogfeld, \_ einzelnes \_ Bild</span><span class="sxs-lookup"><span data-stu-id="f3860-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="f3860-122">Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld Geräte Abbild Erfassung.</span><span class="sxs-lookup"><span data-stu-id="f3860-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="f3860-123">Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f3860-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="f3860-124">Verwenden Sie die Benutzeroberfläche des Systems, falls verfügbar, anstelle der vom Hersteller bereitgestellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f3860-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="f3860-125">Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3860-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="f3860-126">Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="f3860-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f3860-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="f3860-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-128">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="f3860-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="f3860-129">Gibt das Handle für das übergeordnete Fenster des Dialog Felds an.</span><span class="sxs-lookup"><span data-stu-id="f3860-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-130">**bstrinfoldername**</span><span class="sxs-lookup"><span data-stu-id="f3860-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-131">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3860-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f3860-132">Gibt den Ordnernamen an, in den die Dateien übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="f3860-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="f3860-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-134">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3860-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f3860-135">Gibt die Dateinamen Vorlage an, die für Dateien verwendet werden soll, die von WIA-Elementen in den von **bstrindername** festgelegten Zielordner übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="f3860-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="f3860-136">Eine beliebige Anzahl eindeutiger Dateinamen kann erstellt werden, indem zusätzliche Zeichen an die Dateinamen Vorlage angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="f3860-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-137">**lnumfiles**</span><span class="sxs-lookup"><span data-stu-id="f3860-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-138">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="f3860-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="f3860-139">Empfängt die Anzahl der Zeichen folgen, die in das **pbstrfilepath** -Array geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f3860-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-140">**pbstraufilepfade**</span><span class="sxs-lookup"><span data-stu-id="f3860-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="f3860-141">Geben Sie Folgendes ein: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="f3860-141">Type: \**BSTR\** _</span></span>

</dd> <dd>

<span data-ttu-id="f3860-142">Zeiger auf ein Array von BSTR-Zeigern.</span><span class="sxs-lookup"><span data-stu-id="f3860-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="f3860-143">Jedes Array Element verweist auf ein BSTR, das den Zielnamen einer Datei enthält, die erfolgreich in den von bstrindername identifizierten Ordner übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="f3860-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="f3860-144">Die-Methode muss den Speicher für diesen Member zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f3860-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="f3860-145">_ *ppwiaitem*\*</span><span class="sxs-lookup"><span data-stu-id="f3860-145">_ *ppWiaItem*\*</span></span>
</dt> <dd>

<span data-ttu-id="f3860-146">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f3860-146">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

</dd> <dd>

<span data-ttu-id="f3860-147">Ein Zeiger auf die [_ *IWiaItem2* \*](-wia-iwiaitem2.md) -Schnittstelle des WIA-Elements, die Daten an die Datei oder die Dateien im **pbstrfilepath** -Array überträgt.</span><span class="sxs-lookup"><span data-stu-id="f3860-147">Pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3860-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3860-148">Requirements</span></span>



| <span data-ttu-id="f3860-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3860-149">Requirement</span></span> | <span data-ttu-id="f3860-150">Wert</span><span class="sxs-lookup"><span data-stu-id="f3860-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3860-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3860-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f3860-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3860-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f3860-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3860-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f3860-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3860-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3860-155">Header</span><span class="sxs-lookup"><span data-stu-id="f3860-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3860-156"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3860-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




