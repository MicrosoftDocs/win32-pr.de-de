---
description: Die iamtimelinesrc-Schnittstelle stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quell Objekte in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Iamtimelinesrc-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359251"
---
# <a name="iamtimelinesrc-interface"></a>Iamtimelinesrc-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IAMTimelineSrc` -Schnittstelle stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quell Objekte in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit. Ein-Quell Objekt stellt einen Stream aus einer Medienquelle dar.

Sie können einen Teil der Daten innerhalb einer Quelldatei verwenden, indem Sie die Start-und Medien Endzeiten der Medien festlegen. Diese Werte geben den Anfang und das Ende des Quell Objekts relativ zur ursprünglichen Medienquelle an. Die Medien Zeiten können sich von den Start-und Endzeiten des Objekts auf der Zeitachse unterscheiden, sodass eine schnelle oder langsame Bewegungs Wiedergabe ermöglicht wird. (Bei Audioquellen erfolgt die Verschiebung der Tonhöhe.)

Um ein Quell Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline- \_ \_ Haupttyp \_ Quelle auf. Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die **iamtimelinesrc** -Schnittstelle Abfragen. Weitere Informationen finden Sie unter [Erstellen einer Zeitachse](constructing-a-timeline.md) und [Arbeiten mit Quellen](working-with-sources.md).

## <a name="members"></a>Member

Die **iamtimelinesrc** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinesrc** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinesrc** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**Fixmediatimes**](iamtimelinesrc-fixmediatimes.md)     | Rundet die angegebenen Uhrzeitwerte auf die nächste Frame Grenze.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Rundet die angegebenen Uhrzeitwerte, die als **reftime** -Werte angegeben sind, auf die nächste Frame Grenze.<br/> |
| [**Getdefaultfps**](iamtimelinesrc-getdefaultfps.md)     | Ruft die Standardbildrate des Quell Objekts ab.<br/>                                             |
| [**Getmedialength**](iamtimelinesrc-getmedialength.md)   | Ruft die Medien Länge dieses Quell Objekts ab.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Ruft die Medien Länge dieses Quell Objekts als **ref** -Wert ab.<br/>                     |
| [**Getmedianame**](iamtimelinesrc-getmedianame.md)       | Ruft den Namen der Quelldatei ab, die durch dieses Quell Objekt dargestellt wird.<br/>                      |
| [**Getmediatimes**](iamtimelinesrc-getmediatimes.md)     | Ruft die Start-und Endzeit des Mediums ab.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Ruft die Start-und Endzeit Werte des Mediums als **ref-Zeit** Werte ab.<br/>                              |
| [**Getstreamnumber**](iamtimelinesrc-getstreamnumber.md) | Ruft die aktuelle streamnummer für das Quell Objekt ab.<br/>                                    |
| [**Getstretchmode**](iamtimelinesrc-getstretchmode.md)   | Ruft den streckungs Modus einer Videoquelle ab.<br/>                                                 |
| [**Isnormalrate**](iamtimelinesrc-isnormalrate.md)       | Gibt an, ob der Clip mit der normalen Wiedergabe Rate wiedergegeben wird.<br/>                             |
| [**Modifystoptime**](iamtimelinesrc-modifystoptime.md)   | Legt die Endzeit relativ zur Zeitachse fest.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Legt die Endzeit als **ref** -Wert fest.<br/>                                                   |
| [**Setdefaultfps**](iamtimelinesrc-setdefaultfps.md)     | Legt die Standardbildrate des Quell Objekts fest.<br/>                                                  |
| [**Setmedialength**](iamtimelinesrc-setmedialength.md)   | Gibt die Dauer der Quelldatei an.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Gibt die Dauer der Quelldatei als **ref** -Wert an.<br/>                            |
| [**Setmedianame**](iamtimelinesrc-setmedianame.md)       | Gibt den Namen der Quelldatei an, die durch dieses Quell Objekt dargestellt wird.<br/>                      |
| [**Setmediatimes**](iamtimelinesrc-setmediatimes.md)     | Legt die Start-und Startzeiten des Mediums fest.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Legt die Start-und Startzeiten der Medien als **ref-Zeit** Werte fest.<br/>                                   |
| [**Setstreamnumber**](iamtimelinesrc-setstreamnumber.md) | Gibt an, welcher Stream aus der mit diesem Quell Objekt verknüpften Quelldatei gelesen werden soll.<br/>       |
| [**Setstretchmode**](iamtimelinesrc-setstretchmode.md)   | Legt den streckungs Modus einer Videoquelle fest.<br/>                                                      |
| [**Splicewithnext**](iamtimelinesrc-splicewithnext.md)   | Verbindet dieses Quell Objekt mit einem anderen Quell Objekt.<br/>                                            |



 

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



 

 
