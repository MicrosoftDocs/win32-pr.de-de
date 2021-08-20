---
description: Die SetMediaTimes-Methode legt die End- und Startzeiten des Mediums fest.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: IAMTimelineSrc::SetMediaTimes-Methode (Qedit.h)
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
ms.openlocfilehash: 5de058e31da605b96f7b013c03e9c0d020daa11ec676618b4a13f5ff92e701f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154926"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>IAMTimelineSrc::SetMediaTimes-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetMediaTimes` -Methode legt die End- und Startzeiten des Mediums fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Startzeit des Mediums in Einheiten von 100 Nanosekunden.

</dd> <dt>

*Beenden* 
</dt> <dd>

Medienstoppzeit in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Medienzeiten sind die Beendigungs- und Startzeiten relativ zur ursprünglichen Mediendatei. Legen Sie immer die Medienzeiten fest, wenn Sie der Zeitachse eine Video- oder Audioquelle hinzufügen. Andernfalls können Renderingprobleme auftreten. Die Beendigungszeit muss größer als die Startzeit sein.

Um einen Stillframe aus einer Videoquelle zu verwenden, legen Sie die Beendigungszeit auf einen Bruchteil mehr als die Startzeit fest, z. B. 100 Nanosekunden. Wenn sie auf den gleichen Wert festgelegt werden, wird ein Renderingfehler verursacht.

Wenn die Zeitachsendauer nicht mit der Mediendauer übereinstimmt, wird die Quelle entsprechend gestreckt oder verkleinert. Dies bewirkt, dass der Clip langsamer oder schneller als die erstellte Rate wiedergegeben wird. (Die Tonhöhenverschiebung erfolgt in einer Audioquelle.) Weitere Informationen finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Sie können die Dauer der Quelldatei angeben, indem Sie die [**SetMediaLength-Methode**](iamtimelinesrc-setmedialength.md) aufrufen. Wenn Sie eine Medienstoppzeit festlegen, die die Dauer überschreitet, schneidet DES die Beendigungszeit ab.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




