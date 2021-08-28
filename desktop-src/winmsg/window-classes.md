---
description: In diesem Thema werden die Typen von Fensterklassen, deren Suche durch das System und die Elemente beschrieben, die das Standardverhalten von Fenstern definieren, die zu ihnen gehören.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Fensterklassen (Windows und Meldungen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77e96a06433bf6bbcb72fb76a41a29fccee27ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482646"
---
# <a name="window-classes-windows-and-messages"></a>Fensterklassen (Windows und Meldungen)

In diesem Thema werden die Typen von Fensterklassen, deren Suche durch das System und die Elemente beschrieben, die das Standardverhalten von Fenstern definieren, die zu ihnen gehören.

Eine Fensterklasse ist ein Satz von Attributen, die das System als Vorlage zum Erstellen eines Fensters verwendet. Jedes Fenster ist ein Member einer Fensterklasse. Alle Fensterklassen sind prozessspezifisch.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Fensterklassen](about-window-classes.md)     | Erläutert Fensterklassen. Jede Fensterklasse verfügt über eine zugeordnete Fensterprozedur, die von allen Fenstern derselben Klasse gemeinsam genutzt wird. Die Fensterprozedur verarbeitet Meldungen für alle Fenster dieser Klasse und steuert daher deren Verhalten und Darstellung.<br/> |
| [Verwenden von Fensterklassen](using-window-classes.md)     | Veranschaulicht, wie ein lokales Fenster registriert und zum Erstellen eines Hauptfensters verwendet wird.<br/>                                                                                                                                                                     |
| [Window-Klassenreferenz](window-class-reference.md) | Enthält den API-Verweis.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Window-Klassenfunktionen



| Name                                         | BESCHREIBUNG                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Ruft Informationen zu einer Fensterklasse ab, einschließlich eines Handles für das kleine Symbol, das der Fensterklasse zugeordnet ist. Die [**GetClassInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) ruft kein Handle für das kleine Symbol ab.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Ruft den angegebenen 32-Bit-Wert **(long)** aus der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) ab, die dem angegebenen Fenster zugeordnet ist. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Ruft den angegebenen Wert aus der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) ab, die dem angegebenen Fenster zugeordnet ist.<br/>                                                                                            |
| [**Typedescriptor.getclassname**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Ruft den Namen der Klasse ab, zu der das angegebene Fenster gehört. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Ruft Informationen zum angegebenen Fenster ab. Die Funktion ruft auch den 32-Bit-Wert **(lang)** am angegebenen Offset in den zusätzlichen Fensterspeicher ab.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Ruft Informationen zum angegebenen Fenster ab. Die Funktion ruft auch den Wert an einem angegebenen Offset in den zusätzlichen Fensterspeicher ab.<br/>                                                                        |
| [**Registerclass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registriert eine Fensterklasse für die nachfolgende Verwendung in Aufrufen der [**CreateWindow-**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registriert eine Fensterklasse für die nachfolgende Verwendung in Aufrufen der [**CreateWindow-**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Ersetzt den angegebenen Wert am angegebenen Offset im zusätzlichen Klassenspeicher oder in der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) für die Klasse, zu der das angegebene Fenster gehört.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Ersetzt den 16-Bit-Wert (**WORD**) am angegebenen Offset in den zusätzlichen Klassenspeicher für die Fensterklasse, zu der das angegebene Fenster gehört.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Ändert ein Attribut des angegebenen Fensters. Die Funktion legt außerdem den 32-Bit-Wert (long) am angegebenen Offset in den zusätzlichen Fensterspeicher fest.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Ändert ein Attribut des angegebenen Fensters. Die Funktion legt auch einen Wert am angegebenen Offset im zusätzlichen Fensterspeicher fest.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Aufheben der Registrierung einer Fensterklasse, wodurch der für die Klasse erforderliche Arbeitsspeicher freigegeben wird. <br/>                                                                                                                                            |



 

Die folgenden Funktionen sind veraltet.




| Name | BESCHREIBUNG | 
|------|-------------|
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> | Ruft Informationen zu einer Fensterklasse ab. <br /><blockquote>[!Note]<br />Die <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo-Funktion</strong></a> wurde durch die <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx-Funktion</strong></a> ersetzt. Sie können <strong>weiterhin GetClassInfo</strong>verwenden, wenn Sie jedoch keine Informationen zum kleinen Symbol der Klasse benötigen.</blockquote><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a> | Ruft den 16-Bit-Wert<strong>(WORD)</strong>am angegebenen Offset in den zusätzlichen Klassenspeicher für die Fensterklasse ab, zu der das angegebene Fenster gehört.<blockquote>[!Note]<br />Diese Funktion ist für jede andere Verwendung als <em>nIndex</em> veraltet, die auf GCW_ATOM festgelegt ist. Die Funktion wird nur aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Anwendungen sollten die <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong-Funktion</strong></a> verwenden.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a> | Ersetzt den angegebenen 32-Bit-Wert (<strong>long</strong>) am angegebenen Offset in den zusätzlichen Klassenspeicher oder die <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX-Struktur</strong></a> für die Klasse, zu der das angegebene Fenster gehört.<blockquote>[!Note]<br />Diese Funktion wurde durch die <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr-Funktion</strong></a> ersetzt. Verwenden Sie <strong>SetClassLongPtr,</strong>um Code zu schreiben, der sowohl mit 32-Bit- als auch mit 64-Bit-Versionen von Windows kompatibel ist.</blockquote><br /><br /> | 




 

### <a name="window-class-structures"></a>Fensterklassenstrukturen



| Name                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Enthält die Fensterklassenattribute, die von der [**RegisterClass-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassa) registriert werden. <br/> Diese Struktur wurde durch die [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) ersetzt, die mit der [**RegisterClassEx-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassexa) verwendet wird. Sie können [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) und [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) weiterhin verwenden, wenn Sie das kleine Symbol, das der Fensterklasse zugeordnet ist, nicht festlegen müssen.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Enthält Fensterklasseninformationen. Sie wird mit den Funktionen [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) und [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  verwendet. <br/> Die [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) ähnelt der [**WNDCLASS-Struktur.**](/windows/win32/api/winuser/ns-winuser-wndclassa) Es gibt zwei Unterschiede. **WNDCLASSEX** enthält den **cbSize-Member,** der die Größe der -Struktur angibt, und den **hIconSm-Member,** der ein Handle für ein kleines Symbol enthält, das der Fensterklasse zugeordnet ist.<br/> |



 

 

 
