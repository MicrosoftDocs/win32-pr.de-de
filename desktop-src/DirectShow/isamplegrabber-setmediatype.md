---
description: Die setmediatype-Methode gibt den Medientyp für die Verbindung in der Eingabe-PIN der Sample Grabber an.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Isamplegrabber:: setmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365784"
---
# <a name="isamplegrabbersetmediatype-method"></a>Isamplegrabber:: setmediatype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetMediaType` Methode gibt den Medientyp für die Verbindung in der Eingabe-PIN der Sample Grabber an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pType* 
</dt> <dd>

Ein Zeiger auf eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur gibt den erforderlichen Medientyp an. Es ist nicht erforderlich, alle Strukturmember festzulegen. Weitere Informationen finden Sie in den hinweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Standardmäßig hat der beispielgrabber keinen bevorzugten Medientyp. Um sicherzustellen, dass der Sample Grabber eine Verbindung mit dem richtigen Filter herstellt, müssen Sie diese Methode vor dem Aufbau des Filter Diagramms abrufen.

Diese Methode schränkt den Bereich der Medientypen ein, den der Filter akzeptiert. Wenn der Filter eine Verbindung herstellt, versucht er, den in *pType* angegebenen Medientyp abzugleichen. Zu diesem Zweck werden der Haupttyp, der Untertyp und die Formattyp-GUIDs in dieser Reihenfolge verglichen. Wenn *pType* für jede dieser GUIDs den Wert GUID \_ null hat, akzeptiert der beispielgrabber den Medientyp ohne weitere Überprüfungen. Wenn *pType* einen anderen Wert aufweist, vergleicht der Sample Grabber ihn mit der GUID im Verbindungstyp. Wenn die beiden GUIDs nicht exakt übereinstimmen, lehnt der Beispiel-Grabber die Verbindung ab.

Bei Video Medientypen ignoriert der Sample Grabber den Format Block. Aus diesem Grund werden die Videogröße und die Framerate akzeptiert. Wenn Sie aufzurufen `SetMediaType` , legen Sie den Format Block (**pbformat**) auf **null** und die Größe (**cbformat**) auf 0 (null) fest. Für audiomedientyp untersucht der Beispiel-Grabber die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur und erfordert, dass der andere Filter eine Verbindung mit diesem Format herstellt – es sei denn, der Format Block in *pType* ist **null**, oder das Format-Tag ist das Wave \_ \_ -Format PCM, und die anderen Strukturmember sind 0 (null).

Beispiel 1:

-   Haupttyp: MediaType- \_ Video
-   Untertyp: GUID \_ null
-   Formattyp: GUID \_ null

Der beispielgrabber akzeptiert jeden Videotyp, bei dem der Haupttyp dem Video "MediaType" gleicht \_ . Der Untertyp wird nicht überprüft.

Beispiel 2:

-   Haupttyp: MediaType- \_ Video
-   Untertyp: mediasubtype \_ RGB24
-   Formattyp: GUID \_ null

Nun prüft der Sample Grabber den Untertyp und akzeptiert nur RGB 24-Videos.

**Einschränkungen:** Unabhängig davon, welchen Typ Sie festlegen, lehnt der Sample Grabber Filter alle Video Typen mit der Top-Down-Ausrichtung (negative *biheight*) oder dem Formattyp Format \_ VideoInfo2 ab. In diesem Fall stellt `SetMediaType` der Filter keine Verbindung her, obwohl die Methode erfolgreich ausgeführt wird.

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

 

 
