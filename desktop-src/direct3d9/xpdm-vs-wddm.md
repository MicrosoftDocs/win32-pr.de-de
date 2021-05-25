---
description: Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreibermodell (XPDM) oder dem Windows Vista-Anzeigetreibermodell (Windows Vista Display Driver Model, WDDM).
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM im Vergleich zu WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343535"
---
# <a name="xpdm-vs-wddm"></a>XPDM im Vergleich zu WDDM

Die Direct3D 9-API funktioniert abhängig vom installierten Betriebssystem entweder mit dem Windows XP-Anzeigetreibermodell (XPDM) oder dem Windows Vista-Anzeigetreibermodell (Windows Vista Display Driver Model, WDDM). Es gibt einige Unterschiede im Verhalten der Direct3D-API bei den beiden Treibermodellen.

-   [Sicherer Desktop](#secure-desktop)
-   [Remotedesktop](#remote-desktop)
-   [Windows-Dienst](#windows-service)
-   [Verwandte Themen](#related-topics)

## <a name="secure-desktop"></a>Sicherer Desktop

Der sichere Desktop ist immer dann aktiv, wenn einer der folgenden Ereignisse auftritt: Der Benutzer sperrt seinen Desktop (Windows+L), der Bildschirmschoner wird aktiviert (wenn kein Benutzer angemeldet ist) oder standardmäßig, wenn die Benutzerkontensteuerung eine Eingabeaufforderung einleiten. Wenn der sichere Desktop aktiv ist, ist der Zugriff auf das HALOGEN-Gerät nicht möglich.

Unterschiede zwischen XPDM und WDDM:

- Beim Versuch, ein Direct3D9-GERÄT zu erstellen, ist ein Fehler **(D3DERR \_ \_ NICHT** VERFÜGBAR) möglich, und alle vorhandenen Direct3D 9-Geräte weisen auf einen verloren gegangenen Geräte-Rückgabecode auf Present hin.

- Direct3D9Ex- und Direct3D 10-APIs können erfolgreich ein Gerät erstellen, während der sichere Desktop aktiv ist, und alle Aufrufe von Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) oder DXGI) geben einen Statuscode zurück, der angibt, dass der Desktop derzeit nicht verfügbar ist.



 

## <a name="remote-desktop"></a>Remotedesktop

Wenn ein Remotedesktop aktiv ist, wird die Anzeige vom Anzeigecomputer verarbeitet, während der Hostcomputer Informationen über das Netzwerk sendet.

Unterschiede zwischen XPDM und WDDM:

- Unter XPDM sind alle Versuche, ein Direct3D 9-Gerät auf einem Remotedesktop zu erstellen, fehlgeschlagen.

- Auf WDDM unterstützt Remotedesktop das Erstellen eines HALOGEN-Geräts über eine Remotedesktopsitzung.



 

## <a name="windows-service"></a>Windows-Dienst

Ein Windows-Dienst ist ein Prozess, der im Hintergrund ausgeführt wird und vom Dienststeuerungs-Manager (Service Control Manager, SCM) gesteuert wird. Ein Dienst wird unabhängig vom aktiven Desktop ausgeführt und verfügt daher nur über eingeschränkte Möglichkeiten zur Interaktion mit Benutzern.

Unterschiede zwischen XPDM und WDDM:

- Unter WDDM stellt die Sitzungs-0-Isolation sicher, dass ein Dienst keinen Zugriff auf Benutzerdesktops als Sicherheitsmaßnahme hat. Daher ist ein Direct3D 9-MSI-Gerät nie über einen Windows-Dienst verfügbar.



 

> [!Note]  
> Direct3D 9 kann nicht in einem Windows-Dienst verwendet werden. Weitere Informationen finden Sie im [Microsoft-Supportartikel 978635.](https://support.microsoft.com/kb/978635)

 


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
| WARP10          | –  | –              | Ja                          |



 

Weitere Informationen zu XPDM, WDDM, Direct3D9Ex und Direct3D 10 finden Sie unter [Grafik-APIs in Windows.](../direct3darticles/graphics-apis-in-windows-vista.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
