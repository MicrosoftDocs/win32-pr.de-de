---
description: Die setmediatimes-Methode legt die Start-und Startzeiten des Mediums fest.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Iamtimelinesrc:: setmediatimes-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360921"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>Iamtimelinesrc:: setmediatimes-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetMediaTimes` -Methode legt die Start-und Startzeiten des Mediums fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* 
</dt> <dd>

Start Zeit der Medien in 100-Nanosecond-Einheiten.

</dd> <dt>

*Beenden* 
</dt> <dd>

Endzeit der Medien in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Medien Zeiten sind die Beendigung und Startzeiten in Relation zur ursprünglichen Mediendatei. Legen Sie die Medien Zeiten immer fest, wenn Sie der Zeitachse ein Video oder eine Audioquelle hinzufügen. Andernfalls können Renderingprobleme auftreten. Die Endzeit muss nach der Startzeit liegen.

Wenn Sie einen immer noch Frame aus einer Videoquelle verwenden möchten, legen Sie für die Endzeit einen größeren Wert als die Startzeit fest, z. b. 100 Nanosekunden. Wenn Sie auf denselben Wert festlegen, wird ein Renderingfehler verursacht.

Wenn die Zeitachsen Dauer nicht der Medien Dauer entspricht, wird die Quelle entsprechend gestreckt oder verkleinert. Dies bewirkt, dass der Clip langsamer oder schneller als die erstellte Rate abgespielt wird. (In einer Audioquelle tritt die Verschiebung der Tonhöhe auf.) Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).

Sie können die Dauer der Quelldatei angeben, indem Sie die [**setmedialength**](iamtimelinesrc-setmedialength.md) -Methode aufrufen. Wenn Sie eine Zeit für das Medien Ende festlegen, die die Dauer überschreitet, verkürzt des die Endzeit.

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




