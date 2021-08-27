---
description: Wenn der Windows Media Audio-Encoder Ausgabetypen aufzählt, identifiziert er jeden aufzählbaren Typ entweder als Standard, Professional oder Als verlustfrei.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Konfigurieren der Standard-, Professional- oder verlustfreien Audiocodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa4184af8bc6b83710a3710ac1a278de71de0b7221dc11757bdeba46af8c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743537"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Konfigurieren der Standard-, Professional- oder verlustfreien Audiocodierung

Wenn der Windows Media Audio-Encoder Ausgabetypen aufzählt, identifiziert er jeden aufzählbaren Typ entweder als Standard, Professional oder Als verlustfrei. Sie können ermitteln, ob ein Ausgabetyp Standard, Professional oder Lossless ist, indem Sie die folgenden Schritte ausführen.

1.  Rufen Sie [**ÜBERTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine [**INTERFACESMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) abzurufen, die den Ausgabetyp darstellt.
2.  Rufen Sie [**ÜBERMEDIATYPE::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) auf, um eine [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) abzurufen, die Informationen zum Ausgabetyp enthält.
3.  Der **pbFormat-Member** der [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) zeigt auf eine [**WAVEFORMATEX-Struktur,**](/previous-versions/dd757713(v=vs.85)) die zusätzliche Informationen zum Ausgabetyp enthält. Überprüfen Sie den **wFormatTag-Member** der **WAVEFORMATEX-Struktur.** Der Wert 0x161 steht für Standard, der Wert 0x162 für Professional und der Wert 0x163 für Lossless.

Wenn Sie Eigenschaften für den Windows Media Audio-Encoder festlegen, bevor Sie Ausgabetypen auflisten, können Sie die Anzahl der aufgezählten Ausgabetypen begrenzen. Wenn Sie z. B. die VBR-Eigenschaften entsprechend festlegen, können Sie die aufzählten Ausgabetypen auf diejenigen beschränken, die sich in der Kategorie Verlustlos befinden.

## <a name="standard-audio-encoding"></a>Standardaudiocodierung

Sie können die folgenden Schritte ausführen, um die Standardaudiocodierung zu konfigurieren.

1.  Legen Sie die Eigenschaften Ihrer Wahl für den Encoder fest.
2.  Aufzählen der möglichen Ausgabetypen.
3.  Überprüfen Sie die aufzählten Typen, und wählen Sie einen Typ aus, der über ein Audioformattag 0x161 verfügt.
4.  Legen Sie den Ausgabetyp auf den ausgewählten Typ fest, indem Sie [**ÜBERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

## <a name="professional-audio-encoding"></a>Professional Audiocodierung

Sie können die folgenden Schritte ausführen, um Professional Audiocodierung zu konfigurieren.

1.  Legen Sie die Eigenschaften Ihrer Wahl für den Encoder fest.
2.  Aufzählen der möglichen Ausgabetypen.
3.  Überprüfen Sie die aufzählten Typen, und wählen Sie einen Typ aus, der über ein Audioformattag 0x162 verfügt.
4.  Legen Sie den Ausgabetyp auf den ausgewählten Typ fest, indem Sie [**ÜBERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

## <a name="lossless-audio-encoding"></a>Verlustfreie Audiocodierung

Sie können die folgenden Schritte ausführen, um die verlustfreie Audiocodierung zu konfigurieren.

1.  Legen Sie die [**MFPKEY \_ VBRENABLED-Eigenschaft**](mfpkey-vbrenabledproperty.md) auf **VARIANT \_ TRUE** fest.
2.  Legen Sie die [**EIGENSCHAFT MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) auf **VARIANT \_ TRUE** fest.
3.  Legen Sie die [**MFPKEY \_ DESIRED \_ VBRQUALITY-Eigenschaft**](mfpkey-desired-vbrqualityproperty.md) auf 100 fest.
4.  Aufzählen von Ausgabetypen.
5.  Legen Sie den Ausgabetyp auf einen der in Schritt 4 aufzählten Typen fest, indem Sie [**DEN TYPTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

Der folgende Code listet alle verlustfreien Ausgabetypen für den Windows Media Audio-Encoder auf. Der Code gibt den Wert des Audioformattags für jeden aufzählten Typ aus. Da alle aufzählbaren Typen verlustfrei sind, haben alle diese Formattags den Wert 0x163. Angenommen, pIMT ist ein Zeiger auf eine [**POINTERTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) auf einem Windows Media Audio-Encoderobjekt und pStore ist ein Zeiger auf eine **IPropertyStore-Schnittstelle** für dasselbe Objekt. Angenommen, hr ist eine Variable vom Typ **HRESULT,** die zuvor im Code deklariert wurde.


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

 

 
