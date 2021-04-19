---
description: Die isamplegrabber-Schnittstelle wird durch den Sample-Grabber Filter verfügbar gemacht. Sie ermöglicht es einer Anwendung, einzelne Medien Beispiele abzurufen, während Sie durch das Filter Diagramm bewegt werden.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Isamplegrabber-Schnittstelle (qedit. h)
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
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369537"
---
# <a name="isamplegrabber-interface"></a>Isamplegrabber-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **isamplegrabber** -Schnittstelle wird durch den [**Sample-Grabber**](sample-grabber-filter.md) Filter verfügbar gemacht. Sie ermöglicht es einer Anwendung, einzelne Medien Beispiele abzurufen, während Sie durch das Filter Diagramm bewegt werden.

## <a name="members"></a>Member

Die **isamplegrabber** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Isamplegrabber** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **isamplegrabber** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md) | Ruft den Medientyp für die Verbindung mit der Eingabe-PIN von Sample Grabber ab.<br/>                                        |
| [**Getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md)           | Ruft eine Kopie des Beispiels ab, das der Filter zuletzt empfangen hat.<br/>                                                 |
| [**Getcurrentsample**](isamplegrabber-getcurrentsample.md)           | Nicht implementiert.<br/>                                                                                                       |
| [**Setbuffersamples**](isamplegrabber-setbuffersamples.md)           | Gibt an, ob Beispiel Daten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Gibt eine Rückruf Methode an, die für eingehende Stichproben aufgerufen wird.<br/>                                                               |
| [**Setmediatype**](isamplegrabber-setmediatype.md)                   | Gibt den Medientyp für die Verbindung in der Eingabe-PIN der Beispiel-Grabber an.<br/>                                    |
| [**"Abtoneshot"**](isamplegrabber-setoneshot.md)                       | Gibt an, ob der [**Sample Grabber**](sample-grabber-filter.md) -Filter angehalten wird, nachdem der Filter ein Beispiel erhalten hat.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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
</dt> </dl>

 

 
