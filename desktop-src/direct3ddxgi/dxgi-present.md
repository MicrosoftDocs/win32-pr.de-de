---
description: Die vorhandenen DXGI- \_ Konstanten geben Optionen zum Darstellen von Frames für die Ausgabe an.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366634"
---
# <a name="dxgi_present"></a>DXGI \_ vorhanden

Die **\_ vorhandenen DXGI** -Konstanten geben Optionen zum Darstellen von Frames für die Ausgabe an.



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
<td style="text-align: left;">Stellt einen Frame aus jedem Puffer (beginnend mit dem aktuellen Puffer) für die Ausgabe dar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002ul</dt> </dl></td>
<td style="text-align: left;">Stellt einen Frame vom aktuellen Puffer zur Ausgabe dar. Verwenden Sie dieses Flag, damit die Präsentation vertikal leere Synchronisierungen verwenden kann, anstatt Puffer in der Kette auf die übliche Weise zu sequenzieren.<br/>
<blockquote>
[!Note]<br />
Wenn die aufrufende Anwendung die DXGI_PRESENT_DO_NOT_SEQUENCE Konstante beim ersten aktuellen Vorgang festlegt (d. h., wenn kein aktueller Puffer vorhanden ist), ignoriert die Laufzeit diesen Vorgang und ruft den Treiber nicht auf.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001ul</dt> </dl></td>
<td style="text-align: left;">Stellen Sie den Frame nicht für die Ausgabe dar. Der Status der Austausch Kette wird getestet, und es werden entsprechende Fehler zurückgegeben. DXGI_PRESENT_TEST ist nur für die Verwendung vorgesehen, wenn aus dem Leerlauf gewechselt wird. Verwenden Sie ihn nicht, um zu bestimmen, wann in den Leerlauf wechselt, da dadurch die SwapChain nicht mehr den Vollbildmodus beenden kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004ul</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Laufzeit ausstehende vorgestellte in der Warteschlange verwerfen wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008ul</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Laufzeit die Präsentation fehlschlägt (d. h. einen Aufruf von <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>) mit dem <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> Fehlercode fehlschlägt, wenn der aufrufende Thread blockiert ist. die Laufzeit gibt DXGI_ERROR_WAS_STILL_DRAWING zurück, anstatt zu warten, bis die Abhängigkeit aufgelöst wird.<br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8 unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010ul</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass Präsentations Inhalte nur für die jeweilige Ausgabe angezeigt werden. Der Inhalt wird in anderen Ausgaben nicht angezeigt. Wenn der Benutzer z. b. versucht, Videoinhalte in einer anderen Ausgabe zu verschieben, wird der Videoinhalt nicht angezeigt. <br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8 unterstützt. <br/>
<blockquote>
[!Note]<br />
Dieses Flag sollte nur mit Auslagerungs Effekten <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> oder DXGI_SWAP_EFFECT_FLIP_DISCARD verwendet werden. Die Verwendung dieses Flags mit <em>anderen</em> Auslagerungs Effekten wird als veraltet markiert und funktioniert möglicherweise nicht mehr in zukünftigen Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020ul</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass, wenn das Stereo vorhanden sein muss, auf Mono reduziert werden soll, die Anzeige in der rechten Ecke anstelle der linken Sicht verwendet wird.<br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8 unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040ul</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Darstellung den linken Puffer als Mono-Puffer verwenden soll. Eine Anwendung ruft die <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1:: istemporarymonosupported</strong></a> -Methode auf, um zu bestimmen, ob eine austauschkette &quot; temporäres Mono unterstützt &quot; .<br/> <strong>Direct3D 11:</strong> Dieser Enumerationswert wird ab Windows 8 unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100ul</dt> </dl></td>
<td style="text-align: left;">Dieses Flag muss von Media apps festgelegt werden, die zurzeit eine benutzerdefinierte aktuelle Dauer (benutzerdefinierte Aktualisierungsrate) verwenden. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>idxgitauapchainmedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Dieser Wert wird ab Windows 8.1 unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200ul</dt> </dl></td>
<td style="text-align: left;">Das Zulassen von zerreißen ist eine Anforderung der Variablen Aktualisierungsrate.<br/> Die Bedingungen für die Verwendung von DXGI_PRESENT_ALLOW_TEARING während der Gegenwart lauten wie folgt:<br/>
<ul>
<li>Die SwapChain muss mit dem <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> -Flag erstellt werden.</li>
<li>Das an <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (oder <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) über gegebene Synchronisierungs Intervall muss 0 sein.</li>
<li>Das DXGI_PRESENT_ALLOW_TEARING-Flag kann nicht in einer Anwendung verwendet werden, die sich derzeit im Vollbildmodus befindet (durch Aufrufen von <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>setfullscreenstate (true)</strong></a>festgelegt). Sie kann nur im Fenstermodus verwendet werden. Wenn Sie dieses Flag in den Win32-apps im Vollbildmodus verwenden möchten, sollte die Anwendung in einem Fenster mit erweiterter Breite angezeigt werden, und Sie können die automatische ALT + EINGABETASTE mithilfe von <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>idxgifactory:: makewindowassociation</strong></a>deaktivieren. UWP-apps, die durch Aufrufen des Vollbildmodus in den Vollbildmodus wechseln, <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> sind Vollbildschirm Fenster und können das-Flag verwenden.</li>
</ul>
Wenn Sie <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (oder <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) mit diesem Flag aufrufen und die obigen Bedingungen nicht erfüllen, wird ein DXGI_ERROR_INVALID_CALL Fehler an die aufrufende Anwendung zurückgegeben.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Präsentations Optionen werden im Rahmen des [**idxgiswapchain::P Resent**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) -oder [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Aufrufes bereitgestellt. Die Puffer werden in der Beschreibung der Austausch Kette angegeben (Weitere Informationen finden Sie unter [**DXGI \_ Swap \_ Chain \_**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) debug or [**DXGI \_ Swap \_ Chain \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).

Der vorhandene DXGI \_ \_ -Neustart ist nur für Swapketten und den Vollbildmodus von Flip-Modellen gültig. Anwendungen können DXGI Present Restart verwenden, um eine Wiederherstellung nach einem Fehler \_ \_ in der Wiedergabe durchführen zu können, und um vorherige Präsentationen zu verwerfen. Das Verwerfen von bereits in der Warteschlange befindlichen Präsentationen ist nützlich, wenn diese Präsentationen in der Warteschlange Szenarios sind. Vor allem könnte bei der zuvor in der Warteschlange befindlichen Präsentation angenommen werden, dass das Fenster eine alte Größe hat (d. h., nach der Übermittlung ist ein Größenänderung aufgetreten).

DXGI \_ Present \_ " \_ auf \_ Ausgabe beschränken" ist nur für Swapketten gültig, die eine bestimmte Ausgabe angegeben haben, um Inhalte einzuschränken, wenn diese [**Swapketten erstellt wurden (IDXGIFactory2:: kreateswapchainforhwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Wenn keine Ausgabe vorhanden ist, auf die eingeschränkt werden kann, ist das Flag ungültig.

DXGI \_ Present " \_ Stereo \_ bevorzugen" \_ gibt an, dass das richtige Auge anstelle des linken (Standard-) Auges verwendet werden muss, wenn das Stereo vorhanden sein auf Mono reduziert werden muss. Sie können dieses Flag verwenden, wenn eine Seite eine höhere Qualität ist (z. b., wenn das Stereopaar von einem Standardbild synthetisiert wird).

DXGI \_ Present " \_ Stereo \_ temporäres \_ Mono" gibt an, dass der vorhandene den linken Puffer als Mono-Puffer verwenden soll. Sie können dieses Flag verwenden, um zu vermeiden, dass der richtige Puffer aktualisiert wird, wenn eine Anwendung vorübergehend keinen Stereo Inhalt hat. Verwenden Sie dieses Flag, wenn dies möglich ist, da es eine deutliche Optimierung durch das Betriebssystem ermöglicht und unter bestimmten Umständen das Ändern von Elementen im sichtbaren Modus vermieden werden kann.

Verwenden Sie für die meisten Anwendungen, für die Sie Vorhersagen, erneut Stereo, das DXGI \_ Present \_ Stereo \_ Temporary \_ Mono-Flag. Sie müssen die Verwendung dieses Flags in Anwendungen ausgleichen, die sehr lange ausgeführt werden oder nur selten gegen den Nachteil von nicht verwendetem Speicher angezeigt werden.

> [!Note]  
> Vollbildanwendungen, die zu einer Mono-Swap-Kette wechseln, führen zu einer Modusänderung, die im allgemeinen sichtbare Artefakte aufweist (z. b. "blinken"). Temporäres Mono wird jedoch möglicherweise nicht für Vollbild-Austausch Ketten unterstützt.

 

Das DXGI \_ -vorhanden sein \_ von "Stereo \_ bevorzugen" und " \_ DXGI Present" sind \_ \_ \_ temporäre Mono- \_ Flags gelten nur für Stereo Austausch Ketten. Wenn Sie diese verwenden, wenn Sie Mono-Austausch Ketten darstellen, tritt ein ungültiger Vorgang auf.

Wenn Sie das DXGI \_ Present \_ Stereo Temporary Mono-Flag verwenden, \_ \_ Wenn Sie eine Stereo Austausch Kette darstellen, die temporäre Mono nicht unterstützt, tritt ein Fehler auf, die Swapkette wird nicht angezeigt, und die Darstellung gibt einen [ \_ \_ ungültigen \_ DXGI-Fehler](dxgi-error.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
