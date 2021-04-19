---
description: In diesem Thema werden die Arten von Fenster Klassen, die Art und Weise, wie das System Sie finden, und die Elemente beschrieben, die das Standardverhalten von Fenstern definieren, die zu Ihnen gehören.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Fenster Klassen (Windows und Meldungen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da95fc54a9527bade0d925c1f993cf853b0ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362899"
---
# <a name="window-classes-windows-and-messages"></a>Fenster Klassen (Windows und Meldungen)

In diesem Thema werden die Arten von Fenster Klassen, die Art und Weise, wie das System Sie finden, und die Elemente beschrieben, die das Standardverhalten von Fenstern definieren, die zu Ihnen gehören.

Eine Fenster Klasse ist ein Satz von Attributen, der vom System als Vorlage zum Erstellen eines Fensters verwendet wird. Jedes Fenster ist ein Member einer Fenster Klasse. Alle Fenster Klassen sind Prozess spezifisch.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Fenster Klassen](about-window-classes.md)     | Erläutert Fenster Klassen. Jede Fenster Klasse verfügt über eine zugeordnete Fenster Prozedur, die von allen Fenstern derselben Klasse gemeinsam genutzt wird. Die Fenster Prozedur verarbeitet Nachrichten für alle Fenster dieser Klasse und steuert somit das Verhalten und die Darstellung.<br/> |
| [Verwenden von Fenster Klassen](using-window-classes.md)     | Veranschaulicht, wie ein lokales Fenster registriert und zum Erstellen eines Hauptfensters verwendet wird.<br/>                                                                                                                                                                     |
| [Fenster Klassen Verweis](window-class-reference.md) | Enthält die API-Referenz.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Fenster Klassen Funktionen



| Name                                         | BESCHREIBUNG                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getclassinfoex**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Ruft Informationen zu einer Fenster Klasse ab, einschließlich eines Handles zum kleinen Symbol, das der Fenster Klasse zugeordnet ist. Die [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) -Funktion ruft kein Handle zum kleinen Symbol ab.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Ruft den angegebenen 32-Bit-Wert (**Long**) aus der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur ab, die dem angegebenen Fenster zugeordnet ist. <br/>                                                                         |
| [**Getclasslongptr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Ruft den angegebenen Wert aus der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur ab, die dem angegebenen Fenster zugeordnet ist.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Ruft den Namen der Klasse ab, zu der das angegebene Fenster gehört. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Ruft Informationen zum angegebenen Fenster ab. Die-Funktion ruft auch den 32-Bit-Wert (**Long**) am angegebenen Offset in den zusätzlichen Fenster Speicher ab.<br/>                                                    |
| [**Getwindowlongptr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Ruft Informationen zum angegebenen Fenster ab. Die-Funktion ruft auch den Wert an einem angegebenen Offset in den zusätzlichen Fenster Speicher ab.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registriert eine Fenster Klasse [**für die nachfolg**](/windows/win32/api/winuser/nf-winuser-createwindowa) Ende Verwendung in Aufrufen [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " von "" oder "" von "".<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registriert eine Fenster Klasse [**für die nachfolg**](/windows/win32/api/winuser/nf-winuser-createwindowa) Ende Verwendung in Aufrufen [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " von "" oder "" von "". <br/>                                                            |
| [**Setclasslongptr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Ersetzt den angegebenen Wert am angegebenen Offset im zusätzlichen Klassen Speicher oder in der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur für die Klasse, zu der das angegebene Fenster gehört.<br/>                              |
| [**Setclassword**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Ersetzt den 16-Bit-Wert (**Word**) am angegebenen Offset in den zusätzlichen Klassen Speicher für die Fenster Klasse, zu der das angegebene Fenster gehört.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Ändert ein Attribut im angegebenen Fenster. Die-Funktion legt auch den 32-Bit-Wert (Long) am angegebenen Offset in den zusätzlichen Fenster Speicher fest.<br/>                                                                 |
| [**Setwindowlongptr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Ändert ein Attribut im angegebenen Fenster. Die Funktion legt außerdem einen Wert am angegebenen Offset im zusätzlichen Fenster Speicher fest.<br/>                                                                                   |
| [**Unregisterclass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Hebt die Registrierung einer Fenster Klasse auf und gibt den für die Klasse benötigten Arbeitsspeicher frei. <br/>                                                                                                                                            |



 

Die folgenden Funktionen sind veraltet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></td>
<td>Ruft Informationen zu einer Fenster Klasse ab. <br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> -Funktion wurde durch die <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>getclassinfoex</strong></a> -Funktion abgelöst. Sie können jedoch immer noch <strong>GetClassInfo</strong>verwenden, wenn Sie keine Informationen zum kleinen Symbol der Klasse benötigen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>Getclassword</strong></a></td>
<td>Ruft den 16-Bit-Wert (<strong>Word</strong>) am angegebenen Offset in den zusätzlichen Klassen Speicher für die Fenster Klasse ab, zu der das angegebene Fenster gehört.
<blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert, wenn eine andere Verwendung als <em>nIndex</em> auf GCW_ATOM festgelegt ist. Die-Funktion wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Anwendungen sollten die <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> -Funktion verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></td>
<td>Ersetzt den angegebenen 32-Bit-Wert (<strong>Long</strong>) am angegebenen Offset im zusätzlichen Klassen Speicher oder in der <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> -Struktur für die Klasse, zu der das angegebene Fenster gehört.
<blockquote>
[!Note]<br />
Diese Funktion wurde durch die Funktion " <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>setclasslongptr</strong></a> " abgelöst. Verwenden Sie zum Schreiben von Code, der mit 32-Bit-und 64-Bit-Versionen von Windows kompatibel ist, <strong>setclasslongptr</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a>Fenster Klassenstrukturen



| Name                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Enthält die Fenster Klassenattribute, die von der [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion registriert werden. <br/> Diese Struktur wurde von der mit der [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion verwendeten [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur abgelöst. Sie können immer noch " [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) " und " [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) " verwenden, wenn Sie das kleine Symbol, das der Fenster Klasse zugeordnet ist, nicht festlegen müssen.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Enthält Fenster Klassen Informationen. Sie wird mit den Funktionen " [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) " und " [**getclassinfoex**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  " verwendet. <br/> Die [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur ähnelt der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur. Es gibt zwei Unterschiede. **WNDCLASSEX** enthält das **CBSIZE** -Element, das die Größe der Struktur angibt, und das **hiensm** -Element, das ein Handle für ein kleines Symbol enthält, das der Fenster Klasse zugeordnet ist.<br/> |



 

 

 
