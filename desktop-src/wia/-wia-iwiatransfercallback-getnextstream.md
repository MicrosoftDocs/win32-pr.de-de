---
description: Ruft einen neuen Stream für das angegebene Element ab.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Iwiatransfercallback:: getnextstream-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356776"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="a7893-103">Iwiatransfercallback:: getnextstream-Methode</span><span class="sxs-lookup"><span data-stu-id="a7893-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="a7893-104">Ruft einen neuen Stream für das angegebene Element ab.</span><span class="sxs-lookup"><span data-stu-id="a7893-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7893-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7893-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="a7893-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7893-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7893-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7893-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="a7893-108">Type: **LONG**</span></span>

<span data-ttu-id="a7893-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7893-109">Currently unused.</span></span> <span data-ttu-id="a7893-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7893-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-111">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7893-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7893-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a7893-112">Type: **BSTR**</span></span>

<span data-ttu-id="a7893-113">Gibt den Namen des Elements an, für das der Stream erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7893-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-114">*bstraufullitemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7893-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7893-115">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a7893-115">Type: **BSTR**</span></span>

<span data-ttu-id="a7893-116">Gibt den vollständigen Namen des Elements an, für das der Stream erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7893-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-117">*ppdestination* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7893-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7893-118">Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="a7893-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="a7893-119">Empfängt die Adresse eines Zeigers auf das neue [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7893-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7893-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7893-120">Return value</span></span>

<span data-ttu-id="a7893-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7893-121">Type: **HRESULT**</span></span>

<span data-ttu-id="a7893-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7893-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7893-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7893-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7893-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7893-124">Remarks</span></span>

<span data-ttu-id="a7893-125">Wenn diese Methode von einem Bild Verarbeitungs Filter implementiert wird, ruft der Windows-Abbild Erfassungs Dienst (WIA) 2,0 Mini Treiber ihn während der Abbild Erfassung auf, um den Zielstream vom Client zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7893-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="a7893-126">**Iwiatransfercallback:: getnextstream** eines Filters muss an die Rückruf Methode der Anwendung delegieren.</span><span class="sxs-lookup"><span data-stu-id="a7893-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="a7893-127">Der Filter verwendet den Datenstrom, der von der **iwiatransfercallback:: getnextstream** -Implementierung des Anwendungs Rückrufs zurückgegeben wurde, um einen eigenen Stream zu erstellen, der an den WIA 2,0-Dienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a7893-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="a7893-128">Die Filterung erfolgt, wenn der Datenstrom des Filters die [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="a7893-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="a7893-129">Der Stream des Filters kann keine Annahmen über die Anzahl der Bytes machen, die bei jedem Schreibvorgang in ihn geschrieben werden, da die ungefilterten Image Daten möglicherweise von der WIA 2,0-Vorschau Komponente und nicht vom Treiber stammen.</span><span class="sxs-lookup"><span data-stu-id="a7893-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="a7893-130">Die WIA 2,0-Vorschau Komponente schreibt die gesamten ungefilterten Bild Daten immer nur einmal in den Stream des Filters, was bedeutet, dass der Stream des Filters eine Quelle in Sie schreibt.</span><span class="sxs-lookup"><span data-stu-id="a7893-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="a7893-131">Wenn sowohl der Treiber als auch die Vorschau Komponente in den Datenstrom des Filters schreiben, kann der streamingstream nicht davon ausgehen, dass er den vollständigen Header erhält, wenn [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) das erste Mal aufgerufen wird, obwohl der entsprechende Treiber immer zuerst die Header Daten in einem Schreibvorgang schreibt.</span><span class="sxs-lookup"><span data-stu-id="a7893-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="a7893-132">Es kann auch nicht davon ausgegangen werden, dass ein nachfolgender Schreibvorgang genau eine Scan Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="a7893-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="a7893-133">Der Filterungs Datenstrom muss also möglicherweise die Anzahl der zu schreibenden Bytes zählen, um z. b. zu ermitteln, wo die Bilddaten gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a7893-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="a7893-134">Die **iwiatransfercallback:: getnextstream** -Implementierung des Bild Verarbeitungs Filters sollte die Eigenschaften lesen, die für die Bildverarbeitung von dem Element benötigt werden, für das das Image abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a7893-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="a7893-135">Der Filter liest die Eigenschaften nicht direkt aus dem *pWiaItem2* , der in [**initializefilter**](-wia-iwiaimagefilter-initializefilter.md)übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="a7893-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="a7893-136">Stattdessen muss der Filter [**finditembyname**](-wia-iwiaitem2-finditembyname.md) für dieses WIA 2,0-Element aufrufen, um das tatsächliche WIA 2,0-Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7893-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="a7893-137">Der Grund hierfür ist, dass das abgerufene Image tatsächlich ein untergeordnetes Element von *pWiaItem2* sein kann.</span><span class="sxs-lookup"><span data-stu-id="a7893-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="a7893-138">Beispielsweise verwendet der Filter während einer Ordner Erfassung *pWiaItem2* , um die untergeordneten Elemente von *pWiaItem2* in **iwiatransfercallback:: getnextstream** abzurufen (während der Ordner Erfassung gibt der Treiber die Bilder zurück, die von den untergeordneten Elementen von *pWiaItem2* dargestellt werden).</span><span class="sxs-lookup"><span data-stu-id="a7893-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="a7893-139">Dasselbe gilt, wenn die WIA 2,0-Vorschau Komponente den Bild Verarbeitungs Filter aufruft, indem ein untergeordnetes WIA 2,0-Element übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a7893-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7893-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7893-140">Requirements</span></span>



| <span data-ttu-id="a7893-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7893-141">Requirement</span></span> | <span data-ttu-id="a7893-142">Wert</span><span class="sxs-lookup"><span data-stu-id="a7893-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7893-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7893-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a7893-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7893-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a7893-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7893-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a7893-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7893-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a7893-147">Header</span><span class="sxs-lookup"><span data-stu-id="a7893-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7893-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7893-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="a7893-149">IDL</span><span class="sxs-lookup"><span data-stu-id="a7893-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7893-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7893-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="a7893-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7893-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7893-152"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7893-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
