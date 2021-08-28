---
description: Von D3DPRESENT PARAMETERS verwendete \_ Konstanten.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf3a8ad3a22f5104e4d4a78d3a01a29d07d757
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624556"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Konstanten, die von [**D3DPRESENT PARAMETERS \_ verwendet werden.**](d3dpresent-parameters.md)



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Wert</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device. D3DPRESENTFLAG_DEVICECLIP ist mit -D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Legen Sie dieses Flag fest, wenn das Gerät oder die Auslagerungskette erstellt wird, um das Z-Buffer-Verwerfen zu aktivieren. Wenn dieses Flag festgelegt ist, ist der Inhalt des Tiefen-Schablonenpuffers ungültig, nachdem entweder <a href="/windows/desktop/api"><strong>Present</strong></a>oder <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> mit einer anderen Tiefenoberfläche aufruft. Das Verwerfen von Z-Buffer-Daten kann die Leistung erhöhen und ist treiberabhängig. Die Debuglaufzeit erzwingt das Verwerfen, indem der Z-Puffer auf einen konstanten Wert gelöscht wird, nachdem entweder <a href="/windows/desktop/api"><strong>Present</strong></a>oder <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> mit einer anderen Tiefenoberfläche aufruft.<br/> Das Verwerfen von Z-Buffer-Daten ist für alle sperrbaren Formate, D3DFMT_D16_LOCKABLE und D3DFMT_D32F_LOCKABLE. Bei jeder Verwendung <a href="/windows/desktop/api"><strong>von CreateDevice,</strong></a> die ein sperrbares Format und Z-Buffer-Verwerfen anknt, kommt es zu einem Fehler. Weitere Informationen zu Formaten finden Sie unter <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Legen Sie dieses Flag fest, wenn die Anwendung die Möglichkeit erfordert, den Hintergrundpuffer direkt zu sperren. Beachten Sie, dass Hintergrundpuffer nur dann gesperrt werden können, wenn die Anwendung D3DPRESENTFLAG_LOCKABLE_BACKBUFFER <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> oder <a href="/windows/desktop/api"><strong>Reset angibt.</strong></a> Sperrbare Hintergrundpuffer führen bei einigen Grafikhardwarekonfigurationen zu Leistungskosten. Das Ausführen eines Sperrvorgang (oder der <a href="/windows/desktop/api"><strong>Verwendung von UpdateSurface</strong></a> zum Schreiben) für den sperrbaren Hintergrundpuffer verringert die Leistung auf vielen Karten. Ziehen Sie in diesem Fall die Verwendung von strukturierten Dreiecken in Betracht, um Daten in den Hintergrundpuffer zu verschieben.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> In Direct3D9Ex kann dieses Flag nicht festgelegt werden, wenn D3DSWAPEFFECT D3DSWAPEFFECT_FLIPEX ist, da das Flip-Modell dem Desktopfenster-Manager den Zugriff auf den Zurückpuffer einer Anwendung ermöglicht. Eine prozessübergreifende freigegebene Oberfläche sollte nicht gesperrt werden.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Rotierte Monitore werden während der Präsentation automatisch mit einer rotierenden Kopie verarbeitet, was nicht sehr effizient ist. Dieses Flag bedeutet, dass die Anwendung eine eigene Anzeigerotation vor sich geht. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Anwendungen können ihre eigene Drehung möglicherweise mithilfe einer gedrehten Ansichtsmatrix erreichen. Die Methoden <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> und <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> sollten verwendet werden, um die aktuelle Drehungseinstellung zu finden. Die Parameter für Breite und Höhe des Hintergrundpuffers in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> und <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> müssen die Querformatierung verwenden, während die Vollbildmodusstruktur mit der von <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> zurückgegebenen Struktur identisch sein sollte (d. h. Breite und Höhe werden ausgetauscht, wenn sie um 90 und 270 Grad gedreht werden).</p>
<p>Bei Verwendung von Sperren für gedrehte Renderziele sind Annahmen in der oberen linken Ecke nicht mehr wahr, das Renderziel SURFACE_DESC bleibt querformatiert (wie durch die Erstellungsparameter impliziert), und GDI-Fenster, Mauskoordinaten und solche müssen ordnungsgemäß übersetzt werden, wenn sie mit dem Direct3D-Renderziel und der Direct3D-Renderszene verwendet werden.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Verwenden Sie dieses Flag, um einen vom Adapter aufzählten RAW-Anzeigemodus anzugeben, obwohl Direct3D möglicherweise angegeben hat, dass der Modus ungültig ist. Die Anwendung sollte dies robust implementieren, falls der gewünschte Modus tatsächlich ungültig ist. 
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
<td>Dies ist ein Hinweis an den Treiber, dass die Hintergrundpuffer Videodaten enthalten.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Gibt an, ob es sich bei der Überlagerung um einen RGB-Vollbereich oder um rgb-Bereich mit eingeschränktem Bereich handelt. Das Festlegen dieses Flags gibt den begrenzten Bereich RGB an. In einem begrenzten Bereich von RGB wird der RGB-Bereich so komprimiert, dass 16:16:16 schwarz und 235:235:235 weiß ist.
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
<td>Gibt an, ob die Überlagerung BT.601 oder BT.709 ist. Wenn Sie dieses Flag festlegen, wird BT.709 für high-definition TV (GS) angegeben.
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
<td>Gibt an, ob die Überlagerung konventioneller YCbCr oder erweiterter YCbCr (xvYCC) ist. Das Festlegen dieses Flags gibt die erweiterte YCbCr (xvYCC) an.
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
<td>Das Festlegen dieses Flags gibt an, dass die Swapchain geschützten Inhalt enthält und bewirkt automatisch, dass die Runtime den Zugriff auf die Swapchain einschränkt, sodass nur der Desktop Windows Manager (DWM) die Swapchain verwenden kann.
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
<td>Das Festlegen dieses Flags gibt an, dass der Treiber den Zugriff auf alle freigegebenen Ressourcen einschränken soll, die für die DWM-Interaktion erstellt werden. Der Aufrufer muss einen authentifizierten Kanal mit dem Treiber erstellen. Der Treiber sollte dann den Zugriff auf Prozesse zulassen, die versuchen, diese freigegebenen Ressourcen zu öffnen.
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



 

Diese Konstanten werden von [**D3DPRESENT PARAMETERS \_ verwendet.**](d3dpresent-parameters.md)

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3d9types.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




