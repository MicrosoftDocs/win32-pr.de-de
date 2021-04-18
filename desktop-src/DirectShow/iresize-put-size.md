---
description: Die Put \_ size-Methode legt die Ausgabegröße und den streckungs Modus fest.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: Iresize::p ut_Size-Methode (qedit. h)
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
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368378"
---
# <a name="iresizeput_size-method"></a>Iresize::p UT \_ size-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `put_Size` -Methode legt die Ausgabegröße und den streckungs Modus fest.

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

*Höhe* \[ in\]
</dt> <dd>

Die Höhe des Videos in Pixel.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Die Breite des Videos in Pixel.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Der streckungs Modus. Informationen zu möglichen Werten finden Sie unter [**Größenänderung für Flags**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

DES kann diese Methode vor oder nach dem Aufruf von **Put \_ mediaType** aufrufen. Wenn des auf diese Methode vor dem Aufruf von **Put \_ mediaType** aufruft, sollte der Filter einen Standardwert für die Bittiefe auswählen und die Größen Werte zum Erstellen eines Ausgabemedien Typs verwenden. Wenn des nach dem Aufruf von **Put \_ mediaType** diese Methode aufruft, sollte der Filter seinen aktuellen Ausgabetyp mit den neuen Größen ändern.

Des kann diese Methode auch nach der Verbindungs Herstellung der Ausgabe-PIN aufruft. Ändern Sie in diesem Fall den Ausgabetyp, und verbinden Sie die Ausgabe-PIN erneut mit dem neuen Typ. Weitere Informationen finden Sie unter Wiederherstellen einer [Verbindung mit Pins](reconnecting-pins.md) .

Der *Flags* -Parameter gibt an, wie der Filter den Vorgang zum Ändern der Größe ausführen soll.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**Iresize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




