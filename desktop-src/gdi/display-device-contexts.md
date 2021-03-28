---
description: Eine Anwendung erhält einen anzeigen Domänen Controller, indem Sie die Funktion BeginPaint, GetDC oder getdcex aufruft und das Fenster identifiziert, in dem die entsprechende Ausgabe angezeigt wird.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Geräte Kontexte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d0eeb3055209ad99a6a50fd129f9f9c064bf52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754448"
---
# <a name="display-device-contexts"></a>Geräte Kontexte anzeigen

Eine Anwendung erhält einen anzeigen Domänen Controller, indem Sie die Funktion [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)oder [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) aufruft und das Fenster identifiziert, in dem die entsprechende Ausgabe angezeigt wird. In der Regel erhält eine Anwendung einen anzeigen-DC nur dann, wenn Sie im Client Bereich gezeichnet werden muss. Allerdings kann ein [Fenster Gerätekontext](#window-device-contexts) durch Aufrufen der [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) -Funktion abgerufen werden. Nachdem die Anwendung das Zeichnen abgeschlossen hat, muss Sie den Domänen Controller freigeben, indem Sie die [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -oder [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion aufrufen.

Es gibt fünf Arten von DCS für Video-anzeigen:

-   Klasse
-   Allgemein
-   Privat
-   Fenster
-   Parent

## <a name="class-device-contexts"></a>Klassen Geräte Kontexte

*Klassen Geräte Kontexte* werden ausschließlich für die Kompatibilität mit 16-Bit-Versionen von Windows unterstützt. Wenn Sie Ihre Anwendung schreiben, sollten Sie die Verwendung des-Klassen Geräte Kontexts vermeiden. Verwenden Sie stattdessen einen privaten Gerätekontext.

## <a name="common-device-contexts"></a>Allgemeine Geräte Kontexte

*Häufig ausgestellte Geräte Kontexte* werden in einem speziellen Cache vom System verwaltet. Allgemeine Geräte Kontexte werden in Anwendungen verwendet, die seltene Zeichnungsvorgänge ausführen. Bevor das System das DC-handle zurückgibt, initialisiert es den gemeinsamen Gerätekontext mit Standardobjekten,-Attributen und-Modi. Alle von der Anwendung ausgeführten Zeichnungsvorgänge verwenden diese Standardwerte, es sei denn, eine der GDI-Funktionen wird aufgerufen, um ein neues Objekt auszuwählen, die Attribute eines vorhandenen Objekts zu ändern oder einen neuen Modus auszuwählen.

Da nur eine begrenzte Anzahl von gängigen Geräte Kontexten vorhanden ist, sollte eine Anwendung Sie nach Abschluss der Zeichnung freigeben. Wenn die Anwendung einen gemeinsamen Gerätekontext freigibt, gehen alle Änderungen an den Standarddaten verloren.

## <a name="private-device-contexts"></a>Private Geräte Kontexte

*Private Geräte Kontexte* sind DCS, die im Gegensatz zu gemeinsamen Geräte Kontexten Änderungen an den Standarddaten beibehalten, auch nachdem Sie von einer Anwendung freigegeben wurden. Private Geräte Kontexte werden in Anwendungen verwendet, die zahlreiche Zeichnungsvorgänge ausführen, wie z. b. Anwendungen mit computergestütztem Design (CAD), Desktop Publishing Anwendungen, zeichnen und Zeichnen von Anwendungen usw. Private Geräte Kontexte sind nicht Teil des System Caches und müssen daher nicht nach der Verwendung freigegeben werden. Das System entfernt automatisch einen privaten Gerätekontext, nachdem das letzte Fenster dieser Klasse zerstört wurde.

Eine Anwendung erstellt einen privaten Gerätekontext, indem Sie zuerst den Stil der CS \_ -owndc-Fenster Klasse angibt,  Wenn Sie den Formatvorlagen Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur initialisiert und die [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion aufruft. (Weitere Informationen zu Fenster Klassen finden Sie unter [Fenster Klassen](../winmsg/window-classes.md).)

Nachdem ein Fenster mit dem CS- \_ owndc-Stil erstellt wurde, kann eine Anwendung die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)-, [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex)-oder [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -Funktion einmal aufrufen, um ein Handle zu erhalten, das einen privaten Gerätekontext identifiziert. Die Anwendung kann dieses Handle (und den zugeordneten DC) weiter verwenden, bis das mit dieser Klasse erstellte Fenster gelöscht wird. Alle Änderungen an Grafikobjekten und deren Attributen oder Grafikmodi werden vom System beibehalten, bis das Fenster gelöscht wird.

## <a name="window-device-contexts"></a>Fenster Geräte Kontexte

Mithilfe eines *Fenster Geräte Kontexts* kann eine Anwendung an beliebiger Stelle in einem Fenster gezeichnet werden, einschließlich des nicht-Client Bereichs. Fenster Geräte Kontexte werden in der Regel von Anwendungen verwendet, die die Nachrichten von [**WM \_ ncpaint**](wm-ncpaint.md) und [**WM \_ ncaktivierungs**](../winmsg/wm-ncactivate.md) für Windows mit benutzerdefinierten nicht-Client-Bereichen verarbeiten. Die Verwendung eines Fenster Geräte Kontexts wird für keinen anderen Zweck empfohlen. Weitere Informationen finden Sie unter. Weitere Informationen finden Sie unter [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Übergeordnete Geräte Kontexte

Mit einem über *geordneten Gerätekontext* kann eine Anwendung die Zeit minimieren, die zum Einrichten des Clippingbereichs für ein Fenster erforderlich ist. Eine Anwendung verwendet in der Regel übergeordnete Geräte Kontexte, um das Zeichnen von Steuerungs Fenstern zu beschleunigen, ohne einen privaten oder Klassen Gerätekontext zu erfordern. Beispielsweise verwendet das System die übergeordneten Geräte Kontexte für die Schaltfläche Push-Schaltfläche und Bearbeitungs Steuerelemente. Übergeordnete Geräte Kontexte sind nur für die Verwendung mit untergeordneten Fenstern gedacht, niemals mit den Fenstern der obersten Ebene oder des Popup Fensters. Weitere Informationen finden Sie unter. Siehe über [geordnete Anzeigegeräte Kontexte](parent-display-device-contexts.md).

 

 
