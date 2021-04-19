---
description: 'Die iamtimelinegroup-Schnittstelle legt Eigenschaften für Gruppen in DirectShow-Bearbeitungs Diensten fest und ruft Sie ab. Eine Gruppe enthält eine oder mehrere Spuren und möglicherweise eine oder mehrere Kompositionen, die wiederum Quell Clips eines einheitlichen Typs enthalten, z. b. Video oder Audiodaten. Gruppen sind die obersten Kompositionen in einer Zeitachse und machen außerdem die iamtimelinecomp-Schnittstelle verfügbar. Eine Zeitachse kann mehrere Gruppen enthalten. Jede Gruppe verfügt über die folgenden Attribute. Ein zugeordneter Medientyp. Die Framerate, bei der die Gruppe in Frames pro Sekunde (fps) gerendert wird. Alle Änderungen erfolgen zu einem Zeitpunkt, der auf die nächste Frame Grenze gerundet wird, wie in der FPS-Einstellung der Gruppe definiert. Eine Prioritätsstufe zum Schreiben von Dateien mit mehreren Streams desselben Medientyps (z. b. eine Datei mit zwei Video-Stream-AVI). Um ein Gruppen Objekt zu erstellen, rufen Sie iamtimeline:: kreateemptynode mit dem Wert Timeline \_ Major \_ Type \_ Group auf. Sie können den zurückgegebenen iamtimelineobj-Zeiger für die iamtimelinegroup-Schnittstelle Abfragen.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Iamtimelinegroup-Schnittstelle (qedit. h)
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
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370854"
---
# <a name="iamtimelinegroup-interface"></a>Iamtimelinegroup-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IAMTimelineGroup` -Schnittstelle legt Eigenschaften für Gruppen in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fest und ruft Sie ab.

Eine Gruppe enthält eine oder mehrere Spuren und möglicherweise eine oder mehrere Kompositionen, die wiederum Quell Clips eines einheitlichen Typs enthalten, z. b. Video oder Audiodaten. Gruppen sind die obersten Kompositionen in einer Zeitachse und machen außerdem die [**iamtimelinecomp**](iamtimelinecomp.md) -Schnittstelle verfügbar. Eine Zeitachse kann mehrere Gruppen enthalten.

Jede Gruppe verfügt über die folgenden Attribute.

-   Ein zugeordneter Medientyp.
-   Die Framerate, bei der die Gruppe in Frames pro Sekunde (fps) gerendert wird. Alle Änderungen erfolgen zu einem Zeitpunkt, der auf die nächste Frame Grenze gerundet wird, wie in der FPS-Einstellung der Gruppe definiert.
-   Eine Prioritätsstufe zum Schreiben von Dateien mit mehreren Streams desselben Medientyps (z. b. eine Datei mit zwei Video-Stream-AVI).

Um ein Gruppen Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline \_ Major \_ Type \_ Group auf. Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die **iamtimelinegroup** -Schnittstelle Abfragen.

## <a name="members"></a>Member

Die **iamtimelinegroup** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinegroup** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinegroup** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                            | BESCHREIBUNG                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Clearrecompressformatdirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Wird nicht unterstützt.<br/>                                                                       |
| [**Getgroupname**](iamtimelinegroup-getgroupname.md)                             | Ruft den von der Anwendung definierten Namen der Gruppe ab.<br/>                                 |
| [**Getmediatype**](iamtimelinegroup-getmediatype.md)                             | Ruft den unkomprimierten Medientyp für die Gruppe ab.<br/>                                 |
| [**Getoutputbuffereing**](iamtimelinegroup-getoutputbuffering.md)                 | Ruft die Anzahl der Frames ab, die während der Vorschau im Voraus gerendert werden.<br/>                   |
| [**Getoutputfps**](iamtimelinegroup-getoutputfps.md)                             | Ruft die Ausgabe Rahmenrate dieser Gruppe ab.<br/>                                       |
| [**Getpreviewmode**](iamtimelinegroup-getpreviewmode.md)                         | Ruft den Vorschaumodus für die Gruppe ab.<br/>                                            |
| [**GetPriority**](iamtimelinegroup-getpriority.md)                               | Ruft die Priorität der Gruppe ab.<br/>                                                      |
| [**Geffs martrecompressformat**](iamtimelinegroup-getsmartrecompressformat.md)     | Ruft das aktuelle Komprimierungs Format für die intelligente Neukomprimierung ab.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Ruft die Zeitachse ab, zu der diese Gruppe gehört.<br/>                                  |
| [**Isrecompressformatdirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Wird nicht unterstützt.<br/>                                                                       |
| [**Issmartrecompressformatset**](iamtimelinegroup-issmartrecompressformatset.md) | Bestimmt, ob ein intelligentes Komprimierungs Format für die Gruppe festgelegt wurde.<br/>                 |
| [**Setgroupname**](iamtimelinegroup-setgroupname.md)                             | Legt den von der Anwendung definierten Namen der Gruppe fest.<br/>                                      |
| [**Setmediatype**](iamtimelinegroup-setmediatype.md)                             | Legt den unkomprimierten Medientyp für die Gruppe fest.<br/>                                      |
| [**Setmediatypeer forvb**](iamtimelinegroup-setmediatypeforvb.md)                   | Gibt den Gruppen Medientyp für Automatisierungs Clients an.<br/>                              |
| [**Setoutputbuffereing**](iamtimelinegroup-setoutputbuffering.md)                 | Gibt an, wie viele Frames während der Vorschau vorab gerendert werden.<br/>                   |
| [**Setoutputfps**](iamtimelinegroup-setoutputfps.md)                             | Legt die nicht komprimierte Ausgabe Frame Rate für diese Gruppe fest.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Legt den Vorschaumodus für die Gruppe fest.<br/>                                                 |
| [**"Abbild compformatfromsource"**](iamtimelinegroup-setrecompformatfromsource.md)   | Legt das Format der Video Neukomprimierung mit dem Komprimierungs Format aus einer Quelldatei fest.<br/> |
| [**"-Martrecompressformat"**](iamtimelinegroup-setsmartrecompressformat.md)     | Gibt ein für die intelligente Neukomprimierung zu verwendende Komprimierungs Format an.<br/>                       |
| [**Settimeline**](iamtimelinegroup-settimeline.md)                               | Wird nicht unterstützt.<br/>                                                                       |



 

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



 

 
