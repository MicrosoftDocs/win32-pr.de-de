---
description: Sehen Sie sich eine Kombination aus einem oder mehreren Flags an, die das Geräteerstellungsverhalten in der D3DCREATE-Konstante steuern.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cfd220e3fae2af079ba4eceba8f820a9267b4d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630228"
---
# <a name="d3dcreate"></a>D3DCREATE

Eine Kombination aus einem oder mehreren Flags, die das Erstellungsverhalten des Geräts steuern.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>Die Anwendung fordert das Gerät auf, alle Kopfteile zu steuern, die dieser Masteradapter besitzt. Das Flag ist auf Nichtmasteradaptern ungültig. Wenn dieses Flag festgelegt ist, sollten die an <a href="/windows/desktop/api"><strong>CreateDevice übergebenen</strong></a> Präsentationsparameter auf ein Array von <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>verweisen. Die Anzahl der Elemente in <strong>D3DPRESENT_PARAMETERS</strong> sollte der Anzahl der Adapter entsprechen, die vom NumberOfAdaptersInGroup-Element der <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9-Struktur</strong></a> definiert werden. Die DirectX-Runtime weist jedem Kopf jedes Element in der numerischen Reihenfolge zu, die vom AdapterOrdinalInGroup-Member von <strong>D3DCAPS9</strong>angegeben wird.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D verwaltet Ressourcen anstelle des Treibers. Direct3D-Aufrufe schlagen bei Ressourcenfehlern wie unzureichendem Videospeicher nicht fehl.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Wie D3DCREATE_DISABLE_DRIVER_MANAGEMENT verwaltet Direct3D Ressourcen anstelle des Treibers. Im Gegensatz zu D3DCREATE_DISABLE_DRIVER_MANAGEMENT gibt D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX Fehler für Bedingungen wie unzureichenden Videospeicher zurück.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Bewirkt, dass die Runtime keine Hotkeys für Printscreen registriert, Ctrl-Printscreen und Alt-Printscreen den Desktop- oder Fensterinhalt erfasst. 
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
<td>Unterschiede zwischen Windows XP und Windows Vista:<br/> Dieses Flag ist auf Windows Vista, Windows Server 2008 und Windows 7 verfügbar.<br/></td>
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
<td>Gibt die gemischte Vertexverarbeitung (software- und hardwareseitig) an. Für Windows 10 Version 1607 und höher wird die Verwendung dieser Einstellung nicht empfohlen. Weitere Informationen finden Sie unter D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Gibt die Verarbeitung von Softwarevertex an. Für Windows 10 Version 1607 und höher wird die Verwendung dieser Einstellung nicht empfohlen. Verwenden Sie D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
Sofern keine Hardwarevertexverarbeitung verfügbar ist, wird die Verwendung der Softwarevertexverarbeitung in Windows 10 Version 1607 (und höher) nicht empfohlen, da die Effizienz der Verarbeitung von Softwarevertex erheblich reduziert und gleichzeitig die Sicherheit der Implementierung verbessert wurde.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Gibt an, dass die Anwendung Direct3D anfordert, multithreadsicher zu sein. Dadurch übernimmt ein Direct3D-Thread häufiger den Besitz seines globalen <a href="/windows/desktop/Sync/critical-section-objects">kritischen Abschnitts,</a> was die Leistung beeinträchtigen kann. Wenn eine Anwendung Fenstermeldungen in einem Thread verarbeitet, während Direct3D-API-Aufrufe in einem anderen Thread erfolgen, muss die Anwendung dieses Flag beim Erstellen des Geräts verwenden. Dieses Fenster muss auch vor dem Entladen d3d9.dll zerstört werden.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Gibt an, dass Direct3D das Fokusfenster in keiner Weise ändern darf.
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
<td>Gibt an, dass Direct3D keine Get*-Aufrufe für alle Aufrufe unterstützt, die in Zustandsblöcken gespeichert werden können. Außerdem wird Direct3D angewiesen, keine Emulationsdienste für die Vertexverarbeitung bereitzustellen. Dies bedeutet, dass die Anwendung nur nachtransformationsbasierte Scheitelpunkte verwenden kann, wenn das Gerät die Scheitelpunktverarbeitung nicht unterstützt.</td>
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

 

 
