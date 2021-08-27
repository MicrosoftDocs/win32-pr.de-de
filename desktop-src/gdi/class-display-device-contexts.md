---
description: Mithilfe eines Klassengerätekontexts kann eine Anwendung einen einzelnen Anzeigegerätekontext für jedes Fenster verwenden, das zu einer angegebenen Klasse gehört.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: Klassenanzeigegerätekontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8e4ca7f7d51f3dd50f50a07ab44496d56e4a78effb78f33e9eed6f5ffc3745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062480"
---
# <a name="class-display-device-contexts"></a>Klassenanzeigegerätekontexte

Mithilfe eines *Klassengerätekontexts* kann eine Anwendung einen einzelnen Anzeigegerätekontext für jedes Fenster verwenden, das zu einer angegebenen Klasse gehört. Klassengerätekontexte werden häufig mit Steuerfenstern verwendet, die mit denselben Attributwerten gezeichnet werden. Wie private Gerätekontexte minimieren Klassengerätekontexte die Zeit, die erforderlich ist, um einen Gerätekontext für das Zeichnen vorzubereiten.

Das System stellt einen Klassengerätekontext für ein Fenster bereit, wenn es zu einer Fensterklasse mit dem CS \_ CLASSDC-Stil gehört. Das System erstellt den Gerätekontext beim Erstellen des ersten Fensters, das zur -Klasse gehört, und verwendet dann den gleichen Gerätekontext für alle später erstellten Fenster in der -Klasse. Anfänglich hat der Klassengerätekontext die gleichen Standardwerte für Attribute wie ein allgemeiner Gerätekontext, aber die Anwendung kann diese jederzeit ändern. Das System behält alle Änderungen mit Ausnahme des Ausschneidebereichs und des Geräteursprungs bei, bis das letzte Fenster in der Klasse zerstört wurde. Eine Für ein Fenster vorgenommene Änderung gilt für alle Fenster in dieser Klasse.

Eine Anwendung kann das Handle jederzeit nach dem Erstellen des ersten Fensters mithilfe der [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) in den Klassengerätekontext abrufen. Die Anwendung kann das Handle beibehalten und verwenden, ohne es freizugeben, da der Klassengerätekontext nicht Teil des Anzeigegerätekontextcaches ist. Wenn die Anwendung ein weiteres Fenster in derselben Fensterklasse erstellt, muss die Anwendung den Klassengerätekontext erneut abrufen. Durch das Abrufen des Gerätekontexts werden der richtige Geräteursprung und der richtige Ausschneidebereich für das neue Fenster festgelegt. Nachdem die Anwendung den Klassengerätekontext für ein neues Fenster in der -Klasse abgerufen hat, kann der Gerätekontext nicht mehr zum Zeichnen im ursprünglichen Fenster verwendet werden, ohne ihn für dieses Fenster erneut abzurufen. Im Allgemeinen muss eine Anwendung jedes Mal, wenn sie in einem Fenster zeichnen muss, den Klassengerätekontext für das Fenster explizit abrufen.

Anwendungen, die Klassengerätekontexte verwenden, sollten [**beginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) immer aufrufen, wenn eine [**WM \_ PAINT-Nachricht**](wm-paint.md) verarbeitet wird. Die Funktion legt den richtigen Geräteursprungs- und Clippingbereich für das Fenster fest und integriert den Updatebereich. Die Anwendung sollte auch [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) aufrufen, um den Caretstrich wiederherzustellen, wenn **BeginPaint** es ausgeblendet hat. **EndPaint** hat keine anderen Auswirkungen auf einen Klassengerätekontext.

Das System übergibt den Klassengerätekontext beim Senden der [**WM \_ ERASEBKGND-Nachricht**](../winmsg/wm-erasebkgnd.md) an die Anwendung, wodurch die aktuellen Attributwerte sich auf alle Zeichnungen auswirken können, die von der Anwendung oder dem System bei der Verarbeitung dieser Nachricht ausgeführt werden. Wie bei einem Fenster mit einem privaten Gerätekontext kann eine Anwendung [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) verwenden, um zu erzwingen, dass das System einen allgemeinen Gerätekontext für das Fenster zurückgibt, das über einen Klassengerätekontext verfügt.

Die Verwendung von Klassengerätekontexten wird nicht empfohlen.

 

 
