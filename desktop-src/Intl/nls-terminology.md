---
description: In diesem Thema werden Begriffe definiert, die beim Arbeiten mit NLS-Funktionen wichtig sind.
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: NLS-Terminologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a86808d31cb034e7ad29e4580b8f201ad3c9a6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760177"
---
# <a name="nls-terminology"></a>NLS-Terminologie

In diesem Thema werden Begriffe definiert, die beim Arbeiten mit NLS-Funktionen wichtig sind.

## <a name="locale-and-language-terms"></a>Gebiets Schema-und Sprachbedingungen

In der folgenden Tabelle werden Gebiets Schema-und sprachbegriffe zusammengefasst. Siehe auch Gebiets Schemas [und Sprachen](locales-and-languages.md).



|                          | Sprachgruppe                                                                                                                                                                                                                                                                   | Sprache für Programme, die Unicode nicht unterstützen                                                                                                                                                                                                                | Standards und Formate                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zweck**              | Bietet alle Tastaturlayouts, Eingabemethoden-Editoren (IMEs), TrueType-Schriftarten, Schriftart Verknüpfungen, Lizenzpaket Dateien (Lpls), Bitmap-Schriftarten und Codepage-Übersetzungstabellen, die vom Betriebssystem für eine Gruppe von Sprachen benötigt werden. Wirkt sich daher auf alle anderen Einstellungen in dieser Liste aus. | Bestimmt, welche Bitmap-Schriftarten und OEM-, ANSI-und Macintosh-Codepages Standardwerte für das Betriebssystem sind. Diese Sprache wirkt sich nur auf Anwendungen aus, die nicht vollständig Unicode sind. Vor Windows XP wurde diese Sprache als "System locale" bezeichnet. | Bestimmt, welche Einstellungen zum Formatieren von Datumsangaben, Uhrzeiten, Währungen und Zahlen als Standardwert für jeden Benutzer verwendet werden. Bestimmt auch die Sortierreihenfolge für das Sortieren von Text. Vor Windows XP wurden Standards und Formate als "User locale" bezeichnet. |
| **Erster Satz**            | Installation                                                                                                                                                                                                                                                                     | Installation                                                                                                                                                                                                                                     | Installation                                                                                                                                                                                                                            |
| **Ändern der Benutzer Änderung** | Regionale Optionen (System Steuerungselement)<br/> **Windows XP:** Regions-und Sprachoptionen<br/> (nur Administratoren)<br/>                                                                                                                                       | Regionale Optionen (System Steuerungselement)<br/> **Windows XP:** Regions-und Sprachoptionen<br/> (nur Administratoren)<br/>                                                                                                       | Regionale Optionen (System Steuerungselement)<br/> **Windows XP:** Regions-und Sprachoptionen<br/>                                                                                                                               |
| **Standard**              | Westeuropa und USA und Sprachgruppe sind erforderlich, um die Sprache einer lokalisierten Version anzuzeigen.                                                                                                                                                                         | Sprache der lokalisierten Version.                                                                                                                                                                                                                   | Sprache des lokalisierten Betriebssystems.                                                                                                                                                                                                 |
| **Function**             | [**Enumsystemlanguagegroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid), [ **getuserdefaultlocalename**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | Thread Gebiets Schema                                                                                                                                                 | Eingabe Sprache                                                                                            | Standardbenutzer Oberflächen Sprache des Systems                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zweck**              | Legt die Einstellungen fest, die zum Formatieren von Datumsangaben, Uhrzeiten, Währungen und großen Zahlen für einen Thread verwendet werden. Bestimmt auch die Sortierreihenfolge für das Sortieren von Text. | Besteht aus einer Sprache und einer Methode der Eingabe.                                                             | Legt die Standardsprache von Menüs und Dialogfeldern, Meldungen, Setup Informationsdateien (INF) und Hilfedateien fest.<br/> **Windows Vista und höher:** Wird als Installationssprache bezeichnet. Spielt eine eingeschränktere Rolle, die größtenteils durch bevorzugte Benutzeroberflächen Sprachen abgelöst wird.<br/> Weitere Informationen finden Sie unter [sprach Verwaltung in der Benutzeroberfläche](user-interface-language-management.md) .<br/> |
| **Erster Satz**            | Standardeinstellung für Standards und Formate                                                                                                                              | Installation                                                                                              | Installation                                                                                                                                                                                                                                                                                                                                                                                   |
| **Ändern der Benutzer Änderung** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    | Regionale Optionen (System Steuerungselement)<br/> **Windows XP:** Regions-und Sprachoptionen<br/> | Nein                                                                                                                                                                                                                                                                                                                                                                                             |
| **Standard**              | Standards und Formate                                                                                                                                         | Sprache der lokalisierten Version mit der Standardeingabe Methode.                                                  | Sprache der lokalisierten Version.                                                                                                                                                                                                                                                                                                                                                                 |
| **Function**             | [**Getthreadlocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | Benutzeroberflächen Sprache des Systems, bevorzugte Benutzeroberflächen Sprachen                                                                                                                                                                  | Benutzeroberflächen Sprache, Benutzer bevorzugte UI-Sprachen                                                                                                                                               | Thread bevorzugte UI-Sprachen                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zweck**              | Bestimmen Sie die Sprache von Menüs und Dialogfeldern, Meldungen, INF-Dateien und Hilfedateien für das Betriebssystem. Weitere Informationen finden Sie unter [sprach Verwaltung in der Benutzeroberfläche](user-interface-language-management.md). | Bestimmen Sie die Sprache von Menüs und Dialogfeldern, Meldungen und Hilfedateien für den Benutzer. Weitere Informationen finden Sie unter [sprach Verwaltung in der Benutzeroberfläche](user-interface-language-management.md). | **Windows Vista und höher:** Geben Sie die bevorzugten Sprachen für Anwendungsthreads an. Weitere Informationen finden Sie unter [sprach Verwaltung in der Benutzeroberfläche](user-interface-language-management.md). |
| **Erster Satz**            | Standardwert NULL                                                                                                                                                                                                    | Standardwert NULL                                                                                                                                                                             | Standardwert NULL                                                                                                                                                                               |
| **Ändern der Benutzer Änderung** | Regions- und Sprachoptionen<br/> (nur Administratoren)<br/>                                                                                                                                          | Regionale Optionen (System Steuerungselement)<br/> **Windows XP:** Regions-und Sprachoptionen<br/>                                                                                   | [**Setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **Standard**              | **Windows Vista und höher:** Sprache der lokalisierten Version, gefolgt von allen Fallbacks.                                                                                                                             | **Vor Windows Vista:** Sprache der lokalisierten Version.<br/> **Windows Vista und höher:** Sprache der lokalisierten Version, gefolgt von allen Fallbacks.<br/>                     | NULL-Liste                                                                                                                                                                                     |
| **Function**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage), [ **getuserpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**Getthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | Bevorzugte Benutzeroberflächen Sprachen verarbeiten                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zweck**              | **Windows 7 und höher:** Bestimmen Sie die bevorzugten Sprachen für einen Anwendungsprozess. Weitere Informationen finden Sie unter [sprach Verwaltung in der Benutzeroberfläche](user-interface-language-management.md). |
| **Erster Satz**            | Standardwert NULL                                                                                                                                                                                |
| **Ändern der Benutzer Änderung** | Regions-und Sprachoptionen (nur Administratoren)                                                                                                                                            |
| **Standard**              | **Windows 7 und höher:** Sprache der lokalisierten Version, gefolgt von allen Fallbacks.                                                                                                             |
| **Function**             | [**Getprocesliniferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages), [ **setprocesliniferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>Codepage

Die Verwendung von Code Punkten mit 256-Code Punkten, um das Mischen von Skripts in einem einzelnen Text zu unterstützen, war einer der Hauptgründe für die Zunahme von Unicode. Codepages sind für das Schreiben von Konsolen Code, für die Wartung älterer Anwendungen oder die Ausführung unter älteren Versionen von Windows und für die Schnittstellen mit einer nicht-Microsoft-Software, die nicht für Unicode aktiviert ist, wichtig.

## <a name="input-language"></a>Eingabe Sprache

Die Eingabe Sprache wird durch eine Daten Variable pro Prozess dargestellt, die eine Sprache (z. b. Griechisch) und eine Eingabemethode (z. b. die Tastatur) beschreibt. Es können mehrere Eingabe Sprachen installiert werden, und der Benutzer kann zwischen diesen wechseln.

Um den Wert der Eingabe Sprache festzulegen und abzurufen, ruft die Anwendung [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) bzw. [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)auf. Benutzer können Eingabe Sprachen über die Registerkarte **Sprachen** im Bereich Regions-und Sprachoptionen der Systemsteuerung hinzufügen und entfernen.

Die Standardeingabe Sprache ist die lokalisierte Sprache des Betriebssystems, und Sie ist die Einstellung, die aktiv ist, wenn eine neue Anwendung gestartet wird (oder wenn ein neues Fenster für einige Anwendungen geöffnet wird). Der Wechsel zu einer anderen Eingabe Sprache erfolgt pro Anwendung. Mit anderen Worten, zwei verschiedene Eingabe Sprachen können in zwei verschiedenen Anwendungen verwendet werden. Ein Benutzer kann z. b. Deutsch mithilfe des internationalen USA Tastaturlayouts, Englisch mit Spracheingabe (mit nicht-Microsoft-Software) und Spanisch mit einem IME in drei verschiedenen Anwendungen eingeben.

## <a name="language-for-non-unicode-programs"></a>Sprache für nicht-Unicode-Programme

Die Sprache für nicht-Unicode-Programme (früher als "System locale" bezeichnet) bestimmt die Codepage, die standardmäßig auf dem Betriebssystem verwendet wird. Die Einstellung Sprache für nicht-Unicode-Programme wirkt sich nur auf nicht-Unicode-Anwendungen aus, d. h. auf ANSI-Anwendungen. Das Festlegen der Sprache weist Windows an, ein nicht-Unicode-basiertes Betriebssystem zu emulieren, das in dieser Sprache lokalisiert wird. Wenn Sie die Sprache für nicht-Unicode-Programme ändern, werden die erforderlichen bitmapschriftdateien installiert, um nicht-Unicode-Anwendungen in der angegebenen Sprache zu unterstützen. Damit der Benutzer eine Sprache für nicht-Unicode-Programme auswählen kann, muss die entsprechende Sprachgruppe installiert sein. Die Anwendung benötigt die Skriptunterstützung, um eine Sprache für nicht-Unicode-Programme auszuwählen. Die Sprache für nicht-Unicode-Programme ist eine Einstellung pro System und erfordert die Implementierung eines Neustarts.

Manchmal gibt es keinen erkennbaren Unterschied zwischen zwei Sprachen für nicht-Unicode-Programme. Dies ist beispielsweise bei den Gebiets Schemata Deutsch (neutral) und Deutsch (Österreich) der Fall. Im Allgemeinen sind die Einstellungen einer Sprachgruppe sehr ähnlich und unterscheiden sich nur in der OEM-oder Mac-Codepage.

Eine ANSI-Anwendung sollte während der Installation die Einstellung Sprache für nicht-Unicode-Programme überprüfen. Zum Abrufen des Werts wird [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) oder [**getoken**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) verwendet. Zum Festlegen der Sprache für nicht-Unicode-Programme wird keine Funktion unterstützt. Benutzer können Sie jedoch im Bereich Regions-und Sprachoptionen in der Systemsteuerung mithilfe der Registerkarte **erweitert** ändern. Im folgenden finden Sie einige Beispiele für Sprache für nicht-Unicode-Programmeinstellungen:

1.  Ein deutscher Benutzer, der eine japanische Anwendung ausführen möchte, die für Japanisch Windows 95 entwickelt wurde, muss Japanisch als Sprache für nicht-Unicode-Programme auswählen. Nach dieser Auswahl haben nicht-Unicode-deutsche Anwendungen Probleme. So werden z. b. die deutschen Umschlagstellen ("") nicht ordnungsgemäß angezeigt.
2.  Ein deutscher Benutzer, der japanischen Text in einer nicht-Unicode Deutsch-Anwendung eingeben möchte, muss Japanisch als Sprache für nicht-Unicode-Programme auswählen. Wie im ersten Beispiel verursacht dies Probleme bei der Eingabe von deutschem Text in nicht-Unicode-Anwendungen.
3.  Ein arabischer Benutzer, der Arabisch, Französisch und Englisch in einer nicht-Unicode-fremden Anwendung eingeben möchte, sollte Arabisch als Sprache für nicht-Unicode-Programme auswählen, da die arabische ANSI-Codepage die meisten französischen Zeichen und alle englischen Zeichen enthält.

## <a name="language-group"></a>Sprachgruppe

Die Sprachgruppe steuert die Sprache für nicht-Unicode-Programme, Standards und Formate, Eingabe Sprachen und Sprachen der Benutzeroberfläche, die ausgewählt werden können. Für jede lokalisierte Version ist die angegebene Sprachgruppe der Standardwert und kann nicht entfernt werden. Windows installiert z. b. standardmäßig die USA der Westeuropa und die Sprachgruppe. Wenn also die englische Version von Windows in einem anderen Land bzw. einer anderen Sprache als englischsprachige Version installiert wird, installiert der Benutzer in der Regel eine andere Sprachgruppe.

Beim Hinzufügen einer Sprachgruppe werden die erforderlichen Tastatur Dateien, Eingabemethoden-Editoren (Input Method Editors, IMEs), TrueType-Schriftart Dateien, Bitmap-Schriftart Dateien und NLS-Dateien (National Language Support) von Windows kopiert (aber nicht aktiviert). Durch das Hinzufügen einer Sprachgruppe werden auch Registrierungs Werte für die Schriftart Verknüpfung hinzugefügt und Skript-Engines für komplexe Skriptsprachen installiert (Arabisch, Hebräisch, indic und Thai).

Zusätzlich zur Sprachgruppe "Westeuropa" und "USA" sind 16 weitere Sprachgruppen vorhanden:



<table>
<tbody>
<tr class="odd">
<td><dl> Arabisch<br />
Armenisch<br />
Baltisch<br />
Mitteleuropa<br />
Kyrillisch<br />
Georgisch<br />
Griechisch<br />
Hebräisch<br />
</dl></td>
<td><dl> Indische<br />
Japanisch<br />
Koreanisch<br />
Chinesisch (vereinfacht)<br />
Chinesisch (traditionell)<br />
Thailändisch<br />
Türkisch<br />
Vietnamesisch<br />
</dl></td>
</tr>
</tbody>
</table>



 

Beliebige Zahlen und Kombinationen von Sprachgruppen können unter jedem beliebigen Betriebssystem installiert werden. Beispielsweise kann ein spanischer Benutzer die kyrillische Sprachgruppe installieren, um an russischen Texten zu arbeiten. In diesem Fall muss eine Textverarbeitungsanwendung auch die kyrillische Sprachgruppe unterstützen.

> [!Note]  
> Durch das Hinzufügen der entsprechenden Sprachgruppe kann eine Anwendung Text nicht automatisch akzeptieren. Tests werden empfohlen. Beispielsweise kann es sein, dass nicht-Unicode-Anwendungen die Sprache für nicht-Unicode-Programme ändern müssen.

 

## <a name="location"></a>Standort

**Windows XP:** Ein Speicherort ist ein geografischer Bezeichner. Sie wird durch eine benutzerspezifische Daten Variable dargestellt, die das Land bzw. die Region definiert, in der sich der Benutzer befindet.

Um den Wert festzulegen, ruft die Anwendung [**setusergeoid**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid)auf. Um den Wert abzurufen, ruft die Anwendung [**getusergeoid**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid)auf.

## <a name="standards-and-formats"></a>Standards und Formate

Standards und Formate (ehemals "User locale") ist eine benutzerspezifische Variable, die die Standard Sortierreihenfolge und die Standardeinstellungen für das Formatieren von Datumsangaben, Uhrzeiten, Währungen und Zahlen festlegt. Die Variable wird als Sprache dargestellt (manchmal in Kombination mit einem Land/einer Region), Sie ist jedoch keine Sprache selbst. Wenn Sie z. b. die Variable "Standards" und "Formats" auf Hebräisch festlegen, bedeutet dies, dass der Benutzer die Formatierungs Konventionen von Hebräisch, nicht notwendigerweise die hebräische Sprache, verwenden möchte Außerdem wird die Zeichenfolge, die für die Namen von Tagen und Monaten verwendet wird, von der Variablen "Standards" und "Formats" bestimmt. Wenn ein Benutzer beispielsweise "November 25, 1998" anzeigt, kann sich die Zeichenfolge "November" basierend auf der Variablen "Standards" und "Formats" ändern. Wenn Sie die Variable ändern, wird automatisch ein Eingabe Gebiets Schema mit den Standardeinstellungen für die Sprache hinzugefügt.

Um die Einstellung "Standards und Formate" zu erhalten, ruft die Anwendung [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) oder [**getuserdefaultlocalename**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)auf. Es ist keine nls-Funktion zum Festlegen der Variablen verfügbar. Benutzer können Sie jedoch im Bereich Regions-und Sprachoptionen in der Systemsteuerung über die Registerkarte **Regions Optionen** ändern.

Eine Anwendung sollte normalerweise die Standards und formatiert Variablen Einstellungen zum Anzeigen von Daten verwenden. Eine Anwendung, die ein festes Gebiets Schema zum Anzeigen von Daten verwendet, sollte jedoch einen bestimmten Gebiets Schema Bezeichner übergeben, anstatt locale \_ User Default zu verwenden \_ .

## <a name="thread-locale"></a>Thread Gebiets Schema

Das Thread Gebiets Schema wird durch eine Thread spezifische Gebiets Schema Daten Variable dargestellt, die die Formatierung von Datumsangaben, Uhrzeiten, Währungen und großen Zahlen für den Thread bestimmt. Der Standardwert ist der Wert für das Gebiets Schema, das derzeit für Standards und Formate ausgewählt ist. Um das Thread Gebiets Schema festzulegen, ruft die Anwendung [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)auf. Um das Thread Gebiets Schema abzurufen, ruft die Anwendung [**getthreadlocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)auf.

In den meisten Fällen sollte das Thread Gebiets Schema nicht überschrieben werden. Normalerweise sollte Sie nur verwendet werden, um das Thread Gebiets Schema einer Serveranwendung mit der Variablen "Standards und Formate" eines Client Computers zu synchronisieren. Beispielsweise muss eine Finanzaktien-Handels Anwendung für den Kurs Austausch in New York, der in den Banken weltweit verwendet wird, die Zeit-, Datums-und Aktienpreise in USA Formaten anzeigen. Diese Anwendung verwendet [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) , um das Thread Gebiets Schema auf Englisch (USA) festzulegen. Anschließend werden die NLS-Funktionen verwendet, um Datumsangaben, Uhrzeiten und Aktienpreise zu formatieren.

Das geänderte Thread Gebiets Schema wirkt sich nicht auf alle API-Funktionen aus. Daher ist es nicht immer eine zuverlässige Möglichkeit, die Standards und die Formats-Variable zu überschreiben. Stattdessen sollten Anwendungen, die Standards und Formate steuern, ein festes Gebiets Schema zum Anzeigen von Daten verwenden und dabei anstelle von locale User Default einen bestimmten Gebiets Schema Bezeichner übergeben \_ \_ .

## <a name="nls-example"></a>NLS-Beispiel

Das folgende Beispiel zeigt das Zusammenwirken zwischen Standards und Formaten, die Sprache für nicht-Unicode-Programme, den Speicherort und die Benutzeroberflächen Sprache des Benutzers.

Ein Benutzer, der ein System eigenes Chile ist, aber im USA lebt, verfügt über einen Computer, auf dem Windows XP Englisch ausgeführt wird. Der Benutzer legt den Speicherort auf USA fest, um einen Internet Dienstanbieter (Internet Service Provider, ISP) zu verwenden, um das Wetter für die USA zu Die Variable "Standards und Formats" ist jedoch auf Spanisch (Chile) festgelegt, sodass die Informationen gemäß den chilenischen Standards formatiert sind. Außerdem verwendet der Benutzer ein koreanisches Textverarbeitungsprogramm, bei dem es sich um eine ANSI-Anwendung handelt, sodass die Sprache für nicht-Unicode-Programme auf Koreanisch (Korea) festgelegt ist. Zur Verwendung der Anwendung verfügt der Benutzer über eine englische Tastatur und installiert außerdem einen koreanischen IME, um eine zweite Eingabe Sprache zu unterstützen. Der Mitarbeiter des Benutzers, der den Computer freigibt, aber nicht mit Englisch vertraut ist, kann die Benutzeroberflächen Sprache bei der Verwendung des Computers auf Spanisch (Spanien) festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> </dl>

 

 
