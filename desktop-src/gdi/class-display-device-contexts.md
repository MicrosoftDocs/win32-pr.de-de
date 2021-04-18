---
description: Durch die Verwendung eines Klassen Geräte Kontexts kann eine Anwendung einen einzelnen Anzeigegeräte Kontext für jedes Fenster verwenden, das zu einer bestimmten Klasse gehört.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: Klassen Anzeige von Geräte Kontexten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5a4cc0268d948e1a6f95050409698217e3f13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978784"
---
# <a name="class-display-device-contexts"></a>Klassen Anzeige von Geräte Kontexten

Durch die Verwendung eines *Klassen Geräte Kontexts* kann eine Anwendung einen einzelnen Anzeigegeräte Kontext für jedes Fenster verwenden, das zu einer bestimmten Klasse gehört. Klassen Geräte Kontexte werden häufig mit Steuerungs Fenstern verwendet, die mit denselben Attributwerten gezeichnet werden. Wie bei privaten Geräte Kontexten minimieren Klassen Geräte Kontexte den Zeitaufwand für die Vorbereitung eines Geräte Kontexts für das Zeichnen.

Das System stellt einen Klassen Gerätekontext für ein Fenster bereit, wenn er zu einer Fenster Klasse gehört, die über den CS- \_ classdc-Stil verfügt. Das System erstellt den Gerätekontext bei der Erstellung des ersten Fensters, das zur-Klasse gehört, und verwendet dann den gleichen Gerätekontext für alle später erstellten Fenster in der-Klasse. Anfänglich hat der Klassen Gerätekontext dieselben Standardwerte für Attribute wie ein gemeinsamer Gerätekontext, aber die Anwendung kann diese jederzeit ändern. Das System behält alle Änderungen mit Ausnahme des Ausschneide Bereichs und Geräte Ursprungs bei, bis das letzte Fenster in der Klasse zerstört wurde. Eine Änderung, die für ein Fenster vorgenommen wurde, gilt für alle Fenster in dieser Klasse.

Eine Anwendung kann das Handle für den Klassen Gerätekontext abrufen, indem die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion nach der Erstellung des ersten Fensters verwendet wird. Die Anwendung kann das Handle beibehalten und verwenden, ohne es freizugeben, da der Klassen Gerätekontext nicht Teil des Kontext Caches des Anzeige Geräts ist. Wenn die Anwendung ein anderes Fenster in derselben Fenster Klasse erstellt, muss die Anwendung den Klassen Gerätekontext erneut abrufen. Durch Abrufen des Geräte Kontexts wird der richtige Geräte Ursprung und der gewünschte Clippingbereich für das neue Fenster festgelegt. Nachdem die Anwendung den Klassen Gerätekontext für ein neues Fenster in der-Klasse abgerufen hat, kann der Gerätekontext nicht mehr verwendet werden, um im ursprünglichen Fenster zu zeichnen, ohne ihn erneut für dieses Fenster abzurufen. Im Allgemeinen muss eine Anwendung jedes Mal, wenn Sie in einem Fenster gezeichnet werden muss, explizit den Klassen Gerätekontext für das Fenster abrufen.

Anwendungen, die Klassen Geräte Kontexte verwenden, sollten [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) immer aufrufen, wenn eine WM-Zeichnungs Nachricht verarbeitet wird. [**\_**](wm-paint.md) Die-Funktion legt den korrekten Geräte Ursprung und Clippingbereich für das Fenster fest und enthält den Aktualisierungs Bereich. Die Anwendung sollte auch [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) aufrufen, um die Einfügemarke wiederherzustellen, wenn **BeginPaint** Sie verborgen hat. **Endpaint** wirkt sich nicht auf einen Klassen Gerätekontext aus.

Das System übergibt den Klassen Gerätekontext beim Senden der [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung an die Anwendung, sodass die aktuellen Attributwerte alle Zeichnungen beeinflussen können, die von der Anwendung oder dem System bei der Verarbeitung dieser Nachricht ausgeführt werden. Wie bei einem Fenster mit privatem Gerätekontext kann eine Anwendung [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) verwenden, um zu erzwingen, dass das System einen gemeinsamen Gerätekontext für das Fenster mit einem Klassen Gerätekontext zurückgibt.

Die Verwendung von Klassen Geräte Kontexten wird nicht empfohlen.

 

 
