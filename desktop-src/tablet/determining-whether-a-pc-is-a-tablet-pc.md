---
description: Möglicherweise müssen Sie gelegentlich ermitteln, ob Ihre Anwendung auf einem Tablet PC ausgeführt wird, da Sie möchten, dass Ihre Anwendungen inhärente Freihand-, Erkennungs-und Stift Funktionen nutzen.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Ermitteln, ob ein PC ein Tablet PC ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351029"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Ermitteln, ob ein PC ein Tablet PC ist

Möglicherweise müssen Sie gelegentlich ermitteln, ob Ihre Anwendung auf einem Tablet PC ausgeführt wird, da Sie möchten, dass Ihre Anwendungen inhärente Freihand-, Erkennungs-und Stift Funktionen nutzen. Um Ihnen zu helfen, zu bestimmen, ob Ihre Anwendung auf die Tablet PC-Features zugreifen kann, können Sie den GetSystemMetrics ()-Windows-API-Befehl verwenden, wie in diesem Thema beschrieben.

## <a name="client-side-applications"></a>Client-Side Anwendungen

Mithilfe der folgenden Verfahren können Sie feststellen, ob Ihr Code auf einem Tablet PC ausgeführt wird.

-   [Verwenden von GetSystemMetrics (SM \_ TabletPC)](/windows)
-   [Verwenden von Tablet Platform-Binärdateien](#using-the-presence-of-tablet-platform-binaries)
-   [Webbasierte Anwendungen](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Verwenden von GetSystemMetrics (SM \_ TabletPC)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Tablet PC Edition

Verwenden Sie in Microsoft Windows XP Tablet PC Edition die Funktion GetSystemMetrics (SM \_ TabletPC), um zu bestimmen, ob ein Computer ein Tablet PC ist. GetSystemMetrics (SM \_ TabletPC) soll auf einem Computer, auf dem Windows XP Tablet PC Edition ausgeführt wird, "true" zurückgeben.

### <a name="windows-vista"></a>Windows Vista

In Windows Vista ist kein eindeutiges Tablet PC SDK mehr vorhanden. Die Windows SDK enthält jetzt den Abschnitt "Tablet PC and Touchscreen Technology", und die Logik von GetSystemMetrics (SM \_ TabletPC) wurde geändert, um dies widerzuspiegeln. GetSystemMetrics (SM \_ TabletPC) gibt jetzt true zurück, wenn Folgendes zutrifft:

-   Es gibt einen integrierten Digitalisierer (Pen oder Touchscreen) auf dem System.
-   Die optionale Komponente Tablet PC ist installiert. Diese Komponente enthält Features wie Tablet PC Input Panel und Windows Journal.
-   Der Computer ist für die Verwendung der optionalen Komponente lizenziert. Premium-Versionen von Windows Vista – z. b. Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise und Windows Vista Ultimate – sind für die Verwendung der optionalen Komponente lizenziert.
-   Der Tablet PC-Eingabe Dienst wird ausgeführt. Der Tablet PC-Eingabe Dienst ist ein neuer Dienst für Windows Vista, der die Tablet PC-Eingabe steuert.

Mit dieser zunehmenden Genauigkeit ist GetSystemMetrics (SM \_ TabletPC) weiterhin die empfohlene Methode, um zu bestimmen, ob ein Computer, auf dem Windows Vista ausgeführt wird, ein Tablet PC ist.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Verwenden von Tablet Platform-Binärdateien

In Windows XP Tablet PC Edition und Windows Vista können Sie nach dem vorhanden sein der frei Hand Binärdateien suchen – z. b. inkobj.dll und Microsoft.Ink.dll – und ihre unterstützten Funktionen verwenden, sofern diese vorhanden sind.

In Windows Vista werden die Binärdateien der Tablet PC-Plattform standardmäßig auf allen Client Versionen installiert. Eingabe-und Freihand-Funktionen sind für diese Versionen verfügbar. Die Erkennung ist nur in Premium-Versionen von Windows Vista verfügbar.

### <a name="web-based-applications"></a>Web-Based Anwendungen

In Windows Vista enthält die von Internet Explorer gemeldete Benutzer-Agent-Zeichenfolge "Tablet PC 2,0", wenn das Gerät gemäß GetSystemMetrics (SM \_ TabletPC) ein Tablet PC ist.

In Windows XP Tablet PC Edition 2005 enthält die Benutzer-Agent-Zeichenfolge Tablet PC 1,7. Die Benutzer-Agent-Zeichenfolge sieht in etwa wie folgt aus:

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Verwenden Sie diesen Wert, um zu bestimmen, ob es sich bei dem Client Computer um einen Tablet PC handelt

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
