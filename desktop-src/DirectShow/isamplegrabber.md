---
description: Die ISampleGrabber-Schnittstelle wird durch den Sample Grabber-Filter verfügbar gemacht. Sie ermöglicht es einer Anwendung, einzelne Medienbeispiele abzurufen, während sie sich durch das Filterdiagramm bewegen.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: ISampleGrabber-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 485301d58da6ca48bf43414fd9907048943ab8868c514132e2887fef29e5d2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817644"
---
# <a name="isamplegrabber-interface"></a>ISampleGrabber-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die **ISampleGrabber-Schnittstelle** wird durch den [**Sample Grabber-Filter**](sample-grabber-filter.md) verfügbar gemacht. Sie ermöglicht es einer Anwendung, einzelne Medienbeispiele abzurufen, während sie sich durch das Filterdiagramm bewegen.

## <a name="members"></a>Member

Die **ISampleGrabber-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISampleGrabber** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISampleGrabber-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Ruft den Medientyp für die Verbindung auf dem Eingabepin von Sample Grabber ab.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Ruft eine Kopie des Beispiels ab, das der Filter zuletzt empfangen hat.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Nicht implementiert.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Gibt an, ob Beispieldaten während des Durchlaufs des Filters in einen Puffer kopiert werden.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Gibt eine Rückrufmethode zum Aufrufen eingehender Stichproben an.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Gibt den Medientyp für die Verbindung auf dem Eingabepin des Beispielgrabbers an.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Gibt an, ob [**der Sample Grabber-Filter**](sample-grabber-filter.md) anzuhalten ist, nachdem der Filter eine Stichprobe empfangen hat.<br/> |



 

## <a name="remarks"></a>Hinweise

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
</dt> </dl>

 

 
