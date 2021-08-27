---
title: Erleichterte Bedienung-Technologieregistrierung
description: In diesem Artikel wird erläutert, wie Sie eine Barrierefreiheitsanwendung beim Center für erleicherte Bedienung. Außerdem wird erläutert, wie Sie Ihre Barrierefreiheitsanwendung so anpassen, dass sie gut mit dem sicheren Desktop funktioniert.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 28b76356f22c8cde66bce077feea52cd267a5e71
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623286"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Erleichterte Bedienung-Technologieregistrierung

In diesem Artikel wird erläutert, wie Sie eine Barrierefreiheitsanwendung beim Center für erleicherte Bedienung. Außerdem wird erläutert, wie Sie Ihre Barrierefreiheitsanwendung so anpassen, dass sie gut mit dem sicheren Desktop funktioniert.

Das Center für erleicherte Bedienung ist eine Systemsteuerung-Anwendung für Microsoft Windows bietet Funktionen für Barrierefreiheit und Benutzerfreundlichkeit. Mithilfe der Center für erleicherte Bedienung können Benutzer ihre Computer so konfigurieren, dass sie ihren physischen und kognitiven Anforderungen entsprechen.

Eine Funktion der Center für erleicherte Bedienung besteht in der Unterstützung von Benutzern beim Starten von Barrierefreiheitsanwendungen, einschließlich Sprachausgabe, Bildschirmtastatur und Bildschirmlupe. Registrierte Anwendungen von Drittanbietern werden auch in der Center für erleicherte Bedienung und können direkt von dort aus gestartet werden.

Barrierefreiheitsanwendungen müssen reibungslos mit dem sicheren Desktop funktionieren. Der sichere Desktop ist die Benutzeroberfläche, die angezeigt wird, wenn der Computer gesperrt ist (bei der Anmeldung oder wenn der Benutzer den Desktop gesperrt hat), und wenn der Benutzer aufgefordert wird, eine potenziell unsichere Aktion zu erlauben. Aus Sicherheitsgründen werden Windows Drittanbietersoftware, die auf dem sicheren Desktop ausgeführt wird, begrenzt. Wenn Ihre Barrierefreiheitsanwendung auf dem sicheren Desktop ausgeführt werden soll, müssen Sie die Anwendung beim Center für erleicherte Bedienung.

## <a name="registering-with-the-ease-of-access-center"></a>Registrieren beim Center für erleicherte Bedienung

Barrierefreiheitsanwendungen werden beim Center für erleicherte Bedienung, indem sie einen oder mehrere Registrierungsschlüssel erstellen, wenn die Anwendung installiert wird. In der folgenden Tabelle sind die In den Registrierungsschlüsseln enthaltenen Informationen aufgeführt.



| Name                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obligatorisch/Optional | Sprache      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Anwendungsname            | Der Name der Anwendung, die sich in einer Ressourcendatei befindet. Dieser Registrierungswert enthält eine Zeichenfolge in einem angegebenen Format. Dies kann eine lokalisierte Version des Anwendungsnamens sein, wenn die Anwendung in anderen Sprachen als Englisch lokalisiert ist. Der Name wird in der Center für erleicherte Bedienung.<br/>                                                                                                                                                                                                                                                                                       | Obligatorisch.          | Lokalisierte     |
| ATExe                       | Der Name der ausführbaren Datei oder des Images der Anwendung. Windows verwendet diesen Wert, um zu bestimmen, ob die Barrierefreiheitsanwendung ausgeführt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obligatorisch.          | Nicht lokalisiert |
| CopySettingsToLockedDesktop | Ein **DWORD-Wert,** der angibt, ob die Einstellungen der Barrierefreiheitsanwendung auf den gesperrten Desktop kopiert werden.<br/> Wenn dieser Wert 1 ist, kann die Anwendung Einstellungen an einen Speicherort in der Benutzerregistrierung schreiben, und Windows kopiert die Einstellungen an denselben Speicherort in der Benutzerregistrierung für den gesperrten Desktop. Dadurch kann die Anwendung ihren Zustand vom "normalen" Desktop auf dem gesperrten Desktop beibehalten.<br/>                                                                                                                                                             | Optional           | Nicht lokalisiert |
| Beschreibung                 | Eine kurze Beschreibung der Anwendung aus einer Ressourcendatei. Dieser Registrierungswert enthält eine Zeichenfolge in einem angegebenen Format. Dies kann eine lokalisierte Version der Beschreibung sein, wenn die Anwendung in anderen Sprachen als Englisch lokalisiert ist. Die Länge dieser Zeichenfolge muss weniger als 512 Zeichen umfassen.<br/> Die Beschreibung wird in der Center für erleicherte Bedienung, um dem Benutzer zusätzliche Informationen zur Barrierefreiheitsanwendung zur Verfügung zu stellen.<br/> Dieser Wert kann auch verwendet werden, um den Benutzer zu benachrichtigen, dass die Anwendung nicht auf dem sicheren Desktop verwendet wird.<br/>      | Obligatorisch.          | Lokalisierte     |
| Profil                     | Ein kurzer XML-Code, der die von der Anwendung zur Verfügung stellenden Füllungen angibt. Dadurch wird sichergestellt, dass die Anwendung unter der richtigen Kategorie in der Center für erleicherte Bedienung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Obligatorisch.          | Nicht lokalisiert |
| PassiveAutoStartBehavior    | <p>Ein **DWORD-Wert,** der angibt, ob das Legacyverhalten für den automatischen Start aktiviert ist.</p><p>Der Standardwert ist 0 ( 0), was angibt, dass ein AT ein älteres Verhalten für den automatischen Start erfordert. Dies bewirkt, dass die Einstellung "Nach der Anmeldung starten" für at in der Out-of-Box-Umgebung (OOBE) und Systemsteuerung (siehe **Systemsteuerung -> Erleichterte Bedienung -> Center für erleicherte Bedienung -> Change sign-in settings)** überprüft wird und at nach UAC und Sperrbildschirm automatisch gestartet wird.</p><p>Der Wert 1 gibt an, dass AT das neue Automatische Startverhalten verwenden soll, bei dem die Einstellung "Nach Der Anmeldung starten" für at nicht in der Out-of-Box-Benutzeroberfläche (OOBE) und Systemsteuerung überprüft wird und AT nur dann automatisch einmal pro Benutzersitzung (bei der Anmeldung) gestartet wird, wenn die Einstellung "Nach Anmeldung starten" überprüft wird.</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Optional          | Nicht lokalisiert |
| SecureDesktopAccommodation  | Der Name einer alternativen Barrierefreiheitsanwendung, die auf dem sicheren Desktop statt auf dieser Anwendung ausgeführt werden soll. Die Alternative kann eine andere Anwendung, eine andere Version derselben Anwendung, eine der in Windows enthaltenen Barrierefreiheitsanwendungen oder "none" sein, wenn Sie keine Barrierefreiheitsanwendung auf dem sicheren Desktop ausführen möchten. <br/>                                                                                                                                                                                                               | Optional           | Nicht lokalisiert |
| Einfaches Profil              | Ein -Wert, der beschreibt, wie die Anwendung in einem oder zwei Wörtern klassifiziert wird: Sprachausgabe, Bildschirmlupe oder Bildschirmtastatur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Obligatorisch.          | Nicht lokalisiert |
| StartExe                    | Der vollständige Pfad der ausführbaren Datei. Dieser Wert wird verwendet, um die Barrierefreiheitsanwendung zu starten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obligatorisch.          | Nicht lokalisiert |
| StartParams                 | Befehlszeilenargumenten Diese Werte werden zusammen mit StartExe verwendet, um die Anwendung zu starten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Optional           | Nicht lokalisiert |
| TerminateOnDesktopSwitch    | Ein **DWORD-Wert,** der angibt, wie die Barrierefreiheitsanwendung auf Übergänge zum oder vom sicheren Desktop reagiert.<br/> Wenn dieser Wert nicht vorhanden ist oder 1 ist, Windows die Anwendung bei jedem Übergang zum oder vom sicheren Desktop beendet und neu gestartet. Dies ist das Standardverhalten.<br/> Wenn dieser Wert 0 ist, Windows die Barrierefreiheitsanwendung bei einem Desktopübergang nicht beendet. Die Anwendung wird weiterhin auf dem vorherigen Desktop ausgeführt, und Windows eine neue Instanz auf dem neuen Desktop gestartet, wenn dort noch keine Instanz ausgeführt wird.<br/> | Optional           | Nicht lokalisiert |


 

### <a name="localization"></a>Lokalisierung

Die Registrierungswerte von Anwendungsname und Beschreibung müssen lokalisierbar sein, um die mehrsprachige Benutzeroberfläche (MEHRSPRACHIGE BENUTZEROBERFLÄCHE) zu unterstützen.

Diese Zeichenfolgen haben das folgende Format, wobei eckige Klammern erforderliche Elemente und eckige Klammern ein optionales Element bedeuten.

*@<ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*

*<ResDllPath \\ ResDLLFilename>* pfad zur Ressourcen-DLL. Der Pfad kann Umgebungsvariablen enthalten.

*<resID>* ist die Ressourcen-ID für die Zeichenfolge.

*\[ comment \]* enthält optionale Kommentare.

Beispiel:


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



Weitere Informationen zu CENTERS finden Sie unter [Windows KNOWLEDGE Center](../intl/about-multilingual-user-interface.md).

### <a name="hci-profile"></a>HCI-Profil

Das HCI-Profil (Human Computer Interaction) ist eine Möglichkeit, basierend auf den Anforderungen des Benutzers zu bestimmen, welche Lösungen zu bieten sind. Barrierefreiheitsanwendungen sollten Informationen über die Art von Behinderungen registrieren, die die Anwendung unterstützen kann.

Der Profilregistrierungswert enthält XML, in dem die Art von Behinderungen beschrieben wird, auf die die Barrierefreiheitsanwendung abzielt. Dieser XML-Code hat das folgende Format:


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



Die gültigen Werte für das Typattribut **"Zugeführt"** sind wie folgt:

-   Sehvermögen
-   Schwerwiegendes Sehen
-   Cognitive Services
-   schwerwiegende kognitive
-   Dexterity
-   Starke Dexterität
-   Hörvermögen
-   Schwerhörigkeit
-   Spracherkennung
-   Schwerwiegende Spracherkennung

> [!Note]  
> Bei diesen Werten wird zwischen Groß-/Kleinschreibung unterschieden.

 

Wenn eine Barrierefreiheitsanwendung mehrere Beherkunftungen unterstützt, sollte der Profilregistrierungswert ein **Attribut vom Typ "Barrierefreiheit"** für jede Variante enthalten.

### <a name="ease-of-access-registry-details"></a>Erleichterte Bedienung Registrierungsdetails

Um Ihre Barrierefreiheitsanwendung zu registrieren, müssen Sie einen Schlüssel für Ihre Anwendung am folgenden Registrierungsspeicherort erstellen und ihn mit Name-Wert-Paaren auffüllen.

**HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion Accessibility \\ \\ ATs\\**

Benennen Sie den Registrierungsschlüssel Ihrer Anwendung im folgenden Format:

*"CompanyName \_ ProductName \_ v \# "*

Beispiel: \_ "Contoso-Bildschirmlupe \_ v2.0".

Zum Hinzufügen von Registrierungswerten muss das Installationsprogramm mit erhöhten Rechten ausgeführt werden.

### <a name="secure-desktop-accommodation"></a>Sichere Desktopdarstellung

Mit **dem Registrierungsschlüssel SecureDesktopAccommodation** können Sie angeben, wie Ihre Barrierefreiheitsanwendung auf den sicheren Desktop reagiert. Standardmäßig startet der Center für erleicherte Bedienung Ihre Anwendung auf dem sicheren Desktop, wenn sie bereits auf dem normalen Desktop ausgeführt wurde oder für die Ausführung auf dem Anmeldedesktop konfiguriert ist. Mit dem **Schlüssel SecureDesktopAccommodation** haben Sie folgende Möglichkeiten:

-   Geben Sie eine alternative Version Ihrer Anwendung für die Verwendung auf dem sicheren Desktop an. Beispielsweise verfügen Sie möglicherweise über eine alternative Version, die unsichere Features deaktiviert oder optimiert ist, um weniger Arbeitsspeicher zu verwenden und schneller zu starten.

    Legen Sie zum Angeben der alternativen Version den **Schlüssel SecureDesktopAccommodation** auf den Namen der alternativen Version fest. Wenn Sie Ihre Anwendung beispielsweise mit dem Schlüssel Contoso \_ Screen Reader \_ v1.0 registriert haben, können Sie die alternative Version unter Contoso \_ Screen ReaderSecure \_ v1.0 registrieren. Legen Sie dann den **Schlüssel SecureDesktopAccommodation** von Contoso \_ Screen Reader \_ v1.0 auf "Contoso \_ Screen ReaderSecure \_ v1.0" fest.

-   Geben Sie anstelle Ihrer Anwendung eine Microsoft-Barrierefreiheitsanwendung an, die auf dem sicheren Desktop verwendet werden soll. Legen Sie für diese Option **SecureDesktopAccommodation** auf den Namen der jeweiligen Microsoft-Barrierefreiheitsanwendung fest: "osk", "Bildschirmlupe" oder "Sprachausgabe".
-   Geben Sie an, dass Ihre Anwendung nicht auf dem sicheren Desktop ausgeführt werden soll, und keine alternative Anwendung. Legen Sie für diese Option **SecureDesktopAccommodation** auf "none" (empfehlungsgemäß) oder den Namen einer nicht vorhandenen Anwendung fest.

Wenn der **SecureDesktopAccommodation-Registrierungsschlüssel** für Ihre Barrierefreiheitsanwendung eine Microsoft-Barrierefreiheitsanwendung angibt, die auf dem sicheren Desktop anstelle Ihrer Anwendung ausgeführt werden soll, benachrichtigt Windows den Benutzer bei der Umstellung auf den sicheren Desktop darüber. Um den Benutzer zu benachrichtigen, zeigt Windows die zeichenfolge an, die im Registrierungsschlüssel Beschreibung für Ihre Anwendung angegeben ist. Wenn z. B. die ScreenReader-Anwendung "Screens 1.0" die Microsoft-Sprachausgabe auf dem sicheren Desktop verwendet, enthält sie eine Beschreibungszeichenfolge, z. B. "Microsoft-Sprachausgabe wird in den gesperrten, angemeldeten und anderen sicheren Desktops anstelle von ScreenReader Editions 1.0 verwendet."

Wenn der **SecureDesktopAccommodation-Schlüssel** Ihrer Anwendung auf "none" festgelegt ist, verwenden Sie den **Description-Schlüssel,** um dem Benutzer mitzuteilen, dass Ihre Anwendung auf dem sicheren Desktop nicht verfügbar ist und keine Alternative bereitgestellt wird.

Windows zeigt den Beschreibungstext an den relevanten Stellen im Center für erleicherte Bedienung an.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>Wird bei der Installation und auf dem Anmeldedesktop ausgeführt

Wenn Sie den Namen des registrierten Schlüssels Ihrer Barrierefreiheitsanwendung an die Zeichenfolge am folgenden Registrierungsspeicherort anfügen, startet Windows Die Anwendung sofort nach der Installation. Außerdem führt Windows Ihre Anwendung automatisch aus, wenn der Anmeldedesktop aktiv ist.

**HKCU \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion Accessibility \\ \\ Configuration**

Der Konfigurationsschlüssel ist eine durch Trennzeichen getrennte Zeichenfolge. Um Ihre Anwendung hinzuzufügen, fügen Sie eine Zeichenfolge an, die mit dem Registrierungsschlüssel Ihrer Anwendung unter HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion Accessibility ATs identisch \\ \\ \\ ist.

### <a name="running-in-a-job"></a>Ausführen in einem Auftrag

Wenn der **TerminateOnDesktopSwitch-Registrierungsschlüssel** nicht vorhanden oder auf ungleich 0 (null) festgelegt ist, führt Windows die Anwendung im Kontext eines Auftrags aus, wobei die Anwendung bei jedem Desktopübergang beendet und neu gestartet wird. Die Ausführung in einem Auftrag stellt sicher, dass nur eine einzelne Instanz der Anwendung zu einem bestimmten Zeitpunkt ausgeführt wird, und verhindert, dass die Anwendung den Desktopzustand überwachen muss. Die Ausführung in einem Auftrag hat folgende Nachteile:

-   Die Anwendung verursacht bei jedem Desktopübergang Startkosten.
-   Die Anwendung kann nur über die Center für erleicherte Bedienung gestartet werden.
-   Die Anwendung muss ihre Einstellungen kontinuierlich speichern, da sie jederzeit durch einen Desktopübergang beendet werden kann.

Wenn der **TerminateOnDesktopSwitch-Schlüssel** vorhanden ist und auf 0 festgelegt ist, führt Windows die Anwendung für die Barrierefreiheit nicht in einem Auftrag aus. Dies bietet die folgenden Vorteile:

-   Desktopübergängen sind keine Startkosten zugeordnet.
-   Die Anwendung kann außerhalb des Center für erleicherte Bedienung gestartet werden.

Die Nachteile der Nichtausführung in einem Auftrag sind:

-   Da die Anwendung bei Desktopübergängen nicht neu gestartet wird, muss sie erkennen, wann der aktuelle Desktop inaktiv ist, und entsprechend reagieren. Beispielsweise muss die Anwendung die Kontrolle über die Hardware abgeben, damit die sichere Desktopversion der Anwendung sie verwenden kann, und die Anwendung sollte in den Standbymodus wechseln, um die Verwendung von Prozessorressourcen zu vermeiden.
-   Wenn die Anwendung über den Startmenü, Windows Explorer oder die Befehlszeile gestartet werden kann, muss die Center für erleicherte Bedienung informiert werden. Weitere Informationen finden Sie unter **Windows Logo-Taste + U**.
-   Da mehrere Kopien der Anwendung gleichzeitig auf verschiedenen Desktops ausgeführt werden können, muss die Anwendung geschrieben werden, um mehrere ausgeführte Kopien zu unterstützen.

### <a name="windows-logo-key--u"></a>Windows LOGO-TASTE + U

Wenn Ihre Barrierefreiheitsanwendung für die Ausführung in einem Auftrag konfiguriert ist, sollte der Startcode Ihrer Anwendung einen Aufruf der [**IsProcessInJob-Funktion**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) enthalten, um zu bestimmen, ob die Anwendung in einem Auftrag gestartet wird. Ist dies der Grund, sollte die Anwendung den Center für erleicherte Bedienung starten und dann beenden. Das folgende Beispiel zeigt, wie **IsProcessInJob** aufgerufen wird.


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Wenn die Anwendung für die Barrierefreiheit so konfiguriert ist, dass sie außerhalb eines Auftrags ausgeführt wird, sollte sie die Center für erleicherte Bedienung benachrichtigen, dass die Anwendung gestartet wird und wie gewohnt fortgesetzt wird.

Unabhängig davon, wie die Anwendung konfiguriert ist, muss die Anwendung den Center für erleicherte Bedienung benachrichtigen, dass sie beendet wird, wenn sie eine Möglichkeit zum Beenden innerhalb der Anwendung bietet, z. B. eine Schaltfläche Schließen.

Eine Anwendung benachrichtigt die Center für erleicherte Bedienung, indem sie einen temporären Registrierungsschlüssel festlegt und dann die Kombination aus Windows Logo-Taste und U-Taste in den Eingabestream eingibt.

Die Anwendung sollte den temporären Schlüssel am folgenden Speicherort erstellen.

**HKCU \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ AccessibilityTemp**

Der temporäre Schlüssel sollte den gleichen Namen wie der registrierte Anwendungsname aufweisen, z. B. "Contoso \_ Screen Reader \_ v1.0". Der Wert des Schlüssels ist ein **DWORD,** das auf 0x0003 festgelegt ist, wenn er gestartet wird, oder 0x0002, wenn die Anwendung beendet wird.


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a>Windows Logo-Taste + Volume Up

Wenn der Benutzer Ihre Barrierefreiheitsanwendung startet, indem er die Tastenkombination Windows Logo-Taste + Volume-Up-Taste (z. B. auf einem Tabletgerät) drückt, übergibt der Center für erleicherte Bedienung das folgende Befehlszeilenargument an die Anwendung:

**/hardwarebuttonlaunch**

Ihre Anwendung kann dieses Argument verwenden, um zu bestimmen, ob normal gestartet oder das Verhalten entsprechend angepasst werden soll.

### <a name="transferring-secure-desktop-settings"></a>Übertragen sicherer Desktopeinstellungen

Wenn Ihre Barrierefreiheitsanwendung den sicheren Desktop unterstützt, können Sie die Registrierung verwenden, um Einstellungen zu kopieren, wenn die Anwendung auf den sicheren Desktop umgestellt wird. Das Kopieren von Einstellungen erleichtert dem Benutzer den Übergang zum sicheren Desktop.

Legen Sie zum Kopieren von Einstellungen den Registrierungsschlüssel CopySettingsToLockedDesktop der Anwendung auf 1 fest, und speichern Sie die Einstellungen am folgenden Registrierungsspeicherort.

**HKCU \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion Accessibility \\ \\ ATConfig\\<AT Key Name>**

Der Center für erleicherte Bedienung überwacht diesen Registrierungsspeicherort, während die Anwendung ausgeführt wird. Wenn ein Übergang zum sicheren Desktop erfolgt, kopiert der Center für erleicherte Bedienung die Einstellungen an den gleichen Speicherort in der HKCU-Struktur des sicheren Desktops. Die Anwendung kann dann die Einstellungen lesen und ihren Zustand fortsetzen.

Ihre Barrierefreiheitsanwendung sollte ihre Einstellungen in regelmäßigen Abständen oder immer dann schreiben, wenn sich die Werte ändern. Das Schreiben von Einstellungen beim Beenden der Anwendung funktioniert nicht. Wenn die Anwendung in einem Auftrag ausgeführt wird, wird sie beim Übergang vom sicheren Desktop beendet, bevor der Exitcode ausgeführt werden kann. Wenn die Anwendung nicht in einem Auftrag ausgeführt wird, wird die Anwendung beim Übergang vom sicheren Desktop nicht beendet.

### <a name="caution"></a>Achtung

Da die hier beschriebenen Registrierungsschlüssel im Benutzermodus geschrieben werden, sind sie nicht sicher. Wenn Ihre Barrierefreiheitsanwendung den Inhalt dieser Schlüssel liest, sollten sie die Daten sorgfältig überprüfen und mit Vorsicht verwenden. Insbesondere sollte Ihre Anwendung eine Begrenzungsprüfung für **DWORD-Werte** durchführen, mit Zeichenfolgenlängen vorsichtig sein, Plug-In-DLL-Namen nicht lesen und keine Befehle ausführen, die in Zeichenfolgen gefunden wurden.

## <a name="registry-examples"></a>Registrierungsbeispiele

Das folgende Beispiel zeigt die möglichen Registrierungswerte für ein fiktives Produkt namens Contoso ScreenReader Version 2.0, dessen lokalisierter Name als Ressource gespeichert wird.

Die Werte in der Tabelle befinden sich unter dem folgenden Schlüssel:

**HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion Accessibility \\ \\ ATs Contoso Screen Reader \\ \_ \_ v2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>Daten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@%SystemRoot%\system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>Beschreibung</td>
<td>REG_SZ</td>
<td>@%SystemRoot%\system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>SecureDesktopAccommodation</td>
<td>REG_SZ</td>
<td>Narrator</td>
</tr>
</tbody>
</table>



 

Wenn die Anwendung sowohl eine Sprachausgabe als auch eine Bildschirmlupe in einer einzelnen ausführbaren Datei enthält, können die Werte für die Sprachausgabekomponente wie die folgenden aussehen:



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>Daten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-30</td>
</tr>
<tr class="even">
<td>Beschreibung</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-32</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

Die Werte für die Lupenkomponente sind im folgenden Schlüssel angegeben:

**HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Contosoibility \\ ATs Contoso \\ \_ Magnifier \_ v2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>Daten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-31</td>
</tr>
<tr class="even">
<td>Beschreibung</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-42</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>Vergrößerung</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>c:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

