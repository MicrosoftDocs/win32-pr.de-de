---
description: Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreiber Modell (XPDM) oder dem Windows Vista-Anzeigetreiber Modell (WDDM).
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM im Vergleich zu WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343932"
---
# <a name="xpdm-vs-wddm"></a>XPDM im Vergleich zu WDDM

Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreiber Modell (XPDM) oder dem Windows Vista-Anzeigetreiber Modell (WDDM). Es gibt einige Unterschiede in der Art und Weise, wie sich die Direct3D-API auf die beiden Treiber Modelle verhält.

-   [Sicherer Desktop](#secure-desktop)
-   [Remotedesktop](#remote-desktop)
-   [Windows-Dienst](#windows-service)
-   [Zugehörige Themen](#related-topics)

## <a name="secure-desktop"></a>Sicherer Desktop

Der sichere Desktop ist aktiv, wenn eine der folgenden Aktionen auftritt: der Benutzer sperrt den Desktop (Windows + L), der Bildschirmschoner wird aktiviert (wenn kein Benutzer angemeldet ist) oder standardmäßig, wenn die Benutzerkontensteuerung eine Eingabeaufforderung anzeigt. Wenn der sichere Desktop aktiv ist, kann nicht auf das HAL-Gerät zugegriffen werden.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen XPDM und WDDM:<br/> Beim Versuch, ein von Direct3D9 HAL-Gerät zu erstellen, tritt ein Fehler auf (mit **D3DERR \_ nicht \_ verfügbar**), und jedes vorhandene Direct3D 9-Gerät weist auf einen verlorenen Geräte Rückgabecode hin.<br/> Die APIs Direct3D9Ex und Direct3D 10 können ein Gerät erfolgreich erstellen, während der sichere Desktop aktiv ist, und alle Aufrufe an Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) oder DXGI) geben einen Statuscode zurück, der anzeigt, dass der Desktop zurzeit nicht verfügbar ist.<br/> |



 

## <a name="remote-desktop"></a>Remotedesktop

Wenn ein Remote Desktop aktiv ist, wird die Anzeige vom Computer mit dem hostingcomputer behandelt, der Informationen über das Netzwerk sendet.



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen XPDM und WDDM:<br/> Bei XPDM tritt bei allen versuchen, ein Direct3D 9-Gerät auf einem Remote Desktop zu erstellen, ein Fehler auf.<br/> Auf WDDM unterstützt Remote Desktop das Erstellen eines HAL-Geräts über eine Remote Desktop Sitzung.<br/> |



 

## <a name="windows-service"></a>Windows-Dienst

Ein Windows-Dienst ist ein Prozess, der im Hintergrund ausgeführt wird, der vom Dienststeuerungs-Manager (Service Control Manager, SCM) gesteuert wird. Ein Dienst wird unabhängig vom aktiven Desktop ausgeführt und verfügt daher über eingeschränkte Möglichkeiten zur Interaktion mit Benutzern.



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen XPDM und WDDM:<br/> Bei WDDM stellt die Isolation der Sitzung 0 sicher, dass ein Dienst nicht als Sicherheitsmaßnahme auf einen Benutzer Desktop zugreifen kann. aus diesem Grund ist ein Direct3D 9 HAL-Gerät nie über einen Windows-Dienst verfügbar.<br/> |



 

> [!Note]  
> Sie können Direct3D 9 nicht in einem Windows-Dienst verwenden. Weitere Informationen finden Sie im [Microsoft Support-Artikel 978635](https://support.microsoft.com/kb/978635).

 


In der folgenden Tabelle werden die hier aufgeführten Unterschiede zusammengefasst.



|                 | XPDM | WDDM (von Direct3D9) | WDDM (Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| Sicherer Desktop  |      |                  |                              |
| NullRef         | Ja  | Ja              | Ja                          |
| Hale             | Nein   | Nein               | Ja                          |
| REF             | Ja  | Ja              | Ja                          |
| Remotedesktop  |      |                  |                              |
| NullRef         | Nein   | Ja              | Ja                          |
| Hale             | Nein   | Ja              | Ja                          |
| REF             | Ja  | Ja              | Ja                          |
| Windows-Dienst |      |                  |                              |
| NullRef         | Nein   | Nein               | Nein                           |
| Hale             | Nein   | Nein               | Nein                           |
| REF             | Nein   | Nein               | Nein                           |
| WARP10          | –  | –              | Ja                          |



 

Weitere Informationen zu XPDM, WDDM, Direct3D9Ex und Direct3D 10 finden Sie unter [Grafik-APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
