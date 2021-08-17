---
description: Die IAMTimelineObj-Schnittstelle stellt Methoden zum Bearbeiten von Zeitachsenobjekten in DirectShow Editing Services (DES) bereit.
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: IAMTimelineObj-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4a987cfd0f08311a0e7a233ab479e5cdbe2fc649fd521ad4f4ed1b37b6df6d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428160"
---
# <a name="iamtimelineobj-interface"></a>IAMTimelineObj-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IAMTimelineObj` -Schnittstelle stellt Methoden zum Bearbeiten von Zeitachsenobjekten in [DirectShow Editing Services](directshow-editing-services.md) (DES) bereit. Alle Zeitachsenobjekte implementieren diese Methode, einschließlich Quell-, Effekt-, Übergangs-, Nachverfolgungs-, Gruppen- und Kompositionsobjekte. Erstellen Sie ein Zeitachsenobjekt, indem Sie die [**IAMTimeline::CreateEmptyNode-Methode**](iamtimeline-createemptynode.md) aufrufen.

## <a name="members"></a>Member

Die **IAMTimelineObj-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineObj** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineObj-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | Wird nicht unterstützt.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Rundet die angegebenen Start- und Stoppzeiten auf die nächsten Rahmengrenzen.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Rundet die angegebenen Start- und Stoppzeiten, die als [**REFTIME-Werte**](reftime.md) angegeben werden, auf die nächsten Rahmengrenzen.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | Wird nicht unterstützt.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Wird nicht unterstützt.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | Wird nicht unterstützt.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Ruft den generierten Bezeichner des Objekts ab.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | Wird nicht unterstützt.<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | Ruft den Bearbeitungsstatus des Objekts ab (gesperrt oder entsperrt).<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | Ruft den stummgeschalteten Zustand des Objekts ab.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Ruft den Eigenschaftens setter des Objekts ab.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Ruft die Start- und Stoppzeiten des Objekts relativ zum übergeordneten Element des Objekts ab.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Ruft die Start- und Stoppzeiten des Objekts als [**REFTIME-Werte**](reftime.md) ab.<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Ruft das diesem -Objekt zugeordnete Unterobjekt ab.<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Ruft die GUID des Unterobjekts ab, das diesem Zeitachsenobjekt zugeordnet ist.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Ruft die GUID des Unterobjekts als **BSTR-Wert** ab.<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Bestimmt, ob der Unterobjektzeiger des Objekts festgelegt wurde.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | Wird nicht unterstützt.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Ruft den Typ des Objekts ab.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Ruft die anwendungsdefinierten persistenten Daten ab.<br/>                                                                          |
| [**BENUTZERID**](iamtimelineobj-getuserid.md)                   | Ruft den anwendungsdefinierten Bezeichner des Objekts ab.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Ruft den anwendungsdefinierten Namen des Objekts ab.<br/>                                                                            |
| [**Entfernen**](iamtimelineobj-remove.md)                         | Entfernt dieses Objekt aus der Zeitachse, um es an anderer Stelle wieder zu resertionen.<br/>                                                           |
| [**Removeall**](iamtimelineobj-removeall.md)                   | Entfernt dieses Objekt dauerhaft aus der Zeitachse, einschließlich Unterobjekten und untergeordneten Objekten.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Nicht implementiert.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Nicht implementiert.<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | Legt den Bearbeitungszustand des Objekts auf gesperrt oder entsperrt fest.<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | Legt den stummgeschalteten Zustand des Objekts fest.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Legt den Eigenschaftens setter des Objekts fest.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Legt die Start- und Stoppzeiten des Objekts relativ zur Zeitachse fest.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Legt die Start- und Stoppzeiten des Objekts als **REFTIME-Werte** fest.<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | Wird nicht unterstützt.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Gibt den globally unique identifier (GUID) des Diesem -Objekt zugeordneten Unterobjekts an.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Gibt die GUID des Unterobjekts als **BSTR-Wert** an.<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | Wird nicht unterstützt.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Legt anwendungsdefinierte persistente Daten fest.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Legt einen anwendungsdefinierten Bezeichner für das -Objekt fest.<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Legt einen anwendungsdefinierten Namen für das -Objekt fest.<br/>                                                                            |



 

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



 

 
