---
description: Wenn der Windows Media Audio Encoder Ausgabetypen auflistet, identifiziert er jeden enumerierten Typ als Standard, Professional oder verlustfrei.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Konfigurieren von Standard-, Professional-oder Verlust loser Audiocodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749336"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="8a39a-103">Konfigurieren von Standard-, Professional-oder Verlust loser Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="8a39a-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="8a39a-104">Wenn der Windows Media Audio Encoder Ausgabetypen auflistet, identifiziert er jeden enumerierten Typ als Standard, Professional oder verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="8a39a-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="8a39a-105">Mithilfe der folgenden Schritte können Sie ermitteln, ob ein Ausgabetyp "Standard", "Professional" oder "Verlustfrei" ist.</span><span class="sxs-lookup"><span data-stu-id="8a39a-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="8a39a-106">Rufen Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle zu erhalten, die den Ausgabetyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="8a39a-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="8a39a-107">Wenn Sie [**imfmediatype:: getrepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) aufzurufen, wird eine [**am- \_ Medientyp \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur mit Informationen zum Ausgabetyp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a39a-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="8a39a-108">Der **pbformat** -Member der [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur verweist auf eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur, die zusätzliche Informationen über den Ausgabetyp enthält.</span><span class="sxs-lookup"><span data-stu-id="8a39a-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="8a39a-109">Überprüfen Sie den **wformattag** -Member der **WaveFormatEx** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8a39a-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="8a39a-110">Der Wert 0x161 weist auf Standard, der Wert 0x162 den Wert Professional und der Wert 0x163 auf Verlust lose Werte hin.</span><span class="sxs-lookup"><span data-stu-id="8a39a-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="8a39a-111">Wenn Sie Eigenschaften für den Windows Media Audio Encoder festlegen, bevor Sie die Ausgabetypen aufzählen, können Sie die Anzahl der aufgelisteten Ausgabetypen einschränken.</span><span class="sxs-lookup"><span data-stu-id="8a39a-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="8a39a-112">Wenn Sie z. b. die VBR-Eigenschaften entsprechend festgelegt haben, können Sie die Enumerationstypen auf diejenigen beschränken, die sich in der Kategorie verlustfreie Elemente befinden.</span><span class="sxs-lookup"><span data-stu-id="8a39a-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="8a39a-113">Standard-Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="8a39a-113">Standard Audio Encoding</span></span>

<span data-ttu-id="8a39a-114">Mit den folgenden Schritten können Sie die Standard mäßige Audiocodierung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8a39a-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="8a39a-115">Legen Sie die Eigenschaften Ihrer Wahl für den Encoder fest.</span><span class="sxs-lookup"><span data-stu-id="8a39a-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="8a39a-116">Listet die möglichen Ausgabetypen auf.</span><span class="sxs-lookup"><span data-stu-id="8a39a-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="8a39a-117">Überprüfen Sie die Enumerationstypen, und wählen Sie eine aus, die über das audioformattag 0x161 verfügt.</span><span class="sxs-lookup"><span data-stu-id="8a39a-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="8a39a-118">Legen Sie den Ausgabetyp auf den ausgewählten Typ fest, indem Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8a39a-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="8a39a-119">Professionelle Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="8a39a-119">Professional Audio Encoding</span></span>

<span data-ttu-id="8a39a-120">Mit den folgenden Schritten können Sie die professionelle Audiocodierung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8a39a-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="8a39a-121">Legen Sie die Eigenschaften Ihrer Wahl für den Encoder fest.</span><span class="sxs-lookup"><span data-stu-id="8a39a-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="8a39a-122">Listet die möglichen Ausgabetypen auf.</span><span class="sxs-lookup"><span data-stu-id="8a39a-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="8a39a-123">Überprüfen Sie die Enumerationstypen, und wählen Sie eine aus, die über das audioformattag 0x162 verfügt.</span><span class="sxs-lookup"><span data-stu-id="8a39a-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="8a39a-124">Legen Sie den Ausgabetyp auf den ausgewählten Typ fest, indem Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8a39a-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="8a39a-125">Verlustfreie Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="8a39a-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="8a39a-126">Mithilfe der folgenden Schritte können Sie eine verlustfreie Audiocodierung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8a39a-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="8a39a-127">Legen Sie die Eigenschaft " [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) " auf " **Variant \_ true**" fest.</span><span class="sxs-lookup"><span data-stu-id="8a39a-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="8a39a-128">Legen Sie die Eigenschaft [**\_ \_ \_ vbrquality für mfpkey-Einschränkung**](mfpkey-constrain-enumerated-vbrqualityproperty.md) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="8a39a-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="8a39a-129">Legen Sie die [**\_ gewünschte \_ vbrquality-Eigenschaft für mfpkey**](mfpkey-desired-vbrqualityproperty.md) auf 100 fest.</span><span class="sxs-lookup"><span data-stu-id="8a39a-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="8a39a-130">Listet Ausgabetypen auf.</span><span class="sxs-lookup"><span data-stu-id="8a39a-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="8a39a-131">Legen Sie den Ausgabetyp auf einen der in Schritt 4 aufgezählten Typen fest, indem Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8a39a-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="8a39a-132">Der folgende Code listet alle verlustfreien Ausgabetypen für den Windows Media Audio Encoder auf.</span><span class="sxs-lookup"><span data-stu-id="8a39a-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="8a39a-133">Der Code druckt den Wert des audioformattags für jeden enumerierten Typ.</span><span class="sxs-lookup"><span data-stu-id="8a39a-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="8a39a-134">Da alle Enumerationstypen verlustfrei sind, haben alle diese Format Tags den Wert 0x163.</span><span class="sxs-lookup"><span data-stu-id="8a39a-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="8a39a-135">Angenommen, "pimt" ist ein Zeiger auf eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle in einem Windows Media Audio Encoder-Objekt, und pstore ist ein Zeiger auf eine **IPropertyStore** -Schnittstelle für das gleiche Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a39a-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="8a39a-136">Nehmen Sie auch an, dass HR eine Variable vom Typ **HRESULT** ist, die zuvor im Code deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="8a39a-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a><span data-ttu-id="8a39a-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a39a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a39a-138">Konfigurieren der Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="8a39a-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
