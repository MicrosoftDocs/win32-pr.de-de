---
description: Die iamtimelineobj-Schnittstelle stellt Methoden zum Bearbeiten von Zeitachsen Objekten in DirectShow-Bearbeitungs Diensten (de) bereit.
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Iamtimelineobj-Schnittstelle (qedit. h)
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
ms.openlocfilehash: e968ec01d937aeac9a5838b75462a6d23a632512
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352897"
---
# <a name="iamtimelineobj-interface"></a>Iamtimelineobj-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimelineObj` Schnittstelle stellt Methoden zum Bearbeiten von Zeitachsen Objekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit. Alle Timeline-Objekte implementieren diese Methode, einschließlich Quell-, Effekt-, Übergangs-, Nachverfolgung-, Gruppen-und Kompositions Objekte. Erstellen Sie ein Zeitachsen Objekt, indem Sie die [**iamtimeline:: createemptynode**](iamtimeline-createemptynode.md) -Methode aufrufen.

## <a name="members"></a>Member

Die **iamtimelineobj** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelineobj** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelineobj** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Cleardirty**](iamtimelineobj-cleardirty.md)                 | Wird nicht unterstützt.<br/>                                                                                                              |
| [**Fixtimes**](iamtimelineobj-fixtimes.md)                     | Rundet die angegebene Start-und Endzeit auf die nächsten Frame Begrenzungen auf.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Rundet die angegebenen Start-und Endzeit Werte, die als [**reftime**](reftime.md) -Werte angegeben sind, auf die nächsten Frame Begrenzungen auf.<br/> |
| [**Getdirtyrange**](iamtimelineobj-getdirtyrange.md)           | Wird nicht unterstützt.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Wird nicht unterstützt.<br/>                                                                                                              |
| [**Getembedtiefe**](iamtimelineobj-getembeddepth.md)           | Wird nicht unterstützt.<br/>                                                                                                              |
| [**Getgenid**](iamtimelineobj-getgenid.md)                     | Ruft den generierten Bezeichner des Objekts ab.<br/>                                                                                |
| [**Getgroupibelongto**](iamtimelineobj-getgroupibelongto.md)   | Wird nicht unterstützt.<br/>                                                                                                              |
| [**Getlocked**](iamtimelineobj-getlocked.md)                   | Ruft den Bearbeitungs Zustand des Objekts ab (gesperrt oder entsperrt).<br/>                                                                  |
| [**Getmutiert**](iamtimelineobj-getmuted.md)                     | Ruft den gedämpften Zustand des Objekts ab.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Ruft den Eigenschaften Setter des Objekts ab.<br/>                                                                                     |
| [**Getstartstopps**](iamtimelineobj-getstartstop.md)             | Ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Ruft die Start-und Endzeit Werte des-Objekts als [**ref-Zeit**](reftime.md) Werte ab.<br/>                                          |
| [**Getsubobject**](iamtimelineobj-getsubobject.md)             | Ruft das diesem-Objekt zugeordnete untergeordnete Objekt ab.<br/>                                                                        |
| [**Getsubobjectguid**](iamtimelineobj-getsubobjectguid.md)     | Ruft die GUID des untergeordneten Objekts ab, das diesem Zeitachsen Objekt zugeordnet ist.<br/>                                                   |
| [**Getsubobjectguidb**](iamtimelineobj-getsubobjectguidb.md)   | Ruft die GUID des untergeordneten Objekts als **BSTR** -Wert ab.<br/>                                                                    |
| [**Getsubobjectloaded**](iamtimelineobj-getsubobjectloaded.md) | Bestimmt, ob der untergeordnete Zeiger des Objekts festgelegt wurde.<br/>                                                             |
| [**Gettimelinenoref**](iamtimelineobj-gettimelinenoref.md)     | Wird nicht unterstützt.<br/>                                                                                                              |
| [**Gettimelinetype**](iamtimelineobj-gettimelinetype.md)       | Ruft den Objekttyp ab.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Ruft die von der Anwendung definierten persistenten Daten ab.<br/>                                                                          |
| [**BENUTZERID**](iamtimelineobj-getuserid.md)                   | Ruft den von der Anwendung definierten Bezeichner des Objekts ab.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Ruft den von der Anwendung definierten Namen des Objekts ab.<br/>                                                                            |
| [**Aufgeh**](iamtimelineobj-remove.md)                         | Entfernt dieses-Objekt aus der Zeitachse, um es an anderer Stelle wiederherzustellen.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Entfernt dieses objektpermanent aus der Zeitachse, einschließlich untergeordneten Elementen und untergeordneten Elementen.<br/>                                       |
| [**Setdirtyrange**](iamtimelineobj-setdirtyrange.md)           | Nicht implementiert.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Nicht implementiert.<br/>                                                                                                            |
| [**Setlocked**](iamtimelineobj-setlocked.md)                   | Legt den Bearbeitungs Zustand des-Objekts auf gesperrt oder entsperrt fest.<br/>                                                                      |
| [**Setstumm**](iamtimelineobj-setmuted.md)                     | Legt den gedämpften Zustand des-Objekts fest.<br/>                                                                                              |
| [**Setpropertysetter**](iamtimelineobj-setpropertysetter.md)   | Legt den Eigenschaften Setter des Objekts fest.<br/>                                                                                          |
| [**Setstartstopp**](iamtimelineobj-setstartstop.md)             | Legt die Start-und Endzeit des Objekts relativ zur Zeitachse fest.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Legt die Start-und Endzeit Werte des-Objekts als **ref-Zeit** Werte fest.<br/>                                                              |
| [**Setsubobject**](iamtimelineobj-setsubobject.md)             | Wird nicht unterstützt.<br/>                                                                                                              |
| [**Setsubobjectguid**](iamtimelineobj-setsubobjectguid.md)     | Gibt die Globally Unique Identifier (GUID) des untergeordneten Objekts an, das diesem Objekt zugeordnet ist.<br/>                               |
| [**Setsubobjectguidb**](iamtimelineobj-setsubobjectguidb.md)   | Gibt die GUID des untergeordneten Objekts als **BSTR** -Wert an.<br/>                                                                    |
| [**Settimelinetype**](iamtimelineobj-settimelinetype.md)       | Wird nicht unterstützt.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Legt von der Anwendung definierte persistente Daten fest.<br/>                                                                                   |
| [**Setuserid**](iamtimelineobj-setuserid.md)                   | Legt einen von der Anwendung definierten Bezeichner für das-Objekt fest.<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Legt einen von der Anwendung definierten Namen für das-Objekt fest.<br/>                                                                            |



 

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



 

 
