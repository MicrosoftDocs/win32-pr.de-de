---
description: Beschreibt die Beziehung zwischen der Adapter Aktualisierungsrate und der Rate, mit der vorhandene oder vorhandene Vorgänge abgeschlossen werden. Diese Werte dienen auch als Flagwerte für das presentationintervalle-Feld von D3DCAPS9.
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b8bf496c8c8e10d50b23ad4f784634fb983d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353737"
---
# <a name="d3dpresent"></a>D3DPRESENT

Beschreibt die Beziehung zwischen der Adapter Aktualisierungsrate und der Rate, mit der [**vorhandene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) oder [**vorhandene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) Vorgänge abgeschlossen werden. Diese Werte dienen auch als Flagwerte für das presentationintervalle-Feld von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTFLIP"></span><span id="d3dpresent_donotflip"></span><dl> <dt><strong>D3DPRESENT_DONOTFLIP</strong></dt> </dl></td>
<td style="text-align: left;">Verwenden Sie den Front-Puffer als Quell-und Ziel Oberfläche während des Renderings. Eine Rahmen Synchronisierung ist geplant, aber die angezeigte Oberfläche ändert sich nicht. Dieses Flag ist nur verfügbar, wenn sich die Anwendung im Vollbildmodus befindet und D3DSWAPEFFECT_FLIPEX angegeben wurde. <br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl> <dt><strong>D3DPRESENT_DONOTWAIT</strong></dt> </dl></td>
<td style="text-align: left;">Eine Präsentation kann nicht von einem HAL-Gerät geplant werden. Wenn dieses Flag in einem-Aufrufe von " <a href="/windows/desktop/api"><strong>Present</strong></a>" festgelegt ist und die Hardware ausgelastet ist oder auf ein vertikales Synchronisierungs Intervall wartet, gibt Present D3DERR_WASSTILLDRAWING zurück, um anzugeben, dass der Blit-Vorgang unvollständig ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl> <dt><strong>D3DPRESENT_FLIPRESTART</strong></dt> </dl></td>
<td style="text-align: left;">Reserviert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl> <dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">D3DPRESENT_INTERVAL_IMMEDIATE wird bei diesem <a href="/windows/desktop/api"><strong>aktuellen</strong></a> -Befehl erzwungen. Dieses Flag kann nur bei Verwendung von D3DSWAPEFFECT_FLIPEX angegeben werden. Das Fenster Verhalten und das Verhalten der Vollbilddarstellung sind identisch. Dies ist besonders nützlich für Medien-apps, die Frames verwerfen möchten, die als spät erkannt wurden, und die nachfolgenden Frames zum Zeitpunkt der Komposition darstellen. Wenn dieses Flag nicht ordnungsgemäß angegeben ist, wird ein Fehler wegen eines ungültigen Parameters zurückgegeben. Wenn mehrere aufeinander folgende Frames mit D3DPRESENT_FORCEIMMEDIATEs in die Warteschlange eingereiht werden, wird nur der letzte Frame sowohl für die Fenster-als auch für die Vollbilddarstellung angezeigt.<br/> Dieses Flag ist in Direct3D 9Ex unter Betriebssystemen unter Windows 7 oder höher verfügbar.<br/> Wenn Sie D3DSWAPEFFECT_FLIPEX verwenden, setzt jeder Frame, der mit D3DPRESENT_INTERVAL_IMMEDIATE oder D3DPRESENT_INTERVAL_FORCEIMMEDIATE dargestellt wird, das aktuelle Intervall des vorherigen Frames außer Kraft. Wenn Sie z. b. die folgenden Frames mithilfe der folgenden Auslagerungs Effekte in die Warteschlange stellen: Frame A (D3DPRESENT_INTERVAL_ONE), Frame B (D3DPRESENT_INTERVAL_ONE), Frame c (D3DPRESENT_INTERVAL_ONE), Frame d (D3DPRESENT_INTERVAL_FORCEIMMEDIATE), Frame d überschreibt das vorhandene Intervall von Frame c. Die angezeigten Frames pro vorhandenes Intervall sind Frame A, Frame B, (von Frame C überschrieben durch) Frame D.<br/> Siehe Hinweise.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Dies entspricht fast dem D3DPRESENT_INTERVAL_ONE. Siehe Bemerkungen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den vertikalen Ablauf Verfolgungs Zeitraum (der Lauf Zeit Modul &quot; folgt &quot; , um das Zerreißen zu verhindern). <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge werden nicht häufiger beeinflusst als die Bildschirm Aktualisierung. die Laufzeit führt höchstens einen aktuellen Vorgang pro Adapter Aktualisierungs Zeitraum aus. Dies entspricht der Verwendung von D3DSWAPEFFECT_COPYVSYNC in DirectX 8,1. Diese Option ist immer für Fenster-und voll Bildaustausch Ketten verfügbar. Siehe Bemerkungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den Zeitraum für die vertikale neuverfolgung. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge werden nicht häufiger als jede zweite Bildschirm Aktualisierung beeinträchtigt. Überprüfen Sie die presentationintervalle-Obergrenze (siehe <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>), um festzustellen, ob D3DPRESENT_INTERVAL_TWO vom Treiber unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den Zeitraum für die vertikale neuverfolgung. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge werden nicht häufiger betroffen als jede dritte Bildschirm Aktualisierung. Überprüfen Sie die presentationintervalle-Obergrenze (siehe <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>), um festzustellen, ob D3DPRESENT_INTERVAL_THREE vom Treiber unterstützt wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den Zeitraum für die vertikale neuverfolgung. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge werden nicht häufiger betroffen als jede vierte Bildschirm Aktualisierung. Überprüfen Sie den presentationintervalle-Member (siehe <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>), um festzustellen, ob D3DPRESENT_INTERVAL_FOUR vom Treiber unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">Die Laufzeit aktualisiert den Fenster Client Bereich sofort und kann dies mehr als einmal während des Adapter Aktualisierungs Zeitraums durchführen. Dies entspricht der Verwendung von D3DSWAPEFFECT_COPY in DirectX 8. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge können sofort beeinträchtigt werden. Diese Option ist immer für Fenster-und voll Bildaustausch Ketten verfügbar. Siehe Bemerkungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl> <dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt> </dl></td>
<td style="text-align: left;">Der Inhalt des Hintergrund Puffers, der angezeigt werden soll, befindet sich im linearen Farbraum. <br/>
<ul>
<li>Die Darstellung konvertiert implizit von linearem Raum in sRGB (Gamma = 2,2). Dies ist die einzige unterstützte Konvertierung.</li>
<li>Da dieses Flag eine Eigenschaft des Inhalts des Hintergrund Puffers darstellt, kann das Flag während eines <a href="/windows/desktop/api"><strong>aktuellen</strong></a> Aufrufes angegeben werden. Anders ausgedrückt: eine Anwendung kann linearen Inhalt in einem Frame darstellen und dann in der nächsten zu korrigierten Inhalt wechseln.</li>
<li>Dieses Flag wird ignoriert, wenn die SwapChain den voll Bildschirm hat. (Beachten Sie, dass dieses Flag nur für die Version der expliziten austauschkette von <a href="/windows/desktop/api"><strong>vorhanden</strong></a>ist. Die <a href="/windows/desktop/api"><strong>aktuelle</strong></a> Methode nimmt keinen Flags-Parameter an.)</li>
<li>Dieses Flag wird immer akzeptiert, wird jedoch nur wirksam, wenn der Treiber >D3DCAPS3_LINEAR_TO_SRGB_PresentATION verfügbar macht.</li>
<li>Das einzige unterstützte Hintergrund Puffer Format ist <a href="d3dformat.md">X8R8G8B8</a>.</li>
</ul>
Siehe Fenster mit Fenster <a href="gamma.md">Austausch Ketten</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl> <dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt> </dl></td>
<td style="text-align: left;">Schneidet den gerenderten Inhalt auf den Monitor/das Gerät ab, auf den der Adapter ausgerichtet ist, und zeigt Miniaturansichten für den Inhalt in der Flip3D-Ansicht und in der Taskleiste auf anderen Monitoren <br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> Weitere Informationen zu diesem Feature von Windows Vista finden Sie unter <a href="/windows/desktop/dwm/dwm-overview">Desktopfenster-Manager</a> . Wenn Sie nicht im Desktop Kompositions Modus ausgeführt werden, gibt das-Flag das gleiche Verhalten wie <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP</a>.<br/>
<blockquote>
[!Note]<br />
Dieses Flag sollte nur mit Auslagerungs Effekt D3DSWAPEFFECT_FLIPEX verwendet werden. Die Verwendung dieses Flags mit <em>anderen</em> Auslagerungs Effekten wird als veraltet markiert und funktioniert möglicherweise nicht mehr in zukünftigen Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl> <dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt> </dl></td>
<td style="text-align: left;">Aktualisiert die Überlagerungs Position oder die Colorkey-Daten, ohne dass ein tatsächlicher Flip-Wert verursacht wird und die Dauer des Bilds nicht geändert wird.<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl> <dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt> </dl></td>
<td style="text-align: left;">Schaltet die Überlagerungs Hardware aus.<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl> <dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt> </dl></td>
<td style="text-align: left;">Zeichnet die Colorkey-Daten neu.<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Bemerkungen

Der Windowed-Modus unterstützt das D3DPRESENT \_ Interval \_ Default, das D3DPRESENT \_ Interval \_ immediate und das D3DPRESENT \_ Interval \_ 1. D3DPRESENT \_ Interval \_ default und das D3DPRESENT \_ Interval \_ eins sind fast Äquivalent (Weitere Informationen finden Sie unten in den Informationen zur Zeit Geber Auflösung). Sie führen auf ähnliche Weise \_ eine Kopie von VSYNC aus, da pro Frame nur eine vorhanden ist, und Sie verhindern, dass Sie mit dem folgenden strahlvorgang beendet werden. Im Gegensatz dazu \_ versucht D3DPRESENT Interval \_ immediate, eine unbegrenzte Präsentations Rate bereitzustellen.

Der Vollbildmodus unterstützt eine ähnliche Verwendung als Fenster-Modus, indem das D3DPRESENT- \_ Intervall \_ unabhängig von der Aktualisierungsrate oder dem Austausch Effekt unterstützt wird. D3DPRESENT \_ Interval \_ default verwendet die standardmäßige Systemzeit Geber Auflösung, während das D3DPRESENT- \_ Intervall \_ einen [**TimeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) aufruft, um die Auflösung des Systemzeit Gebers zu erhöhen. Dies verbessert die Qualität der vertikalen Synchronisierung, beansprucht jedoch etwas mehr Verarbeitungszeit. Beide Parameter versuchen, vertikal zu synchronisieren.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
