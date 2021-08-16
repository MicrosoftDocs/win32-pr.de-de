---
description: Die \_ put Size-Methode legt die Ausgabegröße und den Stretchmodus fest.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: IResize::p ut_Size-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d2da95cca7bf19182dd4c0f5f385715256ae9c5253c356094110c028fb1b016d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818130"
---
# <a name="iresizeput_size-method"></a>IResize::p ut \_ Size-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `put_Size` -Methode legt die Ausgabegröße und den Stretchmodus fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Höhe* \[ In\]
</dt> <dd>

Die Videohöhe in Pixel.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Die Videobreite in Pixel.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Der Stretchmodus. Mögliche Werte finden Sie unter Ändern der Größe von [**Flags.**](resize-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

DES kann diese Methode vor oder nach dem Aufruf von **put \_ MediaType** aufrufen. Wenn DES diese Methode vor dem Aufrufen von **put \_ MediaType** aufruft, sollte der Filter einen Standardwert für die Bittiefe auswählen und die Größenwerte verwenden, um einen Ausgabemedientyp zu erstellen. Wenn DES diese Methode nach dem Aufruf von **put \_ MediaType aufruft,** sollte der Filter seinen aktuellen Ausgabetyp mit den neuen Größen ändern.

DES kann diese Methode auch aufrufen, nachdem der Ausgabepin verbunden wurde. Ändern Sie in diesem Fall den Ausgabetyp, und verbinden Sie den Ausgabepin erneut mit dem neuen Typ. Weitere Informationen finden Sie unter [Erneutes Verbinden von Pins.](reconnecting-pins.md)

Der *Flags-Parameter* gibt an, wie der Filter den Größenänderungsvorgang ausführen soll.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9.0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IResize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




