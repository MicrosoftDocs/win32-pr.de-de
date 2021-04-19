---
description: Die enterbitmapgrabmode-Methode schaltet den Medien Detektor in den bitmapingmodus um und sucht das Filter Diagramm zu einem angegebenen Zeitpunkt.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Imediadet:: enterbitmapgrabmode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359382"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>Imediadet:: enterbitmapgrabmode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `EnterBitmapGrabMode` -Methode schaltet den Medien Detektor in den bitmapingmodus um und sucht das Filter Diagramm zu einem bestimmten Zeitpunkt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Streamtime* 
</dt> <dd>

Die Zeit (in Sekunden), die das Diagramm sucht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                             | Beschreibung                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>            | Ungültiges Argument.<br/>                             |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Die Quelldatei enthält keinen Videostream.<br/> |
| <dl> <dt>**VFW \_ E \_ Zeit \_ abgelaufen**</dt> </dl>    | Timeout beim Suchbefehl.<br/>                       |



 

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.

Mit dieser Methode wird der [**Sample Grabber**](sample-grabber-filter.md) Filter in das Filter Diagramm eingefügt. Sie können dann [**imediadet:: getsamplegrabber**](imediadet-getsamplegrabber.md) aufrufen, um einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle zu erhalten. Sobald der Medien Detektor in den bitmapingmodus wechselt, funktionieren die verschiedenen Informationsmethoden in **imediadet** nicht mehr.

Mit der [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) -Methode oder der [**imediadet:: Write-Bitmapbits**](imediadet-writebitmapbits.md) -Methode wird der Medien Detektor auch in den bitmapmodus versetzt.

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

 

 




