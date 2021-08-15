---
description: Beschreibt die Beziehung zwischen der Adapteraktualisierungsrate und der Rate, mit der aktuelle oder aktuelle Vorgänge abgeschlossen werden. Diese Werte dienen auch als Flagwerte für das Feld PresentationIntervals von D3DCAPS9.
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f3fd05609e86682b4524e68e985f03abac59f1dbd4537d1ffd683990ca371fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527590"
---
# <a name="d3dpresent"></a>D3DPRESENT

Beschreibt die Beziehung zwischen der Adapteraktualisierungsrate und der Rate, mit der [**aktuelle oder**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) [**aktuelle**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) Vorgänge abgeschlossen werden. Diese Werte dienen auch als Flagwerte für das Feld PresentationIntervals von [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

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
<td style="text-align: left;">Verwenden Sie den Frontpuffer während des Renderings sowohl als Quell- als auch als Zieloberfläche. Eine Framesynchronisierung ist geplant, aber die angezeigte Oberfläche ändert sich nicht. Dieses Flag ist nur verfügbar, wenn sich die Anwendung im Vollbildmodus befindet und D3DSWAPEFFECT_FLIPEX angegeben wurde. <br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl> <dt><strong>D3DPRESENT_DONOTWAIT</strong></dt> </dl></td>
<td style="text-align: left;">Eine Präsentation kann nicht von einem 12-Gerät geplant werden. Wenn dieses Flag in einem Aufruf von <a href="/windows/desktop/api"><strong>Present</strong></a>festgelegt wird und die Hardware mit der Verarbeitung beschäftigt ist oder auf ein vertikales Synchronisierungsintervall wartet, gibt Present D3DERR_WASSTILLDRAWING zurück, um anzugeben, dass der Blit-Vorgang unvollständig ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl> <dt><strong>D3DPRESENT_FLIPRESTART</strong></dt> </dl></td>
<td style="text-align: left;">Reserviert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl> <dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">D3DPRESENT_INTERVAL_IMMEDIATE wird für diesen <a href="/windows/desktop/api"><strong>Present-Aufruf</strong></a> erzwungen. Dieses Flag kann nur angegeben werden, wenn sie D3DSWAPEFFECT_FLIPEX. Das Darstellungsverhalten für Fenster und Vollbild ist identisch. Dies ist besonders nützlich für Medien-Apps, die Frames verwerfen möchten, die als spät erkannt wurden, und nachfolgende Frames zur Kompositionszeit präsentieren möchten. Wenn dieses Flag nicht ordnungsgemäß angegeben ist, wird ein Ungültiger Parameterfehler zurückgegeben. Wenn mehrere aufeinander folgende Frames mit D3DPRESENT_FORCEIMMEDIATEs in die Warteschlange eingereiht werden, wird nur der letzte Frame für die Darstellung im Fenstermodus und im Vollbildmodus angezeigt.<br/> Dieses Flag ist in Direct3D 9Ex unter Windows 7 oder höher verfügbar.<br/> Wenn Sie D3DSWAPEFFECT_FLIPEX, überschreibt jeder frame, der mit D3DPRESENT_INTERVAL_IMMEDIATE oder D3DPRESENT_INTERVAL_FORCEIMMEDIATE dargestellt wird, das aktuelle Intervall des vorherigen Frames. Wenn Sie z. B. die folgenden Frames mit den folgenden Auslagerungseffekten in die Warteschlange stellen: Frame A (D3DPRESENT_INTERVAL_ONE), Frame B(D3DPRESENT_INTERVAL_ONE), Frame C(D3DPRESENT_INTERVAL_ONE), Frame D(D3DPRESENT_INTERVAL_FORCEIMMEDIATE), überschreibt Frame D das aktuelle Intervall von Frame C. Die angezeigten Frames pro aktuellem Intervall sind Frame A, Frame B, (Frame C überschrieben von) Frame D.<br/> Siehe Hinweise.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Dies entspricht nahezu D3DPRESENT_INTERVAL_ONE. Siehe Bemerkungen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den vertikalen Rücksendezeitraum (die Laufzeit wird durch &quot; "ray &quot; follow" geblendet, um eine Tränkung zu verhindern). <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge sind nicht häufiger betroffen als die Bildschirmaktualisierung. Die Runtime schließt pro Aktualisierungszeitraum des Adapters nur einen Present-Vorgang ab. Dies entspricht der Verwendung D3DSWAPEFFECT_COPYVSYNC in DirectX 8.1. Diese Option ist immer sowohl für Fenster- als auch für Vollbild-Swapketten verfügbar. Siehe Bemerkungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den vertikalen Rückziehzeitraum. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge sind nicht häufiger betroffen als jede zweite Bildschirmaktualisierung. Überprüfen Sie die PresentationIntervals-Obergrenze (siehe <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>), um zu überprüfen, D3DPRESENT_INTERVAL_TWO Treiber unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den vertikalen Rückziehzeitraum. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge sind nicht häufiger betroffen als jede dritte Bildschirmaktualisierung. Überprüfen Sie die PresentationIntervals-Obergrenze (siehe <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>), um zu überprüfen, D3DPRESENT_INTERVAL_THREE Treiber unterstützt wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt> </dl></td>
<td style="text-align: left;">Der Treiber wartet auf den vertikalen Rückziehzeitraum. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge sind nicht häufiger betroffen als jede vierte Bildschirmaktualisierung. Überprüfen Sie das PresentationIntervals-Mitglied (siehe <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>), um zu überprüfen, D3DPRESENT_INTERVAL_FOUR Treiber unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">Die Runtime aktualisiert den Fensterclientbereich sofort und kann dies während des Aktualisierungszeitraums des Adapters mehr als einmal tun. Dies entspricht der Verwendung von D3DSWAPEFFECT_COPY in DirectX 8. <a href="/windows/desktop/api"><strong>Aktuelle</strong></a> Vorgänge können sofort betroffen sein. Diese Option ist immer sowohl für Fenster- als auch für Vollbild-Swapketten verfügbar. Siehe Bemerkungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl> <dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt> </dl></td>
<td style="text-align: left;">Der Inhalt des anzuzeigenden Hintergrundpuffers befindet sich im linearen Farbraum. <br/>
<ul>
<li>Die Präsentation konvertiert implizit aus dem linearen Raum in sRGB (gamma = 2,2). Dies ist die einzige Konvertierung, die unterstützt wird.</li>
<li>Da dieses Flag eine Eigenschaft des Inhalts des Hintergrundpuffers darstellt, kann das Flag während eines <a href="/windows/desktop/api"><strong>Present-Aufrufs angegeben</strong></a> werden. Anders ausgedrückt: Eine Anwendung kann linearen Inhalt in einem Frame präsentieren und dann im nächsten zu korrigiertem Inhalt wechseln.</li>
<li>Dieses Flag wird ignoriert, wenn die Auslagerungskette im Vollbildmodus angezeigt wird. (Beachten Sie, dass dieses Flag nur für die explizite Austauschkettenversion von <a href="/windows/desktop/api"><strong>Present verfügbar ist.</strong></a> Die <a href="/windows/desktop/api"><strong>Present-Methode</strong></a> akzeptiert keinen flags-Parameter.)</li>
<li>Dieses Flag wird immer akzeptiert, wird aber nur wirksam, wenn der Treiber >D3DCAPS3_LINEAR_TO_SRGB_PresentATION.</li>
<li>Das einzige unterstützte Backpufferformat ist <a href="d3dformat.md">X8R8G8B8.</a></li>
</ul>
Weitere Informationen <a href="gamma.md">finden Sie unter Windowed Swap Chains</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl> <dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt> </dl></td>
<td style="text-align: left;">Schneidet den gerenderten Inhalt an den Monitor/das Gerät aus, auf das der Adapter abzielen soll, zeigt Miniaturansichten für den Inhalt in der Flip3D-Ansicht und Miniaturansichten der Taskleiste auf anderen Monitoren an. <br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/> Weitere <a href="/windows/desktop/dwm/dwm-overview">Desktopfenster-Manager</a> zu diesem Feature von Windows Vista finden Sie unter Desktopfenster-Manager Vista. Wenn Sie nicht im Desktopkompositionsmodus ausführen, gibt das -Flag das gleiche Verhalten wie <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP.</a><br/>
<blockquote>
[!Note]<br />
Dieses Flag sollte nur mit swap-Effekten D3DSWAPEFFECT_FLIPEX. Die Verwendung dieses Flags <em>mit</em> anderen Swapeffekten ist veraltet und funktioniert in zukünftigen Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl> <dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt> </dl></td>
<td style="text-align: left;">Aktualisiert die Überlagerungsposition oder die Colorkey-Daten, ohne einen tatsächlichen Kippen zu verursachen und ohne die Dauer zu ändern, mit der das Bild angezeigt wird.<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl> <dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt> </dl></td>
<td style="text-align: left;">Schaltet die Überlagerungshardware aus.<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl> <dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt> </dl></td>
<td style="text-align: left;">Die Colorkey-Daten werden neu gedrammt.<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Hinweise

Der Fenstermodus unterstützt D3DPRESENT \_ INTERVAL \_ DEFAULT, D3DPRESENT \_ INTERVAL IMMEDIATE und \_ D3DPRESENT \_ INTERVAL \_ ONE. D3DPRESENT INTERVAL DEFAULT und D3DPRESENT INTERVAL ONE sind nahezu gleichwertig (siehe informationen \_ \_ zur \_ \_ Timerauflösung unten). Sie führen eine ähnliche Leistung wie COPY VSYNC durch, da nur eins pro Frame vorhanden ist, und sie verhindern das Abrenken \_ mit "balkenverknend". Im Gegensatz dazu versucht D3DPRESENT \_ INTERVAL \_ IMMEDIATE, eine unbegrenzte Präsentationsrate zu bieten.

Der Vollbildmodus unterstützt eine ähnliche Verwendung wie der Fenstermodus, indem D3DPRESENT INTERVAL IMMEDIATE unabhängig von der Aktualisierungsrate oder dem \_ \_ Swapeffekt unterstützt wird. D3DPRESENT INTERVAL DEFAULT verwendet die Standardmäßige Systemzeiterauflösung, während \_ \_ D3DPRESENT \_ INTERVAL \_ ONE [**timeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) aufruft, um die Systemzeiterauflösung zu verbessern. Dies verbessert die Qualität der vertikalen Synchronisierung, verbraucht jedoch etwas mehr Verarbeitungszeit. Beide Parameter versuchen, vertikal zu synchronisieren.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9.h</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
