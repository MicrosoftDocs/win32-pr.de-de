---
description: Die SetMediaType-Methode gibt den Medientyp für die Verbindung auf dem Eingabepin des Sample Grabber an.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: ISampleGrabber::SetMediaType-Methode (Qedit.h)
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
ms.openlocfilehash: 060ff0cc10fed441fdb2d6f2bf1bd0e66f3e8b9facec3cb52d8f270b350b1f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817701"
---
# <a name="isamplegrabbersetmediatype-method"></a>ISampleGrabber::SetMediaType-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetMediaType` -Methode gibt den Medientyp für die Verbindung auf dem Eingabepin des Sample Grabber an.

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

Der Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) gibt den erforderlichen Medientyp an. Es ist nicht erforderlich, alle Strukturmitglieder zu setzen. Weitere Informationen finden Sie unter Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Standardmäßig hat der Beispielgrabber keinen bevorzugten Medientyp. Um sicherzustellen, dass der Sample Grabber eine Verbindung mit dem richtigen Filter herstellt, rufen Sie diese Methode auf, bevor Sie das Filterdiagramm erstellen.

Diese Methode schränkt den Bereich der Medientypen ein, die der Filter akzeptiert. Wenn der Filter eine Verbindung herstellt, versucht er, mit dem in pType angegebenen *Medientyp zu übereinstimmen.* Zu diesem Schritt werden die Haupttyp-, Untertyp- und Formattyp-GUIDs in dieser Reihenfolge verglichen. Wenn *pType* für jede dieser GUIDs den Wert GUID NULL aufgibt, akzeptiert der Sample Grabber den Medientyp ohne \_ weitere Überprüfungen. Wenn *pType* über einen anderen Wert verfügt, vergleicht der Sample Grabber ihn mit der GUID im Verbindungstyp. Sofern die beiden GUIDs nicht genau übereinstimmen, lehnt der Beispielgrabber die Verbindung ab.

Bei Videomedientypen ignoriert der Sample Grabber den Formatblock. Daher akzeptiert sie jede Videogröße und Bildfrequenz. Wenn Sie `SetMediaType` aufrufen, legen Sie den Formatblock (**pbFormat**) auf **NULL** und die Größe (**cbFormat**) auf null fest. Bei Audiomedientypen untersucht der Sample Grabber die [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) und erfordert, dass der andere Filter eine Verbindung mit diesem Format herstellen muss– es sei denn, der Formatblock in *pType* ist **NULL,** oder das Formattag ist WAVE FORMAT PCM, und die anderen Strukturmitglieder sind 0 \_ \_ (null).

Beispiel 1:

-   Haupttyp: MEDIATYPE \_ Video
-   Untertyp: GUID \_ NULL
-   Formattyp: GUID \_ NULL

Der Sample Grabber akzeptiert jeden Videotyp, bei dem der Haupttyp MEDIATYPE \_ Video entspricht. Der Untertyp wird nicht überprüft.

Beispiel 2:

-   Haupttyp: MEDIATYPE \_ Video
-   Untertyp: MEDIASUBTYPE \_ RGB24
-   Formattyp: GUID \_ NULL

Das Beispielgrabber überprüft nun den Untertyp und akzeptiert nur RGB 24-Videos.

**Einschränkungen:** Unabhängig davon, welchen Typ Sie festlegen, lehnt der Sample Grabber Filter alle Videotypen mit top-down-Ausrichtung (negative *biHeight)* oder mit dem Formattyp FORMAT \_ VideoInfo2 ab. Obwohl die Methode erfolgreich ist, wird in diesem Fall `SetMediaType` keine Verbindung mit dem Filter hergestellt.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 
