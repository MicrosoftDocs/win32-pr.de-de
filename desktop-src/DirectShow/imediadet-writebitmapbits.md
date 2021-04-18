---
description: Die "Write-Bitmapbits"-Methode ruft einen Video Frame zum angegebenen Zeitpunkt der Medien ab und schreibt ihn in eine Datei. Der Videoframe weist immer das 24-Bit-RGB-Format auf.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Imediadet:: Beschreib tebitmapbits-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352975"
---
# <a name="imediadetwritebitmapbits-method"></a>Imediadet:: schreitebitmapbits-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `WriteBitmapBits` -Methode ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab und schreibt ihn in eine Datei. Der Videoframe weist immer das 24-Bit-RGB-Format auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Streamtime* 
</dt> <dd>

Der Zeitpunkt, zu dem der Videoframe abgerufen werden soll.

</dd> <dt>

*Width* 
</dt> <dd>

Breite des Bilds in Pixel.

</dd> <dt>

*Height* 
</dt> <dd>

Höhe des Bilds in Pixel.

</dd> <dt>

*Filename* 
</dt> <dd>

Der Pfad der Datei, in der die Bitmap gespeichert werden soll. Wenn die Datei bereits vorhanden ist, wird Sie von dieser Methode überschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt. Folgende Fehlercodes sind möglich:



| Rückgabecode                                                                                             | Beschreibung                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ nointerface**</dt> </dl>           | Der [**Sample Grabber**](sample-grabber-filter.md) -Filter konnte dem Diagramm nicht hinzugefügt werden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                  | Fehler.<br/>                                                                               |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>           | Nicht genügend Arbeitsspeicher.<br/>                                                                   |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>            | Unerwarteter Fehler.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ AccessDenied**</dt> </dl>     | Datei kann nicht überschrieben werden.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Ungültiger Medientyp.<br/>                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.

Mit dieser Methode wird der Medien Detektor in den bitmapingmodus versetzt. Nachdem diese Methode aufgerufen wurde, funktionieren die verschiedenen Datenstrom Informationsmethoden in **imediadet** nicht, es sei denn, Sie erstellen eine neue Instanz des Medien Detektors.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

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

 

 




