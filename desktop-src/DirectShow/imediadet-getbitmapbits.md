---
description: Die GetBitmapBits-Methode ruft einen Videoframe zur angegebenen Medienzeit ab. Der zurückgegebene Frame hat immer das 24-Bit-RGB-Format.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: IMediaDet::GetBitmapBits-Methode (Qedit.h)
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
ms.openlocfilehash: 5c4a7332580d4e9a9fece5a66d390753566fbf54c615699663256c463cb401b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792000"
---
# <a name="imediadetgetbitmapbits-method"></a>IMediaDet::GetBitmapBits-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetBitmapBits` -Methode ruft einen Videoframe zur angegebenen Medienzeit ab. Der zurückgegebene Frame hat immer das 24-Bit-RGB-Format.

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

*StreamTime* 
</dt> <dd>

Zeit, zu der der Videoframe abgerufen werden soll (in Sekunden).

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Empfängt die erforderliche Puffergröße. Wenn *pBuffer* **NULL** ist, empfängt die Variable die Größe des Puffers, der zum Abrufen des Frames erforderlich ist. Wenn *pBuffer* nicht **NULL** ist, wird dieser Parameter ignoriert.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen Puffer, der eine [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) gefolgt von den DIB-Bits empfängt.

</dd> <dt>

*Width* 
</dt> <dd>

Breite des Videobilds in Pixel.

</dd> <dt>

*Height* 
</dt> <dd>

Höhe des Videobilds in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                             | Beschreibung                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | Der Sample [**Grabber-Filter**](sample-grabber-filter.md) konnte dem Diagramm nicht hinzugefügt werden.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Nicht genügend Arbeitsspeicher.<br/>                                                                   |
| <dl> <dt>**E \_ POINTER**</dt> </dl>               | **NULL-Zeigerfehler.**<br/>                                                                |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | Unerwarteter Fehler.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Ungültiger Medientyp.<br/>                                                                    |



 

## <a name="remarks"></a>Hinweise

Legen Sie vor dem Aufrufen dieser Methode den Dateinamen und den Stream fest, indem [**Sie IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) und [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md)aufrufen.

Um die Erforderliche Puffergröße zu bestimmen, rufen Sie diese Methode mit *pBuffer* gleich **NULL** auf. Die Größe wird in der Variablen zurückgegeben, auf die *pBufferSize* zeigt. Erstellen Sie dann den Puffer, und rufen Sie die -Methode erneut auf, wobei *pBuffer* der Adresse des Puffers entspricht. Wenn die Methode zurückgegeben wird, enthält der Puffer eine **BITMAPINFOHEADER-Struktur** gefolgt von der Bitmap. Die Bitmap wird auf die Dimensionen skaliert, die in den Parametern *Width* und *Height* angegeben sind.

Diese Methode versetzt die Medienerkennung in den Bitmapgrabbermodus. Nachdem diese Methode aufgerufen wurde, funktionieren die verschiedenen Streaminformationsmethoden in **IMediaDet** nicht mehr, es sei denn, Sie erstellen eine neue Instanz der Medienerkennung.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




