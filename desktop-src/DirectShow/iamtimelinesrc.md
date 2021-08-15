---
description: Die IAMTimelineSrc-Schnittstelle stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quellobjekte in DirectShow Editing Services (DES) bereit.
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: IAMTimelineSrc-Schnittstelle (Qedit.h)
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
ms.openlocfilehash: 5d2ad5684df6298bde458e87ff322b21622139930fa9aaf994fda0e7ba7e987e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399197"
---
# <a name="iamtimelinesrc-interface"></a>IAMTimelineSrc-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IAMTimelineSrc` -Schnittstelle stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quellobjekte in [DirectShow Editing Services](directshow-editing-services.md) (DES) bereit. Ein Quellobjekt stellt einen Stream aus einer Medienquelle dar.

Sie können einen Teil der Daten in einer Quelldatei verwenden, indem Sie die Start- und Stoppzeiten der Medien festlegen. Diese Werte geben den Anfang und das Ende des Quellobjekts relativ zur ursprünglichen Medienquelle an. Die Medienzeiten können sich von den Start- und Stoppzeiten des Objekts auf der Zeitachse unterscheiden, was eine schnelle oder langsame Wiedergabe ermöglicht. (Bei Audioquellen erfolgt eine Verschiebung der Tonhöhe.)

Rufen Sie zum Erstellen eines Quellobjekts [**IAMTimeline::CreateEmptyNode mit**](iamtimeline-createemptynode.md) dem Wert TIMELINE \_ MAJOR TYPE SOURCE \_ \_ auf. Sie können den zurückgegebenen [**IAMTimelineObj-Zeiger**](iamtimelineobj.md) für die **IAMTimelineSrc-Schnittstelle** abfragen. Weitere Informationen finden Sie unter [Erstellen einer Zeitachse und](constructing-a-timeline.md) Arbeiten mit [Quellen.](working-with-sources.md)

## <a name="members"></a>Member

Die **IAMTimelineSrc-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSrc verfügt** auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineSrc-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Rundet die angegebenen Zeitwerte auf die nächste Rahmengrenze.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Rundet die angegebenen Zeitwerte, die als **REFTIME-Werte** angegeben werden, auf die nächste Framegrenze.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Ruft die Standardbildrate des Quellobjekts ab.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Ruft die Medienlänge dieses Quellobjekts ab.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Ruft die Medienlänge dieses Quellobjekts als **REFTIME-Wert** ab.<br/>                     |
| [**GetMediaName**](iamtimelinesrc-getmedianame.md)       | Ruft den Namen der Quelldatei ab, die durch dieses Quellobjekt dargestellt wird.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Ruft die Start- und Stoppzeiten der Medien ab.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Ruft die Start- und Stoppzeiten der Medien als **REFTIME-Werte** ab.<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Ruft die aktuelle Streamnummer für das Quellobjekt ab.<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | Ruft den Stretchmodus einer Videoquelle ab.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Gibt an, ob der Clip mit der normalen Wiedergaberate abspielt.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Legt die Stoppzeit relativ zur Zeitachse fest.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Legt die Stoppzeit als **REFTIME-Wert** fest.<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Legt die Standardbildrate des Quellobjekts fest.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Gibt die Dauer der Quelldatei an.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Gibt die Dauer der Quelldatei als **REFTIME-Wert** an.<br/>                            |
| [**SetMediaName**](iamtimelinesrc-setmedianame.md)       | Gibt den Namen der Quelldatei an, die durch dieses Quellobjekt dargestellt wird.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Legt die Stopp- und Startzeiten der Medien fest.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Legt die Stopp- und Startzeiten der Medien als **REFTIME-Werte** fest.<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Gibt an, welcher Stream aus der Quelldatei gelesen werden soll, die diesem Quellobjekt zugeordnet ist.<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | Legt den Stretchmodus einer Videoquelle fest.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Verbindet dieses Quellobjekt mit einem anderen Quellobjekt.<br/>                                            |



 

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



 

 
