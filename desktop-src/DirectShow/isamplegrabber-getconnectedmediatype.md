---
description: Die getconnectedmediatype-Methode ruft den Medientyp für die Verbindung mit der Eingabe-PIN der Sample Grabber ab.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Isamplegrabber:: getconnectedmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364595"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>Isamplegrabber:: getconnectedmediatype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetConnectedMediaType` Methode ruft den Medientyp für die Verbindung mit der Eingabe-PIN der Sample Grabber ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pType* 
</dt> <dd>

Zeiger auf eine vom Aufrufer zugeordnete Objekt- [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>             | **Null** -Zeigerargument.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Der Filter ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird der Medientyp in die von " *pType*" angegebene **\_ Medientyp \_** -Struktur kopiert. Der Aufrufer muss den Format Block des Medientyps freigeben. Sie können die Funktion " **CoTaskMemFree** " oder die Funktion " [**freemediatype**](freemediatype.md) " in der Basisklassen Bibliothek verwenden.

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

[Verwenden der Beispiel-Grabber](using-the-sample-grabber.md)
</dt> <dt>

[**Isamplegrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




