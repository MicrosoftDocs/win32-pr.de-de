---
description: Diese Schnittstelle wird verwendet, um die Animationsfunktionalität zu steuern und Animationssätze mit den animierten Transformationsframes zu verbinden.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: ID3DXAnimationController-Schnittstelle (D3dx9anim.h)
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
ms.openlocfilehash: d01bafe9a20e56741f7e8b7ec9828386883fbdc150632335a342240c0a64a858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987810"
---
# <a name="id3dxanimationcontroller-interface"></a>ID3DXAnimationController-Schnittstelle

Diese Schnittstelle wird verwendet, um die Animationsfunktionalität zu steuern und Animationssätze mit den animierten Transformationsframes zu verbinden. Die -Schnittstelle verfügt über Methoden zum Mischen mehrerer Animationen und zum Ändern von Überblendungsparametern im Laufe der Zeit, um reibungslose Übergänge und andere Effekte zu ermöglichen.

## <a name="members"></a>Member

Die **ID3DXAnimationController-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXAnimationController** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXAnimationController-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Animiert das Gitternetz und erweitert die globale Animationszeit um einen angegebenen Betrag.<br/>                                                              |
| [**CloneAnimationController**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Klont oder kopiert einen Animationscontroller.<br/>                                                                                                  |
| [**GetAnimationSet**](id3dxanimationcontroller--getanimationset.md)                     | Ruft einen Animationssatz ab.<br/>                                                                                                                       |
| [**GetAnimationSetByName**](id3dxanimationcontroller--getanimationsetbyname.md)         | Ruft einen Animationssatz mit seinem Namen ab.<br/>                                                                                                       |
| [**GetCurrentPriorityBlend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Gibt ein Ereignishandle für ein Prioritätsmischungsereignis zurück, das derzeit ausgeführt wird.<br/>                                                                 |
| [**GetCurrentTrackEvent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Gibt ein Ereignishandle für das Ereignis zurück, das derzeit auf der angegebenen Animationsspur ausgeführt wird.<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | Ruft eine Beschreibung eines angegebenen Animationsereignisses ab.<br/>                                                                                           |
| [**GetMaxNumAnimationOutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Abrufen der maximalen Anzahl von Animationsausgaben, die der Animationscontroller unterstützen kann.<br/>                                                            |
| [**GetMaxNumAnimationSets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Ruft die maximale Anzahl von Animationssätzen ab, die der Animationscontroller unterstützen kann.<br/>                                                              |
| [**GetMaxNumEvents**](id3dxanimationcontroller--getmaxnumevents.md)                     | Ruft die maximale Anzahl von Ereignissen ab, die der Animationscontroller unterstützen kann.<br/>                                                                      |
| [**GetMaxNumTracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Ruft die maximale Anzahl von Spuren im Animationscontroller ab.<br/>                                                                               |
| [**GetNumAnimationSets**](id3dxanimationcontroller--getnumanimationsets.md)             | Gibt die Anzahl der derzeit im Animationscontroller registrierten Animationssätze zurück.<br/>                                                       |
| [**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)                   | Ruft die aktuelle Prioritätsmischungsgewichtung ab, die vom Animationscontroller verwendet wird.<br/>                                                                  |
| [**Gettime**](id3dxanimationcontroller--gettime.md)                                     | Ruft die globale Animationszeit ab.<br/>                                                                                                              |
| [**GetTrackAnimationSet**](id3dxanimationcontroller--gettrackanimationset.md)           | Ruft den Animationssatz für die angegebene Spur ab.<br/>                                                                                                  |
| [**GetTrackDesc**](id3dxanimationcontroller--gettrackdesc.md)                           | Ruft die Trackbeschreibung ab.<br/>                                                                                                                  |
| [**GetUpcomingPriorityBlend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Gibt ein Ereignishandle für das nächste Prioritätsmischungsereignis zurück, das nach einem angegebenen Ereignis auftreten soll.<br/>                                         |
| [**GetUpcomingTrackEvent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Gibt ein Ereignishandle für das nächste Ereignis zurück, das nach einem angegebenen Ereignis auf einer Animationsspur auftreten soll.<br/>                                  |
| [**KeyPriorityBlend**](id3dxanimationcontroller--keypriorityblend.md)                   | Legt Blendingereignisschlüssel für die angegebene Animationsspur fest.<br/>                                                                                  |
| [**KeyTrackEnable**](id3dxanimationcontroller--keytrackenable.md)                       | Legt einen Ereignisschlüssel fest, der eine Animationsspur aktiviert oder deaktiviert.<br/>                                                                               |
| [**KeyTrackPosition**](id3dxanimationcontroller--keytrackposition.md)                   | Legt einen Ereignisschlüssel fest, der die Ortszeit einer Animationsspur ändert.<br/>                                                                         |
| [**KeyTrackSpeed**](id3dxanimationcontroller--keytrackspeed.md)                         | Legt einen Ereignisschlüssel fest, der die Wiedergaberate einer Animationsspur ändert.<br/>                                                                       |
| [**KeyTrackWeight**](id3dxanimationcontroller--keytrackweight.md)                       | Legt einen Ereignisschlüssel fest, der die Gewichtung einer Animationsspur ändert. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Spuren kombiniert werden.<br/> |
| [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)     | Fügt dem Animationscontroller eine Animationsausgabe hinzu und registriert Zeiger für SRT-Transformationen (Scale, Rotate, Translate).<br/>          |
| [**RegisterAnimationSet**](id3dxanimationcontroller--registeranimationset.md)           | Fügt dem Animationscontroller einen Animationssatz hinzu.<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | Setzt die globale Animationszeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne bei, jedoch im neuen Zeitrahmen.<br/>                 |
| [**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)                   | Legt die Prioritätsmischungsgewichtung fest, die vom Animationscontroller verwendet wird.<br/>                                                                          |
| [**SetTrackAnimationSet**](id3dxanimationcontroller--settrackanimationset.md)           | Wendet den Animationssatz auf die angegebene Spur an.<br/>                                                                                            |
| [**SetTrackDesc**](id3dxanimationcontroller--settrackdesc.md)                           | Legt die Trackbeschreibung fest.<br/>                                                                                                                  |
| [**SetTrackEnable**](id3dxanimationcontroller--settrackenable.md)                       | Aktiviert oder deaktiviert eine Spur im Animationscontroller.<br/>                                                                                     |
| [**SetTrackPosition**](id3dxanimationcontroller--settrackposition.md)                   | Legt die Spur auf die angegebene lokale Animationszeit fest.<br/>                                                                                        |
| [**SetTrackPriority**](id3dxanimationcontroller--settrackpriority.md)                   | Legt die Prioritätsmischungsgewichtung für die angegebene Animationsspur fest.<br/>                                                                         |
| [**SetTrackSpeed**](id3dxanimationcontroller--settrackspeed.md)                         | Legt die Trackgeschwindigkeit fest. Die Trackgeschwindigkeit ähnelt einem Multiplikator, der verwendet wird, um die Wiedergabe der Spur zu beschleunigen oder zu verlangsamen.<br/>            |
| [**SetTrackWeight**](id3dxanimationcontroller--settrackweight.md)                       | Legt die Spurgewichtung fest. Die Gewichtung wird verwendet, um zu bestimmen, wie mehrere Spuren kombiniert werden.<br/>                                                |
| [**UnkeyAllPriorityBlends**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Entfernt alle geplanten Prioritätsmischungsereignisse aus dem Animationscontroller.<br/>                                                                   |
| [**UnkeyAllTrackEvents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Entfernt alle Ereignisse aus einer angegebenen Animationsspur.<br/>                                                                                         |
| [**UnkeyEvent**](id3dxanimationcontroller--unkeyevent.md)                               | Entfernt ein angegebenes Ereignis aus einer Animationsspur, wodurch die Ausführung des Ereignisses verhindert wird.<br/>                                                    |
| [**UnregisterAnimationSet**](id3dxanimationcontroller--unregisteranimationset.md)       | Entfernt einen Animationssatz aus dem Animationscontroller.<br/>                                                                                      |
| [**Validateevent**](id3dxanimationcontroller--validateevent.md)                         | Überprüft, ob ein angegebenes Ereignishandle gültig ist und das Animationsereignis noch nicht abgeschlossen wurde.<br/>                                              |



 

## <a name="remarks"></a>Hinweise

Erstellen Sie mit [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md)ein Animationscontrollerobjekt.

Der LPD3DXANIMATIONCONTROLLER-Typ wird als Zeiger auf die **ID3DXAnimationController-Schnittstelle** definiert.


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



Der D3DXEVENTHANDLE-Typ ist als Ereignishandle für Animationscontrollerereignisse definiert.


```
typedef DWORD D3DXEVENTHANDLE;
```



Der LPD3DXEVENTHANDLE-Typ ist als Zeiger auf ein Ereignishandle für Animationscontrollerereignisse definiert.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
