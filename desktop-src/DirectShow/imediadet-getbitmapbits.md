---
description: Die getbitmapbits-Methode ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab. Der zurückgegebene Frame weist immer das 24-Bit-RGB-Format auf.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Imediadet:: getbitmapbits-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371291"
---
# <a name="imediadetgetbitmapbits-method"></a>Imediadet:: getbitmapbits-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetBitmapBits` Methode ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab. Der zurückgegebene Frame weist immer das 24-Bit-RGB-Format auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Streamtime* 
</dt> <dd>

Der Zeitpunkt, zu dem der Videoframe abgerufen werden soll (in Sekunden).

</dd> <dt>

*pbuffersize* 
</dt> <dd>

Empfängt die erforderliche Puffergröße. Wenn *pbuffer* den Wert **null** hat, erhält die Variable die Größe des Puffers, der zum Abrufen des Frames benötigt wird. Wenn *pbuffer* nicht **null** ist, wird dieser Parameter ignoriert.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur gefolgt von den DIB-Bits empfängt.

</dd> <dt>

*Width* 
</dt> <dd>

Breite des Video Bilds in Pixel.

</dd> <dt>

*Height* 
</dt> <dd>

Höhe des Video Bilds in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                             | Beschreibung                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                                                               |
| <dl> <dt>**E \_ nointerface**</dt> </dl>           | Der [**Sample Grabber**](sample-grabber-filter.md) -Filter konnte dem Diagramm nicht hinzugefügt werden.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>           | Nicht genügend Arbeitsspeicher.<br/>                                                                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>               | **Null** -Zeiger Fehler.<br/>                                                                |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>            | Unerwarteter Fehler.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Ungültiger Medientyp.<br/>                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.

Um die Größe des erforderlichen Puffers zu bestimmen, müssen Sie diese Methode mit *pbuffer* gleich **null** aufzurufen. Die Größe wird in der Variablen zurückgegeben, auf die von *pbuffersize* verwiesen wird. Erstellen Sie dann den Puffer, und rufen Sie die Methode erneut auf, wobei *pbuffer* gleich der Adresse des Puffers ist. Wenn die Methode zurückgegeben wird, enthält der Puffer eine **BITMAPINFOHEADER** -Struktur gefolgt von der Bitmap. Die Bitmap wird auf die Dimensionen skaliert, die in den Parametern *Width* und *height* angegeben sind.

Mit dieser Methode wird der Medien Detektor in den bitmapingmodus versetzt. Nachdem diese Methode aufgerufen wurde, funktionieren die verschiedenen Datenstrom Informationsmethoden in **imediadet** nicht, es sei denn, Sie erstellen eine neue Instanz des Medien Detektors.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="examples"></a>Beispiele

Im folgenden Code wird die `GetBitmapBits` -Methode verwendet, um eine geräteunabhängige Bitmap zu erstellen.


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediadet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




