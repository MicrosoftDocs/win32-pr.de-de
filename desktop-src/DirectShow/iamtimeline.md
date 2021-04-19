---
description: Die iamtimeline-Schnittstelle stellt Methoden zum Bearbeiten der Zeitachse bereit, das zentrale Objekt in Microsoft DirectShow-Bearbeitungs Diensten (des).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Iamtimeline-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356050"
---
# <a name="iamtimeline-interface"></a>Iamtimeline-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimeline` Schnittstelle stellt Methoden zum Bearbeiten der Zeitachse bereit, das zentrale Objekt in Microsoft [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (des). Eine Zeitachse ist eine Auflistung von zeitlich geordneten Elementen, z. b. Videoclips, Audioclips, Effekte und Übergänge zwischen Clips. Die Renderingengine verwendet die Zeitachse, um ein Filter Diagramm zu erstellen, aus dem die Anwendung die gerenderte Ausgabe generieren kann.

`IAMTimeline` führt drei grundlegende Dienste aus. Es

-   Erstellt die-Objekte in der Zeitachse.
-   Fungiert als Container für diese Objekte.
-   Legt allgemeine Parameter der Zeitachse fest und ruft Sie ab.

Um das Timeline-Objekt zu erstellen, rufen Sie **cokreateinstance** mit der Klassen-ID CLSID \_ amtimeline auf.

## <a name="members"></a>Member

Die **iamtimeline** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimeline** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimeline** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**AddGroup**](iamtimeline-addgroup.md)                           | Fügt der Zeitachse eine Gruppe hinzu.<br/>                                                                                          |
| [**Clearallgroups**](iamtimeline-clearallgroups.md)               | Entfernt alle Gruppen aus der Zeitachse zusammen mit allen Objekten, die in diesen Gruppen enthalten sind.<br/>                                |
| [**"Kreateemptynode"**](iamtimeline-createemptynode.md)             | Erstellt ein neues Timeline-Objekt.<br/>                                                                                         |
| [**Effectsenabled**](iamtimeline-effectsenabled.md)               | Bestimmt, ob Effekte aktiviert sind.<br/>                                                                                |
| [**Enableeffects**](iamtimeline-enableeffects.md)                 | Aktiviert oder deaktiviert alle Effekte in der Zeitachse.<br/>                                                                       |
| [**Enableübergänge**](iamtimeline-enabletransitions.md)         | Aktiviert oder deaktiviert alle Übergänge in der Zeitachse.<br/>                                                                   |
| [**Getgräfin Service Type**](iamtimeline-getcountoftype.md)               | Ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Elementen enthalten sind.<br/> |
| [**Getdefaulteffect**](iamtimeline-getdefaulteffect.md)           | Ruft den Standardeffekt ab.<br/>                                                                                          |
| [**Getdefaulteffectb**](iamtimeline-getdefaulteffectb.md)         | Ruft den Standardeffekt als **BSTR** -Wert ab.<br/>                                                                      |
| [**Getdefaultfps**](iamtimeline-getdefaultfps.md)                 | Ruft die Standardausgabe Frame Rate in Frames pro Sekunde ab.<br/>                                                         |
| [**Getdefaulttransition**](iamtimeline-getdefaulttransition.md)   | Ruft den Standard Übergang ab.<br/>                                                                                      |
| [**Getdefaulttransitionb**](iamtimeline-getdefaulttransitionb.md) | Ruft den Standard Übergang als **BSTR** -Wert ab.<br/>                                                                  |
| [**Getdirtyrange**](iamtimeline-getdirtyrange.md)                 | Wird nicht unterstützt.<br/>                                                                                                         |
| [**Getduration**](iamtimeline-getduration.md)                     | Ruft die Dauer der Zeitachse ab.<br/>                                                                                       |
| [**GetDuration2**](iamtimeline-getduration2.md)                   | Ruft die Dauer der Zeitachse als **Double** ab.<br/>                                                                       |
| [**GetGroup**](iamtimeline-getgroup.md)                           | Ruft eine angegebene Gruppe ab.<br/>                                                                                           |
| [**Getgroupcount**](iamtimeline-getgroupcount.md)                 | Ruft die Anzahl der Gruppen ab, die in der Zeitachse enthalten sind.<br/>                                                     |
| [**Getinsertmode**](iamtimeline-getinsertmode.md)                 | Wird nicht unterstützt.<br/>                                                                                                         |
| [**IsDirty**](iamtimeline-isdirty.md)                             | Wird nicht unterstützt.<br/>                                                                                                         |
| [**Remgroupfromlist**](iamtimeline-remgroupfromlist.md)           | Wird nicht unterstützt.<br/>                                                                                                         |
| [**Setdefaulteffect**](iamtimeline-setdefaulteffect.md)           | Legt den Standardeffekt fest.<br/>                                                                                               |
| [**Setdefaulteffectb**](iamtimeline-setdefaulteffectb.md)         | Legt den Standardeffekt als **BSTR** -Wert fest.<br/>                                                                           |
| [**Setdefaultfps**](iamtimeline-setdefaultfps.md)                 | Legt die Standardausgabe Frame Rate in Frames pro Sekunde fest.<br/>                                                              |
| [**Setdefaulttransition**](iamtimeline-setdefaulttransition.md)   | Legt den Standard Übergang fest.<br/>                                                                                           |
| [**Setdefaulttransitionb**](iamtimeline-setdefaulttransitionb.md) | Legt den Standard Übergang als BSTR-Wert fest.<br/>                                                                           |
| [**"Stinsertmode"**](iamtimeline-setinsertmode.md)                 | Nicht implementiert.<br/>                                                                                                       |
| [**Setinterestrange**](iamtimeline-setinterestrange.md)           | Nicht implementiert.<br/>                                                                                                       |
| [**Transitionsenabled**](iamtimeline-transitionsenabled.md)       | Bestimmt, ob Übergänge aktiviert sind.<br/>                                                                            |
| [**Validatesourcenames**](iamtimeline-validatesourcenames.md)     | Überprüft die Quellnamen in der Zeitachse.<br/>                                                                                |



 

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



 

 
