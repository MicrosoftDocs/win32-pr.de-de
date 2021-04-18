---
description: Diese Schnittstelle wird verwendet, um Animations Funktionen zu steuern und Animations Sätze mit den Transformations Frames zu verbinden, die animiert werden.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: ID3DXAnimationController-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361222"
---
# <a name="id3dxanimationcontroller-interface"></a>ID3DXAnimationController-Schnittstelle

Diese Schnittstelle wird verwendet, um Animations Funktionen zu steuern und Animations Sätze mit den Transformations Frames zu verbinden, die animiert werden. Die-Schnittstelle verfügt über Methoden zum Mischen mehrerer Animationen und zum Ändern von Mischungs Parametern im Zeitverlauf, um reibungslose Übergänge und andere Effekte zu ermöglichen.

## <a name="members"></a>Member

Die **ID3DXAnimationController** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXAnimationController** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXAnimationController** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Animiert das Mesh und erhöht die globale Animations Zeit um einen angegebenen Betrag.<br/>                                                              |
| [**Cloneanimationcontroller**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Klone oder kopiert einen Animations Controller.<br/>                                                                                                  |
| [**Getanimationset**](id3dxanimationcontroller--getanimationset.md)                     | Ruft einen Animations Satz ab.<br/>                                                                                                                       |
| [**Getanimationsetbyname**](id3dxanimationcontroller--getanimationsetbyname.md)         | Ruft einen Animations Satz mit dem angegebenen Namen ab.<br/>                                                                                                       |
| [**Getcurrentpriorityblend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Gibt ein Ereignis Handle an ein Priority Blend-Ereignis zurück, das gerade ausgeführt wird.<br/>                                                                 |
| [**Getcurrenttrackevent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Gibt ein Ereignis Handle für das Ereignis zurück, das momentan auf dem angegebenen Animations Titel ausgeführt wird.<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | Ruft eine Beschreibung eines angegebenen Animations Ereignisses ab.<br/>                                                                                           |
| [**Getmaxnumanimationoutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Erhalten Sie die maximale Anzahl von Animations Ausgaben, die der Animations Controller unterstützen kann.<br/>                                                            |
| [**Getmaxnumanimationsets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Ruft die maximale Anzahl von Animations Sätzen ab, die der Animations Controller unterstützen kann.<br/>                                                              |
| [**Getmaxnumevents**](id3dxanimationcontroller--getmaxnumevents.md)                     | Ruft die maximale Anzahl von Ereignissen ab, die der Animations Controller unterstützen kann.<br/>                                                                      |
| [**Getmaxnumtracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Ruft die maximale Anzahl von Spuren im Animations Controller ab.<br/>                                                                               |
| [**Getnumanimationsets**](id3dxanimationcontroller--getnumanimationsets.md)             | Gibt die Anzahl von Animations Sätzen zurück, die derzeit im Animations Controller registriert sind.<br/>                                                       |
| [**Getpriorityblend**](id3dxanimationcontroller--getpriorityblend.md)                   | Ruft die aktuelle Prioritäts Mischungs Gewichtung ab, die vom Animations Controller verwendet wird.<br/>                                                                  |
| [**GetTime**](id3dxanimationcontroller--gettime.md)                                     | Ruft die globale Animations Zeit ab.<br/>                                                                                                              |
| [**Gettrackanimationset**](id3dxanimationcontroller--gettrackanimationset.md)           | Ruft den Animations Satz für den angegebenen Titel ab.<br/>                                                                                                  |
| [**Gettrackdebug**](id3dxanimationcontroller--gettrackdesc.md)                           | Ruft die Titel Beschreibung ab.<br/>                                                                                                                  |
| [**Getupcomingpriorityblend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Gibt ein Ereignis Handle an das nächste in der nächsten Priorität angegebene Blend-Ereignis zurück, das nach einem angegebenen Ereignis geplant ist.<br/>                                         |
| [**Getupcomingtrackevent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Gibt ein Ereignis Handle für das nächste Ereignis zurück, das geplant ist, nachdem ein bestimmtes Ereignis auf einem Animations Titel auftritt.<br/>                                  |
| [**Keypriorityblend**](id3dxanimationcontroller--keypriorityblend.md)                   | Legt Mischungs Ereignis Schlüssel für den angegebenen Animations Titel fest.<br/>                                                                                  |
| [**Keytrackenable**](id3dxanimationcontroller--keytrackenable.md)                       | Legt einen Ereignis Schlüssel fest, der einen Animations Titel aktiviert oder deaktiviert.<br/>                                                                               |
| [**Keytrackposition**](id3dxanimationcontroller--keytrackposition.md)                   | Legt einen Ereignis Schlüssel fest, mit dem die Ortszeit eines Animations Titels geändert wird.<br/>                                                                         |
| [**Keytrackspeed**](id3dxanimationcontroller--keytrackspeed.md)                         | Legt einen Ereignis Schlüssel fest, der die Geschwindigkeit eines Animations Titels ändert.<br/>                                                                       |
| [**Keytrackweight**](id3dxanimationcontroller--keytrackweight.md)                       | Legt einen Ereignis Schlüssel fest, mit dem die Gewichtung eines Animations Titels geändert wird. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Titel zusammen kombiniert werden.<br/> |
| [**Registeranimationoutput**](id3dxanimationcontroller--registeranimationoutput.md)     | Fügt dem Animations Controller eine Animations Ausgabe hinzu und registriert Zeiger für die Transformation für Skalierung, Drehung und Übersetzung (SRT).<br/>          |
| [**Registeranimationset**](id3dxanimationcontroller--registeranimationset.md)           | Fügt dem Animations Controller einen Animations Satz hinzu.<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | Setzt die globale Animations Zeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne, aber im neuen Zeitrahmen bei.<br/>                 |
| [**Setpriorityblend**](id3dxanimationcontroller--setpriorityblend.md)                   | Legt die vom Animations Controller verwendete Prioritäts Mischungs Gewichtung fest.<br/>                                                                          |
| [**Settrackanimationset**](id3dxanimationcontroller--settrackanimationset.md)           | Wendet den Animations Satz auf den angegebenen Titel an.<br/>                                                                                            |
| [**Settrackdebug**](id3dxanimationcontroller--settrackdesc.md)                           | Legt die Titel Beschreibung fest.<br/>                                                                                                                  |
| [**Settrackenable**](id3dxanimationcontroller--settrackenable.md)                       | Aktiviert oder deaktiviert eine Spur im Animations Controller.<br/>                                                                                     |
| [**Settrackposition**](id3dxanimationcontroller--settrackposition.md)                   | Legt den Track auf die angegebene lokale Animations Zeit fest.<br/>                                                                                        |
| [**Settrackpriority**](id3dxanimationcontroller--settrackpriority.md)                   | Legt die Gewichtung für die Prioritäts Mischung für den angegebenen Animations Titel fest.<br/>                                                                         |
| [**Settrackspeed**](id3dxanimationcontroller--settrackspeed.md)                         | Legt die Erfolgs Geschwindigkeit fest. Die Erfolgs Geschwindigkeit ähnelt einem Multiplikator, der verwendet wird, um die Wiedergabe des Titels zu beschleunigen oder zu verlangsamen.<br/>            |
| [**Settrackweight**](id3dxanimationcontroller--settrackweight.md)                       | Legt die Last des Titels fest. Die Gewichtung wird verwendet, um zu bestimmen, wie mehrere Titel miteinander verknüpft werden.<br/>                                                |
| [**Unkeyallprioritymisch**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Entfernt alle Ereignisse für die geplante Prioritäts Mischung aus dem Animations Controller.<br/>                                                                   |
| [**Unkeyalltrackevents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Entfernt alle Ereignisse aus einer angegebenen Animations Spur.<br/>                                                                                         |
| [**Unkeyevent**](id3dxanimationcontroller--unkeyevent.md)                               | Entfernt ein angegebenes Ereignis aus einem Animations Titel und verhindert die Ausführung des Ereignisses.<br/>                                                    |
| [**Unregisteranimationset**](id3dxanimationcontroller--unregisteranimationset.md)       | Entfernt einen Animations Satz aus dem Animations Controller.<br/>                                                                                      |
| [**ValidateEvent**](id3dxanimationcontroller--validateevent.md)                         | Überprüft, ob ein angegebenes Ereignis Handle gültig ist und das Animations Ereignis noch nicht abgeschlossen wurde.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Erstellen Sie ein Animations Controller Objekt mit [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).

Der LPD3DXANIMATIONCONTROLLER-Typ wird als Zeiger auf die **ID3DXAnimationController** -Schnittstelle definiert.


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



Der D3DXEVENTHANDLE-Typ wird als Ereignis Handle für Animations Controller Ereignisse definiert.


```
typedef DWORD D3DXEVENTHANDLE;
```



Der LPD3DXEVENTHANDLE-Typ wird als Zeiger auf ein Ereignis Handle für Animations Controller Ereignisse definiert.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
