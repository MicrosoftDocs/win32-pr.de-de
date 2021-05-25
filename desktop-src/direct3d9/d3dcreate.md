---
description: Sehen Sie sich eine Kombination aus einem oder mehrere Flags an, die das Verhalten beim Erstellen des Geräts steuern.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d89043ac49b72bccf6279ef3c9c8fa2c856c775
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343228"
---
# <a name="d3dcreate"></a>D3DCREATE

Eine Kombination aus einem oder mehrere Flags, die das Verhalten beim Erstellen des Geräts steuern.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>Die Anwendung fordert das Gerät auf, alle Kopfköpfe zu fahren, die dieser Masteradapter besitzt. Das Flag ist für Nichtmasteradapter ungültig. Wenn dieses Flag festgelegt ist, sollten die an <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> übergebenen Präsentationsparameter auf ein Array <a href="d3dpresent-parameters.md"><strong>von</strong></a>D3DPRESENT_PARAMETERS. Die Anzahl der Elemente in <strong>D3DPRESENT_PARAMETERS</strong> der Anzahl von Adaptern, die durch das NumberOfAdaptersInGroup-Element der <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9-Struktur definiert</strong></a> werden. Die DirectX-Laufzeit weist jedem Kopf jedes Element in der numerischen Reihenfolge zu, die vom AdapterOrdinalInGroup-Mitglied <strong>von D3DCAPS9 angegeben wird.</strong></td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D verwaltet Ressourcen anstelle des Treibers. Direct3D-Aufrufe treten bei Ressourcenfehlern wie unzureichendem Videospeicher nicht auf.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Wie D3DCREATE_DISABLE_DRIVER_MANAGEMENT verwaltet Direct3D Ressourcen anstelle des Treibers. Im Gegensatz D3DCREATE_DISABLE_DRIVER_MANAGEMENT gibt D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX Fehler für Bedingungen wie unzureichenden Videospeicher zurück.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Bewirkt, dass die Runtime keine Hotkeys für Printscreen, Ctrl-Printscreen und Alt-Printscreen, um den Desktop- oder Fensterinhalt zu erfassen. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Beschränken Sie die Berechnung auf den Hauptanwendungsthread. Wenn das Flag nicht festgelegt ist, kann die Runtime softwarevertex processing and other computations in worker thread (Softwarevertexverarbeitung und andere Berechnungen im Arbeitsthread) ausführen, um die Leistung auf Systemen mit mehreren Prozessoren zu verbessern. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Windows XP und Windows Vista:<br/> Dieses Flag ist unter Windows Vista, Windows Server 2008 und Windows 7 verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Ermöglicht das Sammeln vorhandener Statistiken auf dem Gerät. Aufrufe von <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> geben gültige Daten zurück. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Legen Sie die Genauigkeit für Direct3D-Gleitkommaberechnungen auf die Genauigkeit fest, die vom aufrufenden Thread verwendet wird. Wenn Sie dieses Flag nicht angeben, verwendet Direct3D aus zwei Gründen standardmäßig den Modus "Round-to-Nearest" mit einfacher Genauigkeit:
<ul>
<li>Der Modus mit doppelter Genauigkeit reduziert die Direct3D-Leistung.</li>
<li>Bei Teilen von Direct3D wird davon ausgegangen, dass Gleitkommaeinheits-Ausnahmen maskiert sind. Das Aufheben derMaskatur dieser Ausnahmen kann zu undefiniertem Verhalten führen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Gibt die Hardwarevertexverarbeitung an.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Gibt die gemischte Vertexverarbeitung (software- und hardwareseitig) an. Für Windows 10 Version 1607 und höher wird die Verwendung dieser Einstellung nicht empfohlen. Siehe D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Gibt die Softwarevertexverarbeitung an. Für Windows 10 Version 1607 und höher wird die Verwendung dieser Einstellung nicht empfohlen. Verwenden D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
Sofern keine Hardwarevertexverarbeitung verfügbar ist, wird die Verwendung der Softwarevertexverarbeitung in Windows 10, Version 1607 (und höher), nicht empfohlen, da die Effizienz der Softwarevertexverarbeitung erheblich reduziert und gleichzeitig die Sicherheit der Implementierung verbessert wurde.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Gibt an, dass die Anwendung Direct3D als multithreadsicher angibt. Dadurch wird ein Direct3D-Thread <a href="/windows/desktop/Sync/critical-section-objects"></a> häufiger besitzer des globalen kritischen Abschnitts, was die Leistung beeinträchtigen kann. Wenn eine Anwendung Fenstermeldungen in einem Thread verarbeitet, während sie Direct3D-API-Aufrufe in einem anderen threadt, muss die Anwendung dieses Flag beim Erstellen des Geräts verwenden. Dieses Fenster muss auch zerstört werden, bevor sie d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Gibt an, dass Direct3D das Fokusfenster nicht ändern darf.
<div class="alert">
<blockquote>
[!Note]<br />
Wenn dieses Flag festgelegt ist, muss die Anwendung alle Fokusverwaltungsereignisse wie ALT+TAB und Mausklickereignisse vollständig unterstützen.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Gibt an, dass Direct3D keine Get*-Aufrufe für etwas unterstützt, das in Zustandsblöcken gespeichert werden kann. Außerdem weist direct3D an, keine Emulationsdienste für die Scheitelpunktverarbeitung zur Verfügung zu stellen. Dies bedeutet, dass die Anwendung nur nach transformierte Scheitelpunkte verwenden kann, wenn das Gerät die Scheitelpunktverarbeitung nicht unterstützt.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Ermöglicht Bildschirmschoner während einer Vollbildanwendung. Ohne dieses Flag deaktiviert Direct3D Bildschirmschoner, solange die aufrufende Anwendung vollbildig ist. Wenn die aufrufende Anwendung bereits ein Bildschirmschoner ist, hat dieses Flag keine Auswirkungen. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING, D3DCREATE \_ MIXED \_ VERTEXPROCESSING und D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING sind sich gegenseitig ausschließende Flags. Mindestens eines dieser Scheitelpunktverarbeitungsflags muss beim Aufrufen von [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)angegeben werden.

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         |  Wert          |
|--------------------------|------------|
| Header                   | D3D9.h     |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
