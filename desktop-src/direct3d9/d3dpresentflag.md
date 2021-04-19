---
description: Von D3DPRESENT- \_ Parametern verwendete Konstanten.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346225"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Von D3DPRESENT- [**\_ Parametern**](d3dpresent-parameters.md)verwendete Konstanten.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Schneiden Sie ein Fenster <a href="/windows/desktop/api"><strong></strong></a> aus, das sich im Fenster Client Bereich befindet, und zwar im Bildschirmbereich des Monitors der Grafikkarte, von der das Direct3D-Gerät erstellt wurde. D3DPRESENTFLAG_DEVICECLIP ist mit D3DSWAPEFFECT_FLIPEX ungültig.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Legen Sie dieses Flag fest, wenn das Gerät oder die Swapkette erstellt wird, um z-Puffer-verwerfen zu aktivieren. Wenn dieses Flag festgelegt ist, ist der Inhalt des tiefen Schablone-Puffers nach dem Aufrufen von " <a href="/windows/desktop/api"><strong>Present</strong></a>" oder " <a href="/windows/desktop/api"><strong>setdepthstencilsurface</strong></a> " mit einer anderen tiefen Oberfläche ungültig. Das Verwerfen von z-Puffer Daten kann die Leistung erhöhen und ist Treiber abhängig. Die Debug-Laufzeit erzwingt das verwerfen, indem Sie den z-Puffer auf einen konstanten Wert nach dem Aufruf von " <a href="/windows/desktop/api"><strong>Present</strong></a>" oder " <a href="/windows/desktop/api"><strong>setdepthstencilsurface</strong></a> " mit einer anderen tiefen Oberfläche löscht.<br/> Das Verwerfen von z-Puffer Daten ist für alle Sperr baren Formate, D3DFMT_D16_LOCKABLE und D3DFMT_D32F_LOCKABLE nicht zulässig. Jede Verwendung von " <a href="/windows/desktop/api"><strong>kreatedevice</strong></a> ", die ein Sperr bares Format und z-Puffer-verwerfen angibt, schlägt fehl. Weitere Informationen zu Formaten finden Sie unter <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Legen Sie dieses Flag fest, wenn die Anwendung die Möglichkeit erfordert, den Hintergrund Puffer direkt zu sperren. Beachten Sie, dass die Back Puffer nicht sperrbar sind, es sei denn, die Anwendung gibt D3DPRESENTFLAG_LOCKABLE_BACKBUFFER beim Aufrufen von <a href="/windows/desktop/api"><strong>createdevice</strong></a> <a href="/windows/desktop/api"><strong>an oder setzt</strong></a> Sperr Bare Sicherungs Puffer verursachen bei manchen Grafikhardware Konfigurationen Leistungseinbußen. Durch das Ausführen eines Sperr Vorgangs (oder mithilfe von <a href="/windows/desktop/api"><strong>updatesurface</strong></a> zum Schreiben) auf dem Sperr baren Hintergrund wird die Leistung auf vielen Karten verringert. In diesem Fall sollten Sie die Verwendung von Text Dreiecken zum Verschieben von Daten in den Hintergrund Puffer in Erwägung ziehen.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> In Direct3D9Ex kann dieses Flag nicht festgelegt werden, wenn der D3DSWAPEFFECT-Wert D3DSWAPEFFECT_FLIPEX ist, da das Flip-Modell dem Desktopfenster-Manager den Zugriff auf den Hintergrund Puffer einer Anwendung ermöglicht. Eine prozessübergreifende, freigegebene Oberfläche sollte nicht gesperrt werden.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Gedrehte Monitore werden bei der Präsentation automatisch mit einer rotierenden Kopie behandelt, was nicht sehr effizient ist. Dieses Flag bedeutet, dass die Anwendung die eigene Anzeigedrehung ausführt. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Anwendungen können eine eigene Drehung erzielen, indem Sie möglicherweise eine gedrehte Ansichts Matrix verwenden. Die Methoden <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>getdisplaymodeex</strong></a> und <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>getadapterdisplaymodeex</strong></a> sollten verwendet werden, um die aktuelle Rotations Einstellung zu ermitteln. Die Parameter "width" und "Height" in " <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>kreatedeviceex</strong></a> " und " <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>rectex</strong></a> " müssen in der Querformat Ausrichtung verwendet werden, während die Struktur des Vollbild-Anzeigemodus identisch mit der Rückgabe von " <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>enumadaptermodesex</strong></a> " ist (d. h., wenn 90 und 270 Grad gedreht werden, werden Breite und Höhe ausgetauscht).</p>
<p>Bei Verwendung der Lock-Klausel für gedrehte Renderziele sind linke obere Ecke nicht mehr true. Das Renderziel SURFACE_DESC bleibt Querformat (wie durch die Erstellungs Parameter impliziert) und GDI-Fenster, Maus Koordinaten und muss bei Verwendung mit dem Direct3D-Renderziel und der Szene ordnungsgemäß übersetzt werden.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Verwenden Sie dieses Flag, um alle vom Anzeige Adapter aufgelisteten unformatierten Anzeigemodi anzugeben, auch wenn Direct3D möglicherweise angibt, dass der Modus ungültig ist. Die Anwendung sollte dies auf robuste Weise implementieren, falls der gewünschte Modus wirklich ungültig ist. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>Dies ist ein Hinweis für den Treiber, dass die Hintergrund Puffer Videodaten enthalten.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Gibt an, ob die Überlagerung den vollen Bereich RGB oder den begrenzten Bereich RGB hat. Das Festlegen dieses Flags gibt den begrenzten Bereich RGB an. Im begrenzten Bereich RGB wird der RGB-Bereich so komprimiert, dass 16:16:16 schwarz und 235:235:235 weiß ist.
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>Gibt an, ob die Überlagerung BT. 601 oder BT. 709 ist. Wenn dieses Flag festgelegt wird, wird "BT. 709" für High-Definition TV (HDTV) angegeben.
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>Gibt an, ob die Überlagerung konventionelle YCbCr oder Extended YCbCr (xwycc) ist. Wenn dieses Flag festgelegt wird, wird der erweiterte YCbCr (xwycc) angegeben.
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>Das Festlegen dieses Flags gibt an, dass die vorhandenes SwapChain geschützte Inhalte enthält und automatisch bewirkt, dass die Laufzeit den Zugriff auf die vorhandenes SwapChain einschränkt, sodass nur der Desktop-Windows-Manager (DWM) vorhandenes SwapChain verwenden kann.
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
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>Wenn dieses Flag festgelegt wird, wird der Zugriff auf freigegebene Ressourcen, die für die DWM-Interaktion erstellt werden, durch den Treiber eingeschränkt. Der Aufrufer muss einen authentifizierten Kanal mit dem Treiber erstellen. Der Treiber sollte dann den Zugriff auf Prozesse zulassen, die versuchen, diese freigegebenen Ressourcen zu öffnen.
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



 

Diese Konstanten werden von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types. h |
| Mindestens Betriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




