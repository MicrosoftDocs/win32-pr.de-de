---
description: Die DXGI \_ PRESENT-Konstanten geben Optionen zum Präsentieren von Frames in der Ausgabe an.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84ce79d686aebd77e24a5be6facccd6fa4abd48e10bf15c07729a8ff6a0397bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796604"
---
# <a name="dxgi_present"></a>DXGI \_ PRESENT

Die **DXGI \_ PRESENT-Konstanten** geben Optionen zum Präsentieren von Frames in der Ausgabe an.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt><dt>0</dt> </dl></td>
<td style="text-align: left;">Stellen Sie einen Frame aus jedem Puffer (beginnend mit dem aktuellen Puffer) in der Ausgabe vor.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Stellen Sie einen Frame vom aktuellen Puffer bis zur Ausgabe vor. Verwenden Sie dieses Flag, damit die Präsentation die vertikale Leere-Synchronisierung verwenden kann, anstatt Puffer in der Kette wie gewohnt zu sequenzieren.<br/>
<blockquote>
[!Note]<br />
Wenn die aufrufende Anwendung die DXGI_PRESENT_DO_NOT_SEQUENCE-Konstante für den ersten aktuellen Vorgang (d. h. wenn kein aktueller Puffer vorhanden ist) legt, ignoriert die Runtime diesen aktuellen Vorgang und ruft den Treiber nicht auf.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">Stellen Sie den Frame nicht in der Ausgabe vor. Der Status der Auslagerungskette wird getestet, und es werden entsprechende Fehler zurückgegeben. DXGI_PRESENT_TEST ist nur für den Wechsel vom Leerlaufzustand vorgesehen. verwenden Sie ihn nicht, um zu bestimmen, wann in den Leerlaufzustand wechseln soll, da die Swapkette dadurch den Vollbildmodus nicht beenden kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Runtime ausstehende in der Warteschlange angezeigte -Daten verwirft.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x000000008UL</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Runtime bei der Präsentation einen Fehler verursacht (d. h. einen Aufruf von <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>) mit dem <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING-Fehlercode</a> fehlschlägt, wenn der aufrufende Thread blockiert ist. Die Runtime gibt DXGI_ERROR_WAS_STILL_DRAWING zurück, anstatt sich zu in den 100Er-Jahren zu befindet, bis die Abhängigkeit aufgelöst wird.<br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass Präsentationsinhalte nur für die bestimmte Ausgabe angezeigt werden. Der Inhalt ist in anderen Ausgaben nicht sichtbar. Wenn der Benutzer beispielsweise versucht, Videoinhalte in einer anderen Ausgabe zu verlagern, ist der Videoinhalt nicht sichtbar. <br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8. <br/>
<blockquote>
[!Note]<br />
Dieses Flag sollte nur mit <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect"></a> swap-Effekt DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL oder DXGI_SWAP_EFFECT_FLIP_DISCARD. Die Verwendung dieses <em>Flags</em> mit anderen Swapeffekten ist veraltet und funktioniert in zukünftigen Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass anstelle der Ansicht mit den linken Augen die Rechte-Augen-Ansicht verwendet wird, wenn die Stereo-Darstellung auf Mono reduziert werden muss.<br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Präsentation den linken Puffer als Monopuffer verwenden soll. Eine Anwendung ruft die <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1::IsTemporaryMonoSupported-Methode</strong></a> auf, um zu bestimmen, ob eine Austauschkette temporäre &quot; Mono &quot; unterstützt.<br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Dieses Flag muss von Medien-Apps festgelegt werden, die derzeit eine benutzerdefinierte aktuelle Dauer (benutzerdefinierte Aktualisierungsrate) verwenden. Siehe <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Dieser Wert wird ab Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">Das Zulassen von Reißern ist eine Anforderung für die Anzeige der variablen Aktualisierungsrate.<br/> Die Bedingungen für die Verwendung DXGI_PRESENT_ALLOW_TEARING present lauten wie folgt:<br/>
<ul>
<li>Die Auslagerungskette muss mit dem DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>erstellt</strong></a> werden.</li>
<li>Das an Present (oder <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1)</strong></a>übergebene Synchronisierungsintervall muss 0 sein. <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong></strong></a></li>
<li>Das DXGI_PRESENT_ALLOW_TEARING-Flag kann nicht in einer Anwendung verwendet werden, die sich derzeit im exklusiven Vollbildmodus befindet (festgelegt durch Aufrufen von <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState(TRUE)</strong></a>). Sie kann nur im Fenstermodus verwendet werden. Um dieses Flag in Win32-Vollbild-Apps zu verwenden, sollte die Anwendung in einem Vollbildfenster ohne Rand angezeigt werden und den automatischen Wechsel von ALT+EINGABE im Vollbildmodus mithilfe von <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory::MakeWindowAssociation deaktivieren.</strong></a> UWP-Apps, die durch Aufrufen von in den Vollbildmodus wechseln, sind rahmenlose Vollbildfenster und können <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> das Flag verwenden.</li>
</ul>
Wenn <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Sie Present</strong></a> (oder <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1)</strong></a>mit diesem Flag aufrufen und die oben genannten Bedingungen nicht erfüllen, DXGI_ERROR_INVALID_CALL Fehler an die aufrufende Anwendung zurückgegeben.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Präsentationsoptionen werden während des [**IDXGISwapChain::P resent-**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) oder [**IDXGISwapChain1::P resent1-Aufrufs**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) bereitgestellt. Die Puffer werden in der Beschreibung der Swapkette angegeben (siehe [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) oder [**DXGI SWAP CHAIN \_ \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).

DXGI \_ PRESENT RESTART ist nur für \_ Flip-Model-Austauschketten und Vollbildmodus gültig. Anwendungen können DXGI PRESENT RESTART verwenden, um eine Wiederherstellung nach Störungen bei der Wiedergabe und zum Verwerfen zuvor in der Warteschlange \_ \_ abgelegter Präsentationen zu ermöglichen. Das Verwerfen zuvor in der Warteschlange gespeicherter Präsentationen ist nützlich, wenn es sich bei diesen Präsentationen in der Warteschlange um Fensterszenarien handelt. Insbesondere könnte bei der darstellung in der Warteschlange angenommen worden sein, dass das Fenster eine alte Größe hat (d. h., nach der Übermittlung ist ein Größenvergrößerungsvorgang aufgetreten).

DXGI PRESENT RESTRICT TO OUTPUT ist nur für Austauschketten gültig, die eine bestimmte Ausgabe angegeben haben, um den Inhalt auf den Zeitpunkt der Erstellung dieser Swapketten zu beschränken \_ \_ ( \_ \_ [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Wenn es keine Ausgabe gibt, auf die beschränkt werden kann, ist das Flag ungültig.

DXGI PRESENT STEREO PREFER RIGHT gibt an, dass anstelle des linken \_ \_ \_ (Standard-) Auges das rechte Auge verwendet werden sollte, wenn das stereo-Present auf Mono \_ reduziert werden muss. Sie können dieses Flag verwenden, wenn eine Seite eine höhere Qualität hat (z. B. wenn das Stereopaar aus einem Standardbild synthetisiert wird).

DXGI PRESENT STEREO TEMPORARY MONO gibt an, dass der aktuelle den linken Puffer als \_ \_ \_ \_ Monopuffer verwenden soll. Sie können dieses Flag verwenden, um das Aktualisieren des richtigen Puffers zu vermeiden, wenn eine Anwendung vorübergehend keinen Stereoinhalt auf hat. Sie sollten dieses Flag nach Möglichkeit verwenden, da es eine erhebliche Optimierung durch das Betriebssystem ermöglicht und unter bestimmten Umständen sichtbaren Modusänderungsartefakten vermieden werden kann.

Sie sollten das DXGI PRESENT STEREO TEMPORARY MONO-Flag verwenden, um für die meisten Anwendungen, für die Sie erwarten, wieder Stereo zu verwenden, zu einer Mono-Austauschkette \_ \_ zu \_ \_ wechseln. Sie müssen die Verwendung dieses Flags in Anwendungen, die extrem lange ausgeführt werden oder selten Stereo anzeigen, gegen den Nachteil von nicht verwendetem Arbeitsspeicher ausgleichen.

> [!Note]  
> Vollbildanwendungen, die zu einer Mono-Austauschkette wechseln, verursachen eine Modusänderung, die in der Regel sichtbare Artefakte aufweise (z. B. "Blinken"). Temporäre Mono-Daten werden für Vollbild-Austauschketten jedoch möglicherweise nicht unterstützt.

 

Die DXGI \_ PRESENT \_ STEREO PREFER \_ \_ RIGHT- und DXGI \_ PRESENT STEREO TEMPORARY \_ \_ \_ MONO-Flags gelten nur für Stereo-Swapketten. Wenn Sie diese beim Präsentieren von Mono-Austauschketten verwenden, tritt ein ungültiger Vorgang auf.

Wenn Sie das DXGI PRESENT STEREO TEMPORARY MONO-Flag verwenden, wenn Sie eine Stereo-Swapkette präsentieren, die temporäres Mono nicht unterstützt, tritt ein Fehler auf, die Swapkette wird nicht angezeigt, und die Präsentation gibt \_ \_ \_ \_ [DXGI \_ ERROR INVALID \_ CALL \_ zurück.](dxgi-error.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
