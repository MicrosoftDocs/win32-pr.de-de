---
description: Beschreibt vorhandenes SwapChain-Statistiken im Zusammenhang mit presentex-aufrufen.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: D3DPRESENTSTATS-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219566"
---
# <a name="d3dpresentstats-structure"></a>D3DPRESENTSTATS-Struktur

Beschreibt vorhandenes SwapChain-Statistiken im Zusammenhang mit [**presentex**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) -aufrufen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a>Member

<dl> <dt>

**Presentcount**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl erfolgreicher Aufrufe, die von einem Anzeigegerät ausgeführt werden, das derzeit auf den Bildschirm aussteht. Dieser Parameter ist tatsächlich die aktuelle ID des letzten aktuellen Aufrufs und ist nicht notwendigerweise die Gesamtzahl der vorhandenen API-Aufrufe.

</dd> <dt>

**Presenterfrischend-Anzahl**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die vblank-Anzahl, bei der das letzte vorhanden sein auf dem Bildschirm angezeigt wurde, die vblank-Anzahl wird nach jedem vblank-Intervall erhöht.

</dd> <dt>

**Synkrefreshcount**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die vblank-Anzahl, wenn der Planer die Zeit des Zeit Planungs Moduls zuletzt durch Aufrufen von QueryPerformanceCounter erfasst hat.

</dd> <dt>

**Syncqpctime**
</dt> <dd>

Typ: **[ **große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Die Zeit des Zeit Planungs Moduls für den letzten Sampling, abgerufen durch Aufrufen von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> <dt>

**Syncgputime**
</dt> <dd>

Typ: **[ **große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn eine 9Ex-Anwendung den Flip-Modus annimmt (D3DSWAPEFFECT \_ flipex), können Anwendungen das Löschen von Frames erkennen, indem Sie getpresentstatistics zu einem beliebigen Zeitpunkt aufrufen. In der Tat können Sie die folgenden Aktionen ausführen:

1.  In den Hintergrund Puffer Rendering
2.  Aufrufe vorhanden
3.  Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern
4.  Den nächsten Frame in den Hintergrund Puffer Rendering
5.  Aufrufe vorhanden
6.  Wiederholen Sie die Schritte 4 und 5 1 oder mehrmals.
7.  Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern
8.  Vergleichen Sie die Werte von presenterfrischendes count aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen. Die Anwendung kann die entsprechende presenterfrischend-Anzahl eines bestimmten presentcount-Parameters basierend auf den Annahmen der presenterfrischendes count Inkrement-und presentcount-Zuweisung von Frame-Vorstellungen berechnen. Wenn die Anzahl der zuletzt erfassten Präsentationen nicht mit der presentcount-Entsprechung identisch ist (d. h., wenn die presentaktuationszahl inkrementiert wurde, aber presentcount nicht, gab es einen Frame, der gelöscht wurde

Anwendungen können bestimmen, ob ein Frame durch Sampling zweier Instanzen von presentcount und getpresentstats (durch Aufrufen der getpresentstats-API zu einem beliebigen Zeitpunkt) gelöscht wurde. Beispielsweise möchte eine Medien Anwendung, die mit derselben Rate wie die Aktualisierungsrate des Monitors (z. b. Monitor Aktualisierungsrate ist 60Hz), die Anwendung einen Frame alle 1/60 Sekunden anzeigt, die Frames a, B, C, D, E darstellen, die jeweils den vorhandenen IDs entsprechen (presentcount) 1, 2, 3, 7, 8.

Der Anwendungscode sieht wie die folgende Sequenz aus.

1.  Rendering von Frame A in den Hintergrund Puffer
2.  Aufrufe vorhanden, presentcount = 1
3.  Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern
4.  Rendering der nächsten 4 Frames, B, C, D, E bzw.
5.  Der-Rückruf ist viermal verfügbar, presentcounts = 2, 3, 7, 8.
6.  Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern
7.  Vergleichen Sie die Werte von presenterfrischendes count aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen. Wenn der Unterschied 2 ist, d. h. zwei vblank-Intervalle zwischen den beiden getpresentstats-API-aufrufen verstrichen sind, sollte der letzte dargestellte Frame Frame C lauten. Da die Anwendung ein sehr vleeres Intervall (die Aktualisierungsrate des Monitors) darstellt, ist die verstrichene Zeit zwischen dem Zeitpunkt, an dem Frame A dargestellt wird, und dem Zeitpunkt, an dem Frame C dargestellt wird, 2 vblank.
8.  Vergleichen Sie die Werte von presentcount aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen. Wenn der erste presentcount 1 ist (entspricht Frame A) und der zweite presentcount 3 (entsprechend Frame C), wurden keine Frames gelöscht. Wenn das zweite presentcount-Element 3 ist, das Frame D entspricht, weiß die Anwendung, dass ein Frame gelöscht wurde.

Beachten Sie, dass getpresentstatistics nach dem Aufruf verarbeitet wird, unabhängig vom Status der Ansichts Aufrufe des flipex-Modus.

**Windows Vista:** Die aktuellen Aufrufe werden in die Warteschlange eingereiht und dann verarbeitet, bevor der getpresentstats-Aufruf verarbeitet wird.

Wenn eine Anwendung erkennt, dass die Darstellung bestimmter Frames dahinter steht, können diese Frames übersprungen und die Präsentation korrigiert werden, um die erneute Synchronisierung mit vblank durchzusetzen. Zu diesem Zweck kann eine Anwendung die späten Frames einfach nicht Rendern und das Rendering mit dem nächsten richtigen Frame in der Warteschlange starten. Wenn eine Anwendung jedoch bereits mit dem Rendern von späten Frames begonnen hat, kann Sie einen neuen Present-Parameter in D3D9Ex namens D3DPRESENT \_ forceimvermittler verwenden. Das Flag wird in den Parametern des aktuellen API-Aufrufes ausgegeben und gibt der Laufzeit an, dass der Frame direkt innerhalb des nächsten vblank-Intervalls verarbeitet wird, was auf dem Bildschirm überhaupt nicht sichtbar ist. Im folgenden finden Sie das Beispiel für die Anwendungs Verwendung nach dem letzten Schritt im vorherigen Beispiel.

1.  Den nächsten Frame in den Hintergrund Puffer Rendering
2.  Entdecken Sie aus presenterfrischen count, dass der nächste Frame bereits spät ist.
3.  Festlegen des aktuellen Intervalls auf D3DPRESENT \_ forceimvermittler
4.  Auf dem nächsten Frame vorhandener aufzurufen

Anwendungen können Video-und Audiostreams auf die gleiche Weise synchronisieren, da sich das Verhalten von getpresentstatistics in diesem Szenario nicht ändert.

Der D3D9Ex Flip-Modus stellt Frame Statistik Informationen für Fenster Anwendungen und Vollbild-9Ex-Anwendungen bereit.

**Windows Vista:** Verwenden Sie die DWM-APIs zum Abrufen der aktuellen Statistik.

Wenn Desktopfenster-Manager ausgeschaltet ist, erhalten die Anwendungen im Fenstermodus 9Ex, die den Flip-Modus verwenden, die Statistik Informationen mit eingeschränkter Genauigkeit.

* * Windows Vista: * *

Wenn eine Anwendung nicht schnell genug ist, um mit der Aktualisierungsrate des Monitors Schritt zu halten, möglicherweise aufgrund langsamer Hardware oder fehlender Systemressourcen, kann ein Grafik-glitch angezeigt werden. Ein Störung ist ein so genanntes visuelles Element. Wenn ein Monitor bei 60 Hz auf Refresh festgelegt ist und die Anwendung nur 30 FPS verwalten kann, werden für die Hälfte der Rahmen ein Fehler angezeigt.

Anwendungen können einen Fehler erkennen, indem Sie die synchrone Anzahl verfolgen. Beispielsweise kann eine Anwendung die folgende Sequenz von Aktionen ausführen.

1.  In den Hintergrund Puffer Rendering.
2.  Aufrufe vorhanden.
3.  Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern.
4.  Den nächsten Frame in den Hintergrund Puffer Rendering.
5.  Aufrufe vorhanden.
6.  Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern.
7.  Vergleichen Sie die Werte von synkrefreshcount aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen. Wenn der Unterschied größer als 1 ist, wurde ein Frame übersprungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
