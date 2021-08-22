---
description: Eine Anwendung ruft einen Anzeige-DC ab, indem sie die BeginPaint-, GetDC- oder GetDCEx-Funktion aufruft und das Fenster identifiziert, in dem die entsprechende Ausgabe angezeigt wird.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Anzeigen von Gerätekontexten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2e2bbd847d1a473ff08de7db52da7513b91377e8a891b2c6fdde04a82bf1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761325"
---
# <a name="display-device-contexts"></a>Anzeigen von Gerätekontexten

Eine Anwendung ruft einen Anzeige-DC ab, indem sie die [**BeginPaint-,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**GetDC-**](/windows/desktop/api/Winuser/nf-winuser-getdc)oder [**GetDCEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdcex) aufruft und das Fenster identifiziert, in dem die entsprechende Ausgabe angezeigt wird. In der Regel erhält eine Anwendung nur dann einen Anzeigedomänencontroller, wenn sie im Clientbereich zeichnen muss. Sie können jedoch einen Fenstergerätekontext [abrufen,](#window-device-contexts) indem Sie die [**GetWindowDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) aufrufen. Wenn die Anwendung mit dem Zeichnen fertig ist, muss sie den DC durch Aufrufen der [**EndPaint-**](/windows/desktop/api/Winuser/nf-winuser-endpaint) oder [**ReleaseDC-Funktion wieder**](/windows/desktop/api/Winuser/nf-winuser-releasedc) frei geben.

Es gibt fünf Arten von DCs für Videoanzeigen:

-   Klasse
-   Allgemein
-   Privat
-   Fenster
-   Parent

## <a name="class-device-contexts"></a>Klassengerätekontexte

*Klassengerätekontexte* werden ausschließlich aus Kompatibilitäts- und 16-Bit-Versionen von Windows. Vermeiden Sie beim Schreiben Ihrer Anwendung die Verwendung des Klassengerätekontexts. Verwenden Sie stattdessen einen privaten Gerätekontext.

## <a name="common-device-contexts"></a>Allgemeine Gerätekontexte

*Allgemeine Gerätekontexte sind* Anzeige-Dcs, die vom System in einem speziellen Cache verwaltet werden. Allgemeine Gerätekontexte werden in Anwendungen verwendet, die selten Zeichnungsvorgänge ausführen. Bevor das System das DC-Handle zurückgibt, initialisiert es den allgemeinen Gerätekontext mit Standardobjekten, Attributen und Modi. Alle von der Anwendung ausgeführten Zeichnungsvorgänge verwenden diese Standardwerte, es sei denn, eine der GDI-Funktionen wird aufgerufen, um ein neues Objekt auszuwählen, die Attribute eines vorhandenen Objekts zu ändern oder einen neuen Modus auszuwählen.

Da nur eine begrenzte Anzahl gängiger Gerätekontexte vorhanden ist, sollte eine Anwendung sie nach Abschluss des Zeichnens wieder frei geben. Wenn die Anwendung einen allgemeinen Gerätekontext frei gibt, gehen alle Änderungen an den Standarddaten verloren.

## <a name="private-device-contexts"></a>Private Gerätekontexte

*Private Gerätekontexte* sind Anzeige-Dcs, die im Gegensatz zu gängigen Gerätekontexten änderungen an den Standarddaten auch nach der Freigabe durch eine Anwendung beibehalten. Private Gerätekontexte werden in Anwendungen verwendet, die zahlreiche Zeichnungsvorgänge ausführen, z. B. CAD-Anwendungen (Computer-Aided Design), Desktopveröffentlichungsanwendungen, Zeichnungs- und Zeichnungsanwendungen und so weiter. Private Gerätekontexte sind nicht Teil des Systemcaches und müssen daher nach der Verwendung nicht freigegeben werden. Das System entfernt automatisch einen privaten Gerätekontext, nachdem das letzte Fenster dieser Klasse zerstört wurde.

Eine Anwendung erstellt einen privaten Gerätekontext, indem sie zuerst den CS OWNDC-Fensterklassenstil ankn., wenn sie den Stil member der \_ [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) initialisiert und die [**RegisterClass-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassa) aufruft.  (Weitere Informationen zu Fensterklassen finden Sie unter [Fensterklassen](../winmsg/window-classes.md).)

Nach dem Erstellen eines Fensters im CS OWNDC-Stil kann eine Anwendung die \_ [**GetDC-,**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**GetDCEx-**](/windows/desktop/api/Winuser/nf-winuser-getdcex)oder [**BeginPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) einmal aufrufen, um ein Handle zu erhalten, das einen privaten Gerätekontext identifiziert. Die Anwendung kann dieses Handle (und den zugeordneten DC) weiterhin verwenden, bis sie das mit dieser Klasse erstellte Fenster löscht. Alle Änderungen an Grafikobjekten und deren Attributen oder Grafikmodi werden vom System beibehalten, bis das Fenster gelöscht wird.

## <a name="window-device-contexts"></a>Fenstergerätekontexte

Mit *einem Fenstergerätekontext* kann eine Anwendung überall in einem Fenster zeichnen, einschließlich des Nicht-Clientbereichs. Fenstergerätekontexte werden in der Regel von Anwendungen verwendet, die die [**WM \_ NCPAINT-**](wm-ncpaint.md) und [**WM \_ NCACTIVATE-Nachrichten**](../winmsg/wm-ncactivate.md) für Fenster mit benutzerdefinierten Nichtclientbereichen verarbeiten. Die Verwendung eines Fenstergerätekontexts wird für keinen anderen Zweck empfohlen. Weitere Informationen finden Sie unter . siehe [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Übergeordnete Gerätekontexte

Mit *einem übergeordneten Gerätekontext* kann eine Anwendung die Zeit minimieren, die zum Einrichten des Ausschneidebereichs für ein Fenster erforderlich ist. Eine Anwendung verwendet in der Regel übergeordnete Gerätekontexte, um das Zeichnen für Steuerfenster zu beschleunigen, ohne dass ein privater oder Klassengerätekontext erforderlich ist. Beispielsweise verwendet das System übergeordnete Gerätekontexte für Pushschaltfläche und Bearbeitungssteuerelemente. Übergeordnete Gerätekontexte sind nur für die Verwendung mit untergeordneten Fenstern vorgesehen, nie mit Fenstern der obersten Ebene oder Popupfenstern. Weitere Informationen finden Sie unter . weitere Informationen [finden Sie unter Gerätekontexte für die übergeordnete Anzeige.](parent-display-device-contexts.md)

 

 
