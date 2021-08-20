---
description: Die IAMTimelineGroup-Schnittstelle legt Eigenschaften für Gruppen in DirectShow Editing Services (DES) fest und ruft sie ab. Eine Gruppe enthält mindestens eine Spur und möglicherweise eine oder mehrere Kompositionen, die wiederum Quellclips eines einheitlichen Typs wie Video oder Audio enthalten. Gruppen sind die obersten Kompositionen in einer Zeitachse und machen auch die IAMTimelineComp-Schnittstelle verfügbar. Eine Zeitachse kann mehrere Gruppen enthalten. Jede Gruppe verfügt über die folgenden Attribute. Ein zugeordneter Medientyp. Die Bildfrequenz, mit der die Gruppe in Frames pro Sekunde (FPS) gerendert wird. Alle Bearbeitungen erfolgen zu einem Zeitpunkt, der auf die nächste Framegrenze gerundet wird, wie durch die FPS-Einstellung der Gruppe definiert. Eine Prioritätsebene zum Schreiben von Dateien mit mehreren Streams desselben Medientyps (z. B. eine AVI-Datei mit zwei Videostreams). Um ein Gruppenobjekt zu erstellen, rufen Sie IAMTimeline::CreateEmptyNode mit dem Wert TIMELINE \_ MAJOR \_ TYPE GROUP \_ auf. Sie können den zurückgegebenen IAMTimelineObj-Zeiger für die IAMTimelineGroup-Schnittstelle abfragen.
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: IAMTimelineGroup-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9356e3edef0b61c119ec4cca774e9ec5976ac3732e0f0a508d103bc22bb0fef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155506"
---
# <a name="iamtimelinegroup-interface"></a>IAMTimelineGroup-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die Schnittstelle legt Eigenschaften für `IAMTimelineGroup` Gruppen in [DirectShow Editing Services](directshow-editing-services.md) (DES) fest und ruft sie ab.

Eine Gruppe enthält mindestens eine Spur und möglicherweise eine oder mehrere Kompositionen, die wiederum Quellclips eines einheitlichen Typs wie Video oder Audio enthalten. Gruppen sind die obersten Kompositionen in einer Zeitachse und machen auch die [**IAMTimelineComp-Schnittstelle**](iamtimelinecomp.md) verfügbar. Eine Zeitachse kann mehrere Gruppen enthalten.

Jede Gruppe verfügt über die folgenden Attribute.

-   Ein zugeordneter Medientyp.
-   Die Bildfrequenz, mit der die Gruppe in Frames pro Sekunde (FPS) gerendert wird. Alle Bearbeitungen erfolgen zu einem Zeitpunkt, der auf die nächste Framegrenze gerundet wird, wie durch die FPS-Einstellung der Gruppe definiert.
-   Eine Prioritätsebene zum Schreiben von Dateien mit mehreren Streams desselben Medientyps (z. B. eine AVI-Datei mit zwei Videostreams).

Um ein Gruppenobjekt zu erstellen, rufen [**Sie IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) mit dem Wert TIMELINE \_ MAJOR TYPE GROUP \_ \_ auf. Sie können den zurückgegebenen [**IAMTimelineObj-Zeiger**](iamtimelineobj.md) für die **IAMTimelineGroup-Schnittstelle** abfragen.

## <a name="members"></a>Member

Die **IAMTimelineGroup-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineGroup** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineGroup-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                            | Beschreibung                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Wird nicht unterstützt.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Ruft den anwendungsdefiniert Namen der Gruppe ab.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Ruft den nicht komprimierten Medientyp für die Gruppe ab.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Ruft die Anzahl der Frames ab, die während der Vorschau im Voraus gerendert wurden.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Ruft die Ausgabebildrate dieser Gruppe ab.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Ruft den Vorschaumodus für die Gruppe ab.<br/>                                            |
| [**GetPriority**](iamtimelinegroup-getpriority.md)                               | Ruft die Priorität der Gruppe ab.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Ruft das aktuelle Komprimierungsformat für die intelligente Neukomprimierung ab.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Ruft die Zeitachse ab, zu der diese Gruppe gehört.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Wird nicht unterstützt.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Bestimmt, ob ein intelligentes Komprimierungsformat für die Gruppe festgelegt wurde.<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | Legt den anwendungsdefinierte Namen der Gruppe fest.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Legt den nicht komprimierten Medientyp für die Gruppe fest.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Gibt den Gruppenmedientyp für Automation-Clients an.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Gibt die Anzahl der Frames an, die während der Vorschau im Voraus gerendert werden.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Legt die unkomprimierte Ausgabebildrate für diese Gruppe fest.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Legt den Vorschaumodus für die Gruppe fest.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Legt das Videorekomprimierungsformat mithilfe des Komprimierungsformats aus einer Quelldatei fest.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Gibt ein Komprimierungsformat an, das für die intelligente Neukomprimierung verwendet werden soll.<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | Wird nicht unterstützt.<br/>                                                                       |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
