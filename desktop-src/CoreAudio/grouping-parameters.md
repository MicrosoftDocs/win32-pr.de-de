---
description: Gruppieren von Parametern
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Gruppieren von Parametern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfb674d4349f351ce36fe1e236d1ecd3b265d8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748384"
---
# <a name="grouping-parameters"></a>Gruppieren von Parametern

Ein Gruppierungs Parameter identifiziert eine Auflistung von [audiositzungen](audio-sessions.md) , die alle von einem einzelnen volumesteuerelement im System Volume-Control-Programm (sndvol) gesteuert werden. Der Gruppierungs Parameter ist eine GUID, die die Sammlung innerhalb des Gültigkeits Bereichs des Computers eindeutig identifiziert.

Der Zweck eines Gruppierungs Parameters ähnelt dem der Sitzungs-GUID für eine prozessübergreifende Sitzung. Das heißt, der Gruppierungs Parameter ermöglicht es dem Benutzer, eine Auflistung von Streams von einer beliebigen Anzahl von Prozessen als einzelne Einheit zu steuern. Der Gruppierungs Parameter dient diesem Zweck jedoch in Situationen, in denen prozessübergreifende Sitzungen keine Lösung bereitstellen können.

Wenn mehrere Clients die entsprechenden Datenströme separaten Sitzungen zuweisen, aber den gleichen Gruppierungs Parameter allen Sitzungen zuweisen, zeigt sndvol für diese Sitzungen ein einzelnes volumesteuerelement an. Zum Bereitstellen von Unterstützung für Gruppierungs Parameter muss sndvol oder eine beliebige ähnliche volumesteuerungsanwendung folgende Aktionen ausführen:

-   Überprüfen Sie vor dem Anzeigen der volumesteuerelemente die Gruppierungs Parameter aller aktiven Sitzungen. Gruppieren Sie unter einem einzelnen Volume alle Sitzungen, die denselben Gruppierungs Parameter aufweisen.
-   Wenn der Benutzer die Einstellung eines volumesteuerelements für einen bestimmten Gruppierungs Parameter ändert, aktualisieren Sie die volumeebenen aller Sitzungen, die diesen Gruppierungs Parameter gemeinsam verwenden.

Gruppierungs Parameter helfen, die Anzahl der von sndvol angezeigten volumesteuerelemente zu verringern. Benutzer werden möglicherweise verwirrt, wenn die Anzeige von sndvol mit zu vielen Steuerelementen angezeigt wird. Ohne Unterstützung für das Gruppieren von Parametern würde sndvol für jede Sitzung immer ein separates volumensteuerelement anzeigen, das in allen Fällen nicht geeignet ist. Außerdem stellen Gruppierungs Parameter eine bequeme Möglichkeit dar, um sicherzustellen, dass Sitzungen, die ähnliche Typen von Audioinhalten enthalten, problemlos auf die gleiche Volumeebene festgelegt werden können.

Wie bereits erläutert, weisen übergeordnete audioapis ihre Streams in der Regel der standardmäßigen prozessspezifischen Sitzung zu (identifiziert durch den Sitzungs-GUID-Wert GUID \_ null). Mit dieser Standardeinstellung kann sndvol ein separates volumesteuerelement für jeden Client Anwendungsprozess anzeigen. Dies ist häufig das gewünschte Verhalten. Wenn darüber hinaus mehrere Instanzen desselben Clients in separaten Prozessen ausgeführt werden, aber ein einzelnes, frei gegebenes Volumen Steuerelement erforderlich sind, können die Clients ihre Streams einfach derselben prozessübergreifenden Sitzung zuweisen. Keines dieser Fälle erfordert die Verwendung von Gruppierungs Parametern. Ein wichtiger Fall, wie von Microsoft Internet Explorer veranschaulicht, erfordert jedoch die Verwendung von Gruppierungs Parametern, um das gewünschte Verhalten zu erzielen.

Internet Explorer ermöglicht es Benutzern, mehrere Browserfenster zu öffnen. diese Fenster werden möglicherweise nicht alle im selben Prozess ausgeführt. Benutzer werden möglicherweise verwirrt, wenn sndvol für jede Anwendungs Instanz ein separates volumensteuerelement angezeigt hat, das die gleiche Bezeichnung hat, "Internet Explorer". Eine prozessübergreifende Sitzung ist in diesem Fall nicht realisierbar – wenn mehrere Instanzen von Internet Explorer in verschiedenen Prozessen ausgeführt werden, können Sie möglicherweise nicht all Ihre Audiostreams einer einzelnen prozessübergreifenden Sitzung zuweisen. Der Grund hierfür ist, dass die Internet Explorer-Fenster möglicherweise Instanzen von Windows Media Player oder ein anderes multimediareplug-in ausführen, das eine audioapi auf höherer Ebene verwendet, um seine Audiostreams wiederzugeben. Diese APIs weisen in der Regel die Datenströme in einem Prozess einer standardmäßigen prozessspezifischen Sitzung zu. Internet Explorer hat keine Kontrolle über die Zuweisung dieser Streams zu Sitzungen.

WASAPI löst dieses Problem, indem jede Instanz von Internet Explorer für die Standardprozess spezifische Sitzung auf die Sitzungs Steuerelemente zugreift und dieser Sitzung einen Gruppierungs Parameter zuweist. Wenn alle Instanzen von Internet Explorer denselben Gruppierungs Parameter allen audiositzungen zuweisen, zeigt sndvol für diese Sitzungen ein einzelnes volumesteuerelement an.

Standardmäßig gehört eine Sitzung keiner Gruppierung an. Wenn ein Client einer Gruppierung nicht explizit eine Sitzung zuweist, zeigt sndvol ein dediziertes volumesteuerelement für die Sitzung an. Der Gruppierungs Parameterwert GUID \_ NULL gibt an, dass eine Sitzung nicht zu einer Gruppierung gehört. Wenn keiner Sitzung von einem Client explizit ein Gruppierungs Parameter zugewiesen wurde, ist der Gruppierungs Parameterwert für diese Sitzung standardmäßig auf GUID NULL festgelegt \_ .

Ein Client kann die Gruppierung, der eine Sitzung zugewiesen ist, dynamisch ändern.

Eine Gruppierung kann eine beliebige Kombination von prozessübergreifenden Sitzungen und prozessspezifischen Sitzungen auf einem [audioendpunktgerät](audio-endpoint-devices.md)einschließen.

Die Benutzeroberfläche von sndvol ermöglicht dem Benutzer die Anzeige der volumesteuerelemente für nur ein audioendpunktgerät gleichzeitig. Wenn der Benutzer die volumesteuerelemente für ein bestimmtes Gerät anpasst, wirkt sich dies nicht auf die volumeebenen der Sitzungen aus, die eine Verbindung mit anderen Geräten herstellen. Insbesondere wirkt sich ein volumesteuerelement für einen bestimmten Gruppierungs Parameter nur auf Sitzungen aus, die den Gruppierungs Parameter gemeinsam verwenden und mit dem aktuell ausgewählten Gerät verbunden sind. Eine Sitzung, die einen identischen Gruppierungs Parameter hat, aber mit einem anderen Gerät verbunden ist, ist nicht betroffen.

Wie bereits beschrieben, bezeichnet sndvol die einzelnen anzuzeigenden volumesteuer Elemente mit einem anzeigen Amen und Symbol. Im Fall eines volumesteuerelements für eine Gruppierung wählt sndvol willkürlich eine der Sitzungen in der Gruppierung als Quelle für den anzeigen Amen und das Symbol aus, das mit dem volumesteuerelement angezeigt wird. Um sicherzustellen, dass sndvol immer den gleichen anzeigen Amen und das gleiche Symbol für eine Gruppierung anzeigt, sollten alle Anwendungs Instanzen, die dieser Gruppierung Sitzungen zuweisen, sicherstellen, dass die entsprechenden Sitzungen denselben anzeigen Amen und dasselbe Symbol aufweisen. Weitere Informationen zu anzeigen Amen und Symbolen finden Sie unter [audiositzungen](audio-sessions.md).

Eine Anwendung wie sndvol kann sich selbst registrieren, um Benachrichtigungen zu empfangen, wenn der Gruppierungs Parameter für eine Sitzung geändert wird. Solche Benachrichtigungen können hilfreich sein, wenn die Anwendung Informationen über die Zuweisung von Sitzungen zu Gruppierungs Parametern zwischenspeichert. In einer Benachrichtigung wird der Anwendung mitgeteilt, dass die zwischengespeicherten Informationen möglicherweise nicht mehr gültig sind.

Um einer Sitzung einen Gruppierungs Parameter zuzuweisen, müssen Sie die [**iaudiosessioncontrol:: setgroupingparam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) -Methode aufrufen. Um den Gruppierungs Parameter zu erhalten, der einer Sitzung zugewiesen ist, rufen Sie die [**iaudiosessioncontrol:: getgroupingparam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) -Methode auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiositzungen](audio-sessions.md)
</dt> </dl>

 

 



