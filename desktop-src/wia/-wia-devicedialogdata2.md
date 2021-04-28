---
description: 'DEVICEDIALOGDATA2-Struktur: Definiert die Daten, die zum Aufrufen eines Gerätedialogs erforderlich sind.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: DEVICEDIALOGDATA2-Struktur (Wiadefd.h)
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
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089804"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="a2fee-103">DEVICEDIALOGDATA2-Struktur</span><span class="sxs-lookup"><span data-stu-id="a2fee-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="a2fee-104">Definiert die Daten, die zum Aufrufen eines Gerätedialogfelds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a2fee-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2fee-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a2fee-106">Member</span><span class="sxs-lookup"><span data-stu-id="a2fee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2fee-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a2fee-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2fee-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-109">Gibt die Größe dieser Struktur in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="a2fee-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="a2fee-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-111">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2fee-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-112">Zeigt auf eine [**IWiaItem2-Schnittstelle,**](-wia-iwiaitem2.md) die das gültige Stammelement in der Anwendungselementstruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fee-112">Points to an [**IWiaItem2**](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="a2fee-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2fee-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-115">Gibt einen Satz von Flags an, die den Vorgang des Dialogfelds steuern.</span><span class="sxs-lookup"><span data-stu-id="a2fee-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="a2fee-116">Kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a2fee-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="a2fee-117">Flag</span><span class="sxs-lookup"><span data-stu-id="a2fee-117">Flag</span></span>                                 | <span data-ttu-id="a2fee-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a2fee-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fee-119">0</span><span class="sxs-lookup"><span data-stu-id="a2fee-119">0</span></span>                                    | <span data-ttu-id="a2fee-120">Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="a2fee-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="a2fee-121">\_WIA-GERÄTEDIALOGFELD \_ \_ – \_ EINZELNES IMAGE</span><span class="sxs-lookup"><span data-stu-id="a2fee-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="a2fee-122">Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld "Gerätebilderfassung".</span><span class="sxs-lookup"><span data-stu-id="a2fee-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="a2fee-123">DIALOGFELD \_ "WIA-GERÄT" \_ VERWENDEN DER ALLGEMEINEN \_ \_ \_ BENUTZEROBERFLÄCHE</span><span class="sxs-lookup"><span data-stu-id="a2fee-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="a2fee-124">Verwenden Sie die Systembenutzeroberfläche (falls verfügbar) anstelle der vom Anbieter bereitgestellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a2fee-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="a2fee-125">Wenn die Systembenutzeroberfläche nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2fee-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="a2fee-126">Wenn keine der Benutzeroberflächen verfügbar ist, gibt die Funktion E \_ NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="a2fee-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a2fee-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="a2fee-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-128">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="a2fee-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-129">Gibt das Handle für das übergeordnete Fenster des Dialogfelds an.</span><span class="sxs-lookup"><span data-stu-id="a2fee-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="a2fee-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-131">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a2fee-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-132">Gibt den Ordnernamen an, an den die Dateien übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="a2fee-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="a2fee-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-134">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a2fee-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-135">Gibt die Dateinamenvorlage an, die für Dateien verwendet werden soll, die von WIA-Elementen in den durch **bstrFolderName festgelegten Zielordner übertragen werden.**</span><span class="sxs-lookup"><span data-stu-id="a2fee-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="a2fee-136">Eine beliebige Anzahl eindeutiger Dateinamen kann durch Anfügen zusätzlicher Zeichen an die Dateinamenvorlage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fee-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="a2fee-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-138">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="a2fee-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-139">Empfängt die Anzahl der Zeichenfolgen, die in das **pbstrFilePaths-Array geschrieben** werden.</span><span class="sxs-lookup"><span data-stu-id="a2fee-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="a2fee-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-141">Typ: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="a2fee-141">Type: **BSTR\***</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-142">Zeiger auf ein Array von BSTR-Zeigern.</span><span class="sxs-lookup"><span data-stu-id="a2fee-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="a2fee-143">Jedes Arrayelement verweist auf einen BSTR, der den Zielnamen einer Datei enthält, die erfolgreich in den durch bstrFolderName identifizierten Ordner übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="a2fee-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="a2fee-144">Die -Methode muss den Speicher für diesen Member zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a2fee-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="a2fee-145">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="a2fee-145">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="a2fee-146">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2fee-146">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="a2fee-147">Zeiger auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des WIA-Elements, das Daten in die Datei oder dateien überträgt, die im **pbstrFilePaths-Array benannt** sind.</span><span class="sxs-lookup"><span data-stu-id="a2fee-147">Pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2fee-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2fee-148">Requirements</span></span>



| <span data-ttu-id="a2fee-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2fee-149">Requirement</span></span> | <span data-ttu-id="a2fee-150">Wert</span><span class="sxs-lookup"><span data-stu-id="a2fee-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fee-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2fee-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fee-152">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2fee-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a2fee-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2fee-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fee-154">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2fee-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2fee-155">Header</span><span class="sxs-lookup"><span data-stu-id="a2fee-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fee-156"><dt>Wiadefd.h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fee-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




