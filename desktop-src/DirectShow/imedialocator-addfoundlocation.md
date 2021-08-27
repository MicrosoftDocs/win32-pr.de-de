---
description: Die AddFoundLocation-Methode fügt dem Verzeichniscache ein Verzeichnis hinzu.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: IMediaLocator::AddFoundLocation-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ba466338e6d148e3c39a6bed4f7db413ad444ee792a4fd49b6e1499f29f0403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051640"
---
# <a name="imedialocatoraddfoundlocation-method"></a>IMediaLocator::AddFoundLocation-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `AddFoundLocation` -Methode fügt dem Verzeichniscache ein Verzeichnis hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DirectoryName* 
</dt> <dd>

Verzeichnispfad, der dem Cache hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der Medienlocator speichert einen Cache von Verzeichnispfaden, in dem dateien in früheren Suchvorgängen erfolgreich gefunden wurden. Wenn eine Datei erfolgreich gefunden wird, wird das Verzeichnis dem Cache hinzugefügt.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaLocator-Schnittstelle**](imedialocator.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




