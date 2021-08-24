---
description: Die Direct3D 9-API funktioniert je nach installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreibermodell (XPDM) oder mit dem Windows Vista-Anzeigetreibermodell (WDDM).
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM im Vergleich zu WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0332198cd7c9425a3b5a107259dda1b1e974a04a2379244cdf939384260a89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746050"
---
# <a name="xpdm-vs-wddm"></a>XPDM im Vergleich zu WDDM

Die Direct3D 9-API funktioniert je nach installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreibermodell (XPDM) oder mit dem Windows Vista-Anzeigetreibermodell (WDDM). Es gibt einige Unterschiede im Verhalten der Direct3D-API für die beiden Treibermodelle.

-   [Sicherer Desktop](#secure-desktop)
-   [Remotedesktop](#remote-desktop)
-   [Windows-Dienst](#windows-service)
-   [Zugehörige Themen](#related-topics)

## <a name="secure-desktop"></a>Sicherer Desktop

Der sichere Desktop ist immer dann aktiv, wenn einer der folgenden Vorgänge auftritt: Der Benutzer sperrt den Desktop (Windows+L), der Bildschirmschoner wird aktiviert (wenn kein Benutzer angemeldet ist) oder standardmäßig, wenn die Benutzerkontensteuerung eine Eingabeaufforderung darstellt. Wenn der sichere Desktop aktiv ist, kann nicht auf das GERÄT zugegriffen werden.

Unterschiede zwischen XPDM und WDDM:

- Beim Versuch, ein Direct3D9-GERÄT zu erstellen, tritt ein Fehler auf **(D3DERR \_ NICHT \_ VERFÜGBAR),** und jedes vorhandene Direct3D 9-Gerät weist auf einen verloren gegangenen Geräterückgabecode auf Present hin.

- Direct3D9Ex- und Direct3D 10-APIs können erfolgreich ein Gerät erstellen, während der sichere Desktop aktiv ist, und alle Aufrufe von Present [**(IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) oder DXGI) geben einen Statuscode zurück, der angibt, dass der Desktop derzeit nicht verfügbar ist.



 

## <a name="remote-desktop"></a>Remotedesktop

Wenn ein Remotedesktop aktiv ist, wird die Anzeige vom Anzeigecomputer verarbeitet, wobei der Hostcomputer Informationen über das Netzwerk sendet.

Unterschiede zwischen XPDM und WDDM:

- Bei XPDM schlagen alle Versuche fehl, ein Direct3D 9-Gerät auf einem Remotedesktop zu erstellen.

- Auf WDDM unterstützt Remotedesktop das Erstellen eines LAMP-Geräts über eine Remotedesktopsitzung.



 

## <a name="windows-service"></a>Windows-Dienst

Ein Windows Dienst ist ein Prozess, der im Hintergrund ausgeführt wird und vom Dienststeuerungs-Manager (Service Control Manager, SCM) gesteuert wird. Ein Dienst wird unabhängig vom aktiven Desktop ausgeführt und kann daher nur eingeschränkt mit Benutzern interagieren.

Unterschiede zwischen XPDM und WDDM:

- Unter WDDM stellt die Sitzungs-0-Isolation sicher, dass ein Dienst keinen Zugriff auf Benutzerdesktops als Sicherheitsmaßnahme hat. Daher ist ein Direct3D 9-HALOGEN-Gerät nie über einen Windows-Dienst verfügbar.



 

> [!Note]  
> Direct3D 9 kann nicht in einem Windows Dienst verwendet werden. Weitere Informationen finden Sie im [Microsoft-Supportartikel 978635](https://support.microsoft.com/kb/978635).

 


In der folgenden Tabelle sind die hier aufgeführten Unterschiede zusammengefasst.



| Sicherer Desktop | Xpdm | WDDM (Direct3D9) | WDDM(Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| NULLREF         | Ja  | Ja              | Ja                          |
| Hal             | Nein   | Nein               | Ja                          |
| REF             | Ja  | Ja              | Ja                          |
| Remotedesktop  |      |                  |                              |
| NULLREF         | Nein   | Ja              | Ja                          |
| Hal             | Nein   | Ja              | Ja                          |
| REF             | Ja  | Ja              | Ja                          |
| Windows-Dienst |      |                  |                              |
| NULLREF         | Nein   | Nein               | Nein                           |
| Hal             | Nein   | Nein               | Nein                           |
| REF             | Nein   | Nein               | Nein                           |
| WARP10          | Nicht zutreffend  | –              | Ja                          |



 

Weitere Informationen zu XPDM, WDDM, Direct3D9Ex und Direct3D 10 finden Sie unter [Grafik-APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
