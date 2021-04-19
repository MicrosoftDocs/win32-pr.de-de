---
description: Implementieren von IWICBitmapCodecProgressNotification (Decoder)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementieren von IWICBitmapCodecProgressNotification (Decoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362513"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="aa4d5-103">Implementieren von IWICBitmapCodecProgressNotification (Decoder)</span><span class="sxs-lookup"><span data-stu-id="aa4d5-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="aa4d5-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="aa4d5-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="aa4d5-105">Wenn ein Codec einen e/a-Vorgang ausführt, z. b. [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) in einem großen Bild, kann es mehrere Sekunden oder sogar Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="aa4d5-106">Wenn Endbenutzer einen Vorgang mit langer Ausführungszeit nicht unterbrechen können, kann die Anwendung davon ausgehen, dass die Anwendung nicht reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="aa4d5-107">Benutzer werden häufig eine Anwendung schließen oder sogar Ihre Computer neu starten, um die Kontrolle über den Computer wiederherzustellen, wenn eine Anwendung nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="aa4d5-108">Diese Schnittstelle ermöglicht es einer Anwendung, eine Rückruffunktion anzugeben, die der Codec in angegebenen Intervallen aufzurufen kann, um den Aufrufer über den Fortschritt des aktuellen Vorgangs zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="aa4d5-109">Die Anwendung kann mithilfe dieser Rückruffunktion einen Hinweis auf den Fortschritt in der Benutzeroberfläche anzeigen, um den Benutzer über den Status des Vorgangs zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="aa4d5-110">Wenn ein **Benutzer im Status Dialogfeld** auf die Schaltfläche **Abbrechen** klickt, gibt die Anwendung den von der Rückruffunktion **\_ \_ abgebrochenen wincodec Err** zurück.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="aa4d5-111">Wenn dies der Fall ist, muss der Codec den angegebenen Vorgang abbrechen und dieses **HRESULT** zurück an den Aufrufer der Methode übergeben, die den Vorgang durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="aa4d5-112">Diese Schnittstelle sollte in Ihrer Decoder-Klasse auf Container-Ebene implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="aa4d5-113">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="aa4d5-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="aa4d5-114">PfnProgressNotification</span><span class="sxs-lookup"><span data-stu-id="aa4d5-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="aa4d5-115">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="aa4d5-115">RegisterProgressNotification</span></span>

<span data-ttu-id="aa4d5-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) wird von einer Anwendung aufgerufen, um eine Rückruffunktion zu registrieren, die der Codec in angegebenen Intervallen aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="aa4d5-117">Der erste Parameter, *pfnProgressNotification*, ist ein Zeiger auf die Rückruffunktion, die der Codec in regelmäßigen Abständen aufrufen sollte.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="aa4d5-118">Der *pvData* -Parameter verweist auf ein Objekt, das der Codec an die Rückruffunktion zurückgeben soll, wenn die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="aa4d5-119">Dieses Objekt kann überhaupt alles sein und hat keine besondere Bedeutung für den Codec.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="aa4d5-120">Der *dwprogressflags* -Parameter gibt an, wann der Codec die Rückruffunktion aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="aa4d5-121">Eine-oder-Funktion kann mit zwei Enumerationen für diesen Parameter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="aa4d5-122">Die [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) -Enumeration gibt an, ob die Rückruffunktion während der Decodierung (**WICProgressOperationCopyPixels**), Codierung (**wicprogerssoperationschreitepixel**) oder beides (**WICProgressOperationAll**) aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="aa4d5-123">Der Codec sollte die Rückruffunktion in regelmäßigen Abständen während des Vorgangs aufzurufen, aber der Aufrufer kann bestimmte Anforderungen angeben.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="aa4d5-124">Die [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) -Enumeration gibt an, an welchem Punkt des Vorgangs die Rückruffunktion aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="aa4d5-125">Wenn der Aufrufer **WICProgressNotificationBegin** angibt, muss er am Anfang des Vorgangs (0,0) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="aa4d5-126">Wenn der Aufrufer diese Angabe nicht angibt, ist er optional.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="aa4d5-127">Wenn der Aufrufer **wicprogerssnotificationend** angibt, müssen Sie ihn ebenso angeben, wenn der Vorgang abgeschlossen ist (1,0).</span><span class="sxs-lookup"><span data-stu-id="aa4d5-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="aa4d5-128">Wenn der Aufrufer **WICProgressNotificationAll** angibt, müssen Sie ihn am Anfang und am Ende sowie in regelmäßigen Abständen während des Vorgangs ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="aa4d5-129">Der Aufrufer kann auch **wicprogerssnotificationfrequent** angeben. Dies deutet darauf hin, dass Sie in regelmäßigen Abständen (möglicherweise nach jedem Paar Scan Zeilen) wieder aufgerufen werden möchten.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="aa4d5-130">(Ein Aufrufer verwendet dieses Flag in der Regel nur für ein sehr großes Bild.) Andernfalls sollten Sie in der Regel einen Rückruf in Intervallen von ungefähr 10 Prozent der Gesamtzahl der zu verarbeitenden Scan Zeilen durchgehen.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="aa4d5-131">Für einen bestimmten Decoder oder eine Encoder-Instanz kann jeweils nur eine Rückruffunktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="aa4d5-132">Wenn eine Anwendung [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) mehrmals aufruft, ersetzen Sie die zuvor registrierte Rückruffunktion durch die neue.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="aa4d5-133">Um eine Rückruf Registrierung abzubrechen, legt ein Aufrufer den *pfnProgressNotification* -Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="aa4d5-134">PfnProgressNotification</span><span class="sxs-lookup"><span data-stu-id="aa4d5-134">PFNProgressNotification</span></span>

<span data-ttu-id="aa4d5-135">[**PfnProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) ist die Rückruffunktion mit der folgenden Signatur.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="aa4d5-136">Wenn Sie die Rückruffunktion aufrufen, verwenden Sie den *pvData* -Parameter, um dieselben *pvData* zurückzugeben, die von der Anwendung beim Registrieren der Rückruffunktion angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="aa4d5-137">Der *uFrameNum* -Parameter sollte den Index des Frame angeben, der verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="aa4d5-138">Legen Sie den Vorgangs Parameter auf **WICProgressOperationCopyPixels** fest, wenn Sie decodieren und **wicprogressoperationwrite tepixel** bei der Codierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="aa4d5-139">Der *dblProgress* -Parameter muss eine Zahl zwischen 0,0 (Beginn des Vorgangs) und 1,0 (der Abschluss des Vorgangs) sein.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="aa4d5-140">Der Wert sollte den Anteil der bereits verarbeiteten Scan Zeilen im Verhältnis zur Gesamtzahl der zu verarbeitenden Scan Zeilen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="aa4d5-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa4d5-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa4d5-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aa4d5-142">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="aa4d5-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa4d5-143">**Progressnotificationcallback**</span><span class="sxs-lookup"><span data-stu-id="aa4d5-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="aa4d5-144">**IWICBitmapCodecProgressNotification**</span><span class="sxs-lookup"><span data-stu-id="aa4d5-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="aa4d5-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="aa4d5-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aa4d5-146">Implementieren von IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="aa4d5-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="aa4d5-147">Implementieren von IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="aa4d5-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="aa4d5-148">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="aa4d5-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="aa4d5-149">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="aa4d5-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



