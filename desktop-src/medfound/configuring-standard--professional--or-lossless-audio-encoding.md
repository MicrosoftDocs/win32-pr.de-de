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
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Konfigurieren von Standard-, Professional-oder Verlust loser Audiocodierung

Wenn der Windows Media Audio Encoder Ausgabetypen auflistet, identifiziert er jeden enumerierten Typ als Standard, Professional oder verlustfrei. Mithilfe der folgenden Schritte können Sie ermitteln, ob ein Ausgabetyp "Standard", "Professional" oder "Verlustfrei" ist.

1.  Rufen Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle zu erhalten, die den Ausgabetyp darstellt.
2.  Wenn Sie [**imfmediatype:: getrepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) aufzurufen, wird eine [**am- \_ Medientyp \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur mit Informationen zum Ausgabetyp angezeigt.
3.  Der **pbformat** -Member der [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur verweist auf eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur, die zusätzliche Informationen über den Ausgabetyp enthält. Überprüfen Sie den **wformattag** -Member der **WaveFormatEx** -Struktur. Der Wert 0x161 weist auf Standard, der Wert 0x162 den Wert Professional und der Wert 0x163 auf Verlust lose Werte hin.

Wenn Sie Eigenschaften für den Windows Media Audio Encoder festlegen, bevor Sie die Ausgabetypen aufzählen, können Sie die Anzahl der aufgelisteten Ausgabetypen einschränken. Wenn Sie z. b. die VBR-Eigenschaften entsprechend festgelegt haben, können Sie die Enumerationstypen auf diejenigen beschränken, die sich in der Kategorie verlustfreie Elemente befinden.

## <a name="standard-audio-encoding"></a>Standard-Audiocodierung

Mit den folgenden Schritten können Sie die Standard mäßige Audiocodierung konfigurieren.

1.  Legen Sie die Eigenschaften Ihrer Wahl für den Encoder fest.
2.  Listet die möglichen Ausgabetypen auf.
3.  Überprüfen Sie die Enumerationstypen, und wählen Sie eine aus, die über das audioformattag 0x161 verfügt.
4.  Legen Sie den Ausgabetyp auf den ausgewählten Typ fest, indem Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

## <a name="professional-audio-encoding"></a>Professionelle Audiocodierung

Mit den folgenden Schritten können Sie die professionelle Audiocodierung konfigurieren.

1.  Legen Sie die Eigenschaften Ihrer Wahl für den Encoder fest.
2.  Listet die möglichen Ausgabetypen auf.
3.  Überprüfen Sie die Enumerationstypen, und wählen Sie eine aus, die über das audioformattag 0x162 verfügt.
4.  Legen Sie den Ausgabetyp auf den ausgewählten Typ fest, indem Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

## <a name="lossless-audio-encoding"></a>Verlustfreie Audiocodierung

Mithilfe der folgenden Schritte können Sie eine verlustfreie Audiocodierung konfigurieren.

1.  Legen Sie die Eigenschaft " [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) " auf " **Variant \_ true**" fest.
2.  Legen Sie die Eigenschaft [**\_ \_ \_ vbrquality für mfpkey-Einschränkung**](mfpkey-constrain-enumerated-vbrqualityproperty.md) auf **Variant \_ true** fest.
3.  Legen Sie die [**\_ gewünschte \_ vbrquality-Eigenschaft für mfpkey**](mfpkey-desired-vbrqualityproperty.md) auf 100 fest.
4.  Listet Ausgabetypen auf.
5.  Legen Sie den Ausgabetyp auf einen der in Schritt 4 aufgezählten Typen fest, indem Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

Der folgende Code listet alle verlustfreien Ausgabetypen für den Windows Media Audio Encoder auf. Der Code druckt den Wert des audioformattags für jeden enumerierten Typ. Da alle Enumerationstypen verlustfrei sind, haben alle diese Format Tags den Wert 0x163. Angenommen, "pimt" ist ein Zeiger auf eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle in einem Windows Media Audio Encoder-Objekt, und pstore ist ein Zeiger auf eine **IPropertyStore** -Schnittstelle für das gleiche Objekt. Nehmen Sie auch an, dass HR eine Variable vom Typ **HRESULT** ist, die zuvor im Code deklariert wurde.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Audiocodierung](configuringaudioencoding.md)
</dt> </dl>

 

 
