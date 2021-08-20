---
description: Gruppieren von Parametern
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Gruppieren von Parametern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3083c3a7ad0971d6d3334303cf9eaf4c0313c4482825c3623a04a12ae046b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018368"
---
# <a name="grouping-parameters"></a>Gruppieren von Parametern

Ein Gruppierungsparameter identifiziert eine Sammlung von [Audiositzungen,](audio-sessions.md) die alle von einer einzelnen Lautstärkeregler im Systemvolume-Steuerungsprogramm Sndvol gesteuert werden. Der Gruppierungsparameter ist eine GUID, die die Auflistung innerhalb des Bereichs des Computers eindeutig identifiziert.

Der Zweck eines Gruppierungsparameters ähnelt dem der Sitzungs-GUID für eine prozessübergreifende Sitzung. Das heißt, der Gruppierungsparameter ermöglicht dem Benutzer, eine Sammlung von Datenströmen aus einer beliebigen Anzahl von Prozessen als einzelne Einheit zu steuern. Der Gruppierungsparameter erfüllt diesen Zweck jedoch in Situationen, in denen prozessübergreifende Sitzungen keine Lösung bereitstellen können.

Wenn mehrere Clients ihre jeweiligen Streams separaten Sitzungen zuweisen, aber allen Sitzungen denselben Gruppierungsparameter zuweisen, zeigt Sndvol eine einzelne Volumesteuerung für diese Sitzungen an. Sndvol oder eine ähnliche Volumesteuerungsanwendung muss folgende Schritte ausführen, um Unterstützung für Gruppierungsparameter bereitzustellen:

-   Überprüfen Sie vor dem Anzeigen der Volumesteuerelemente die Gruppierungsparameter aller aktiven Sitzungen. Gruppieren Sie alle Sitzungen, die über den gleichen Gruppierungsparameter verfügen, unter einer einzelnen Volumesteuerung.
-   Wenn der Benutzer die Einstellung für ein Volumesteuerelement für einen bestimmten Gruppierungsparameter ändert, aktualisieren Sie die Volumeebenen aller Sitzungen, die diesen Gruppierungsparameter gemeinsam nutzen.

Gruppierungsparameter helfen, die Anzahl der Volumesteuerelemente zu reduzieren, die von Sndvol angezeigt werden. Benutzer werden möglicherweise verwirren, wenn Sndvol seine Anzeige mit zu vielen Steuerelementen überladen. Ohne Unterstützung für Gruppierungsparameter würde Sndvol immer ein separates Volumesteuerelement für jede Sitzung anzeigen, was unter Umständen nicht in allen Fällen geeignet ist. Darüber hinaus bieten Gruppierungsparameter eine praktische Möglichkeit, um sicherzustellen, dass Sitzungen, die ähnliche Arten von Audioinhalten enthalten, problemlos auf die gleiche Lautstärkestufe festgelegt werden können.

Wie bereits erläutert, weisen Audio-APIs auf höherer Ebene ihre Datenströme in der Regel der prozessspezifischen Standardsitzung zu (die durch den GUID-Wert DER Sitzung ALS NULL identifiziert \_ wird). Mit dieser Standardeinstellung kann Sndvol ein separates Volumesteuerelement für jeden Clientanwendungsprozess anzeigen, was häufig das gewünschte Verhalten ist. Wenn außerdem mehrere Instanzen desselben Clients in separaten Prozessen ausgeführt werden, aber eine einzelne freigegebene Volumesteuerung erfordern, können die Clients ihre Streams einfach derselben prozessübergreifenden Sitzung zuweisen. Keiner dieser Fälle erfordert die Verwendung von Gruppierungsparametern. Ein wichtiger Fall, wie von Microsoft Internet Explorer veranschaulicht, erfordert jedoch die Verwendung von Gruppierungsparametern, um das gewünschte Verhalten zu erzielen.

Internet Explorer ermöglicht Benutzern, mehrere Browserfenster zu öffnen, und diese Fenster werden möglicherweise nicht alle im selben Prozess ausgeführt. Benutzer werden möglicherweise verwirren, wenn Sndvol für jede Anwendungsinstanz ein separates Volumesteuerelement anzeigt, die alle die gleiche Bezeichnung "Internet Explorer" aufweisen. Eine prozessübergreifende Sitzung ist in diesem Fall keine praktikable Lösung. Wenn mehrere Instanzen von Internet Explorer in verschiedenen Prozessen ausgeführt werden, können sie möglicherweise nicht alle audiostreams einer einzelnen prozessübergreifenden Sitzung zuweisen. Der Grund dafür ist, dass auf den Internet Explorer Fenstern möglicherweise Instanzen von Windows Media Player oder ein anderes Multimedia-Plug-In ausgeführt werden, das eine übergeordnete Audio-API verwendet, um die Audiostreams wiederzugeben. Diese APIs weisen die Streams in einem Prozess in der Regel einer prozessspezifischen Standardsitzung zu. Internet Explorer hat keine Kontrolle über die Zuweisung dieser Datenströme zu Sitzungen.

WASAPI löst dieses Problem, indem es jeder Instanz von Internet Explorer ermöglicht wird, auf die Sitzungssteuerelemente für ihre prozessspezifische Standardsitzung zuzugreifen und dieser Sitzung einen Gruppierungsparameter zuzuweisen. Wenn alle Instanzen von Internet Explorer allen Audiositzungen denselben Gruppierungsparameter zuweisen, zeigt Sndvol ein einzelnes Volumesteuerelement für diese Sitzungen an.

Standardmäßig gehört eine Sitzung keiner Gruppierung an. Wenn ein Client einer Gruppierung nicht explizit eine Sitzung zuweist, zeigt Sndvol eine dedizierte Volumesteuerung für diese Sitzung an. Der Gruppierungsparameterwert GUID \_ NULL gibt an, dass eine Sitzung keiner Gruppierung angehört. Wenn kein Client einer Sitzung explizit einen Gruppierungsparameter zugewiesen hat, ist der Gruppierungsparameterwert für diese Sitzung standardmäßig GUID \_ NULL.

Ein Client kann die Gruppierung, der eine Sitzung zugewiesen ist, dynamisch ändern.

Eine Gruppierung kann eine beliebige Kombination aus prozessübergreifenden sitzungen und prozessspezifischen Sitzungen auf einem [Audioendpunktgerät](audio-endpoint-devices.md)enthalten.

Über die Sndvol-Benutzeroberfläche kann der Benutzer die Lautstärkeregler für jeweils nur ein Audioendpunktgerät anzeigen. Wenn der Benutzer die Lautstärkeregler für ein bestimmtes Gerät anpasst, sind die Volumenebenen von Sitzungen, die eine Verbindung mit anderen Geräten herstellen, nicht betroffen. Insbesondere wirkt sich eine Volumesteuerung für einen bestimmten Gruppierungsparameter nur auf Sitzungen aus, die den Gruppierungsparameter gemeinsam nutzen und mit dem aktuell ausgewählten Gerät verbunden sind. Eine Sitzung, die über einen identischen Gruppierungsparameter verfügt, aber mit einem anderen Gerät verbunden ist, ist davon nicht betroffen.

Wie zuvor beschrieben, bezeichnet Sndvol jedes volume-Steuerelement, das angezeigt wird, mit einem Anzeigenamen und einem Symbol. Im Fall eines Volumesteuerelements für eine Gruppierung wählt Sndvol beliebig eine der Sitzungen in der Gruppierung als Quelle für den Anzeigenamen und das Symbol aus, das mit dem Volumesteuerelement angezeigt wird. Um sicherzustellen, dass Sndvol immer den gleichen Anzeigenamen und das gleiche Symbol für eine Gruppierung anzeigt, sollten daher alle Anwendungsinstanzen, die dieser Gruppierung Sitzungen zuweisen, sicherstellen, dass ihre jeweiligen Sitzungen den gleichen Anzeigenamen und das gleiche Symbol aufweisen. Weitere Informationen zu Anzeigenamen und Symbolen finden Sie unter [Audiositzungen.](audio-sessions.md)

Eine Anwendung wie Sndvol kann sich registrieren, um Benachrichtigungen zu erhalten, wenn sich der Gruppierungsparameter für eine Sitzung ändert. Solche Benachrichtigungen können nützlich sein, wenn die Anwendung Informationen zur Zuweisung von Sitzungen zu Gruppierungsparametern zwischenspeichert. Eine Benachrichtigung informiert die Anwendung, dass die zwischengespeicherten Informationen möglicherweise nicht mehr gültig sind.

Um einer Sitzung einen Gruppierungsparameter zuzuweisen, rufen Sie die [**IAudioSessionControl::SetGroupingParam-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) auf. Um den Gruppierungsparameter abzurufen, der einer Sitzung zugewiesen ist, rufen Sie die [**IAudioSessionControl::GetGroupingParam-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiositzungen](audio-sessions.md)
</dt> </dl>

 

 



