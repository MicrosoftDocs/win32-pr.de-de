---
description: Die GetConnectedMediaType-Methode ruft den Medientyp für die Verbindung am Eingabepin des Beispielgrabbers ab.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: ISampleGrabber::GetConnectedMediaType-Methode (Qedit.h)
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
ms.openlocfilehash: 03dc0c9763bdea75569f9447becb749bf284ae2ad7d77427f6dfc2f0aac58382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818059"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>ISampleGrabber::GetConnectedMediaType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetConnectedMediaType` -Methode ruft den Medientyp für die Verbindung auf dem Eingabepin des Beispielgrabbers ab.

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

Zeiger auf eine VOM Aufrufer zugeordnete [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeigerargument.**<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Filter ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kopiert den Medientyp in die **AM \_ MEDIA \_ TYPE-Struktur,** die durch *pType* angegeben wird. Der Aufrufer muss den Formatblock des Medientyps freigeben. Sie können die **CoTaskMemFree-Funktion** oder die [**FreeMediaType-Funktion**](freemediatype.md) in der Basisklassenbibliothek verwenden.

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

[Verwenden des Beispielgrabbers](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




