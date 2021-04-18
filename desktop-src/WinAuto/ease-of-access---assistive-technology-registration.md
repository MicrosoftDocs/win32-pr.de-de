---
title: Easy of Access-hilfstechnologieregistrierung
description: In diesem Artikel wird erläutert, wie Sie eine Barrierefreiheits Anwendung mit dem Easy Access Center registrieren. Außerdem wird erläutert, wie Sie Ihre Barrierefreiheits Anwendung so anpassen, dass Sie gut mit dem sicheren Desktop funktioniert.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339287"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Easy of Access-hilfstechnologieregistrierung

In diesem Artikel wird erläutert, wie Sie eine Barrierefreiheits Anwendung mit dem Easy Access Center registrieren. Außerdem wird erläutert, wie Sie Ihre Barrierefreiheits Anwendung so anpassen, dass Sie gut mit dem sicheren Desktop funktioniert.

Das Easy of Access Center ist eine System Steuerungsanwendung für Microsoft Windows, die Funktionen für Barrierefreiheit und Benutzerfreundlichkeit vereint. Mithilfe des Easy Access Centers können Benutzer ihre Computer so konfigurieren, dass Sie Ihren physischen und kognitiven Anforderungen entsprechen.

Eine Funktion des Easy Access Centers besteht darin, Benutzern das Starten von Barrierefreiheits Anwendungen zu erleichtern, einschließlich Sprachausgabe, Bildschirmtastatur und Bildschirmlupe. Registrierte Anwendungen von Drittanbietern werden auch im Easy Access Center angezeigt und können direkt von dort aus gestartet werden.

Barrierefreiheits Anwendungen müssen problemlos mit dem sicheren Desktop arbeiten. Der sichere Desktop ist die Benutzeroberfläche, die angezeigt wird, wenn der Computer gesperrt ist (bei der Anmeldung oder wenn der Benutzer den Desktop gesperrt hat), und wenn der Benutzer aufgefordert wird, eine potenziell unsichere Aktion zuzulassen. Aus Sicherheitsgründen werden von Windows Grenzwerte für Software von Drittanbietern auf dem sicheren Desktop platziert. Wenn Sie möchten, dass Ihre Barrierefreiheits Anwendung auf dem sicheren Desktop ausgeführt wird, müssen Sie die Anwendung mit dem Easy Access Center registrieren.

## <a name="registering-with-the-ease-of-access-center"></a>Registrierung mit dem Easy Access Center

Barrierefreiheits Anwendungen registrieren sich mit dem Easy of Access Center, indem bei der Installation der Anwendung mindestens ein Registrierungsschlüssel erstellt wird. In der folgenden Tabelle sind die Informationen aufgeführt, die in den Registrierungs Schlüsseln enthalten sind.



| Name                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obligatorisch/Optional | Sprache      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Anwendungsname            | Der Name der Anwendung in einer Ressourcen Datei. Dieser Registrierungs Wert enthält eine Zeichenfolge in einem angegebenen Format. Dies könnte eine lokalisierte Version des Anwendungs namens sein, wenn die Anwendung in anderen Sprachen als Englisch lokalisiert wird. Der Name wird im Easy Access Center angezeigt.<br/>                                                                                                                                                                                                                                                                                       | Obligatorisch.          | Ertem     |
| ATEXE                       | Der Name der ausführbaren Datei der Anwendung oder des Images. Windows verwendet diesen Wert, um zu bestimmen, ob die Barrierefreiheits Anwendung ausgeführt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obligatorisch.          | Nicht lokalisiert |
| Copysettingstolockeddesktop | Ein **DWORD** -Wert, der angibt, ob die Einstellungen der Barrierefreiheits Anwendung auf den gesperrten Desktop kopiert werden sollen.<br/> Wenn dieser Wert 1 ist, kann die Anwendung Einstellungen in einen Speicherort in der Benutzerregistrierung schreiben, und Windows kopiert die Einstellungen an denselben Speicherort in der Benutzerregistrierung für den gesperrten Desktop. Dadurch kann die Anwendung ihren Zustand vom "normalen" Desktop auf den gesperrten Desktop persistent speichern.<br/>                                                                                                                                                             | Optional           | Nicht lokalisiert |
| BESCHREIBUNG                 | Eine kurze Beschreibung der Anwendung aus einer Ressourcen Datei. Dieser Registrierungs Wert enthält eine Zeichenfolge in einem angegebenen Format. Dies könnte eine lokalisierte Version der Beschreibung sein, wenn die Anwendung in anderen Sprachen als Englisch lokalisiert wird. Die Länge dieser Zeichenfolge muss weniger als 512 Zeichen umfassen.<br/> Die Beschreibung wird im Easy Access Center angezeigt, um dem Benutzer zusätzliche Informationen zur Barrierefreiheits Anwendung bereitzustellen.<br/> Dieser Wert kann auch verwendet werden, um den Benutzer darüber zu benachrichtigen, dass die Anwendung nicht auf dem sicheren Desktop verwendet wird.<br/>      | Obligatorisch.          | Ertem     |
| Profil                     | Ein kurzes XML-Element, das die von der Anwendung bereitgestellten Unterbringung angibt. Dadurch wird sichergestellt, dass die Anwendung im Easy of Access Center unter der richtigen Kategorie angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Obligatorisch.          | Nicht lokalisiert |
| Passiveautostartbehavior    | <p>Ein **DWORD** -Wert, der angibt, ob das automatische Startverhalten aktiviert ist.</p><p>Der Standardwert ist 0 (null). Dies bedeutet, dass ein-Wert ein älteres Automatisches Startverhalten erfordert. Dies bewirkt, dass die Einstellung "nach der Anmeldung starten" für diese Option in der Out-of-Box-Umgebung (OOBE) und in der Systemsteuerung aktiviert wird (siehe **Systemsteuerung-> Easy of Access-> Easy of Access Center-> Change Sign-in Settings**) und startet automatisch auf der UAC und dem Sperrbildschirm.</p><p>Der Wert 1 gibt an, dass der at das neue Auto Startverhalten verwenden soll, bei dem die Einstellung "nach der Anmeldung starten" für diese Option nicht im Feld "Out-of-Box-Umgebung" (OOBE) und in der Systemsteuerung aktiviert ist und der at-Vorgang automatisch einmal pro Benutzersitzung (bei der Anmeldung) gestartet wird.</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Optional          | Nicht lokalisiert |
| Securedesktopaccommodation  | Der Name einer alternativen Barrierefreiheits Anwendung, die auf dem sicheren Desktop anstelle dieser Anwendung ausgeführt werden soll. Die Alternative kann eine andere Anwendung, eine andere Version derselben Anwendung, eine der in Windows enthaltenen Barrierefreiheits Anwendungen oder "None" sein, wenn Sie keine Barrierefreiheits Anwendung auf dem sicheren Desktop ausführen möchten. <br/>                                                                                                                                                                                                               | Optional           | Nicht lokalisiert |
| Einfaches Profil              | Ein Wert, der beschreibt, wie die Anwendung in einem Wort oder zwei klassifiziert wird, z. b. Bildschirmleser, Bildschirmlupe oder Bildschirmtastatur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Obligatorisch.          | Nicht lokalisiert |
| StartExe                    | Der vollständige Pfad der ausführbaren Datei. Dieser Wert wird verwendet, um die Barrierefreiheits Anwendung zu starten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obligatorisch.          | Nicht lokalisiert |
| Startpara                 | Befehlszeilenargumenten Diese Werte werden zusammen mit startexe verwendet, um die Anwendung zu starten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Optional           | Nicht lokalisiert |
| Terminateondesktopswitch    | Ein **DWORD** -Wert, der angibt, wie die Barrierefreiheits Anwendung auf den Übergang zum oder vom sicheren Desktop antwortet.<br/> Wenn dieser Wert nicht vorhanden ist oder 1 ist, wird die Anwendung von Windows bei jedem Übergang zum oder vom sicheren Desktop beendet und neu gestartet. Dies ist das Standardverhalten.<br/> Wenn dieser Wert 0 ist, wird die Barrierefreiheits Anwendung bei einem Desktop Übergang von Windows nicht beendet. Die Anwendung wird weiterhin auf dem vorherigen Desktop ausgeführt, und Windows startet eine neue Instanz auf dem neuen Desktop, wenn eine Instanz nicht bereits ausgeführt wird.<br/> | Optional           | Nicht lokalisiert |


 

### <a name="localization"></a>Lokalisierung

Die Registrierungs Werte für den Anwendungsnamen und die Beschreibung müssen lokalisiert werden können, um die mehrsprachige Benutzeroberfläche (MUI) zu unterstützen.

Diese Zeichen folgen weisen das folgende Format auf, wobei Spitze Klammern erforderliche Elemente und eckige Klammern ein optionales Element angeben.

*@ <resdllpath \\ resdllfilename>,- <resID> \[ ;<comment>\]*

*<resdllpath \\ Resdllfilename>* ist der Pfad zur Ressourcen-DLL. Der Pfad kann Umgebungsvariablen enthalten.

*<resID>* die Ressourcen-ID für die Zeichenfolge.

der *\[ Kommentar \]* enthält optionale Kommentare.

Beispiel:


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



Weitere Informationen zu MUI finden Sie unter [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).

### <a name="hci-profile"></a>HCI-Profil

Mit dem HCI-Profil (Human Computer Interaktion) können Sie feststellen, welche Unterkünfte basierend auf den Anforderungen des Benutzers bereitgestellt werden. Barrierefreiheits Anwendungen sollten Informationen über die Art der Behinderung registrieren, die die Anwendung unterstützt.

Der Wert für die Profil Registrierung enthält XML-Code, der die Art der für die Barrierefreiheits Anwendung vorgesehenen Behinderung beschreibt. Dieser XML-Code weist das folgende Format auf:


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



Die gültigen Werte für das-Attribut des- **Lizenztyps** lauten wie folgt:

-   milde Vision
-   schwerwiegende Vision
-   milde Cognitive
-   Schwerwiegender Cognitive
-   milde Dexterität
-   schwerwiegende Dexterität
-   mildes hören
-   schwerwiegendes hören
-   milde Sprache
-   harte Sprache

> [!Note]  
> Bei diesen Werten wird zwischen Groß-/Kleinschreibung unterschieden.

 

Wenn eine Barrierefreiheits Anwendung mehrere-Unternehmen unterstützt, sollte der Wert für die Profil Registrierung für jede-Unterkunft ein **Attributtyp** Attribut enthalten.

### <a name="ease-of-access-registry-details"></a>Details zur einfachen Zugriffs Registrierung

Zum Registrieren Ihrer Barrierefreiheits Anwendung müssen Sie einen Schlüssel für Ihre Anwendung am folgenden Registrierungs Speicherort erstellen und mit Name-Wert-Paaren auffüllen.

**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\\\**

Benennen Sie den Registrierungsschlüssel Ihrer Anwendung im folgenden Format:

*"CompanyName \_ ProductName \_ v \# "*

Beispiel: "Configuration Manager \_ \_ v 2.0".

Zum Hinzufügen von Registrierungs Werten muss das Installationsprogramm mit erhöhten Rechten ausgeführt werden.

### <a name="secure-desktop-accommodation"></a>Sichere Desktop-Unterbringung

Mit dem Registrierungsschlüssel **securedesktopaccommodation** können Sie angeben, wie Ihre Barrierefreiheits Anwendung auf den sicheren Desktop antwortet. Standardmäßig wird Ihre Anwendung von der Easy Access Center-Anwendung auf dem sicheren Desktop gestartet, wenn Sie bereits auf dem normalen Desktop ausgeführt wurde, oder wenn Sie für die Ausführung auf dem Anmelde Desktop konfiguriert ist. Mit dem Schlüssel **securedesktopaccommodation** können Sie folgende Aktionen ausführen:

-   Geben Sie eine Alternative Version der Anwendung an, die auf dem sicheren Desktop verwendet werden soll. Beispielsweise können Sie über eine Alternative Version verfügen, die nicht gesicherte Features deaktiviert, oder Sie ist für die Verwendung von weniger Arbeitsspeicher und schnellere Starts optimiert.

    Zum Angeben der alternativen Version legen Sie den **securedesktopaccommodation** -Schlüssel auf den Namen der alternativen Version fest. Wenn Sie Ihre Anwendung z. b. auf dem Schlüssel für den Schlüssel von "TSO \_ Screen Reader \_ v 1.0" registriert haben, können Sie die Alternative Version auf dem \_ Bildschirm readersecure \_ v 1.0 registrieren. Legen Sie dann den **securedesktopaccommodation** -Schlüssel von "Configuration Manager" von "Configuration Manager" \_ \_ für "mso" auf "" \_ \_ .

-   Geben Sie eine Microsoft-Barrierefreiheits Anwendung an, die auf dem sicheren Desktop anstelle der Anwendung verwendet werden soll. Legen Sie für diese Option **securedesktopaccommodation** auf den Namen der bestimmten Microsoft-Eingabe Hilfen-Anwendung fest: "OSK", "Bildschirmlupe" oder "Sprachausgabe".
-   Geben Sie an, dass die Anwendung nicht auf dem sicheren Desktop ausgeführt werden soll und keine Alternative Anwendung. Legen Sie für diese Option **securedesktopaccommodation** auf "None" (empfohlen) oder den Namen einer nicht vorhandenen Anwendung fest.

Wenn der **securedesktopaccommodation** -Registrierungsschlüssel für Ihre Barrierefreiheits Anwendung eine Microsoft-Barrierefreiheits Anwendung angibt, die auf dem sicheren Desktop anstelle der Anwendung ausgeführt werden soll, wird der Benutzer von Windows benachrichtigt, wenn der Übergang zum sicheren Desktop erfolgt. Um den Benutzer zu benachrichtigen, zeigt Windows die Zeichenfolge an, die im Registrierungsschlüssel "Description" für Ihre Anwendung angegeben ist. Wenn z. b. die Anwendung Screenreader Deluxe 1,0 die Microsoft-Sprachausgabe auf dem sicheren Desktop verwendet, enthält Sie eine Beschreibungs Zeichenfolge, z. b. "Microsoft-Sprachausgabe wird in den gesperrten, Anmelde-und anderen sicheren Desktops anstelle von Screenreader Deluxe 1,0 verwendet."

Wenn der **securedesktopaccommodation** -Schlüssel Ihrer Anwendung auf "None" festgelegt ist, verwenden Sie den **Beschreibungs** Schlüssel, um dem Benutzer mitzuteilen, dass Ihre Anwendung auf dem sicheren Desktop nicht verfügbar ist und keine Alternative bereitgestellt wird.

Windows zeigt den Beschreibungstext an den entsprechenden Speicherorten im Easy of Access Center an.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>Ausführung bei der Installation und auf dem Anmelde Desktop

Wenn Sie den registrierten Schlüsselnamen ihrer Barrierefreiheits Anwendung an die Zeichenfolge am folgenden Registrierungs Speicherort anfügen, wird die Anwendung sofort nach der Installation von Windows gestartet. Außerdem wird die Anwendung automatisch von Windows ausgeführt, wenn der Anmelde Desktop aktiv ist.

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion ( \\ Barrierefreiheits \\ Konfiguration)**

Der Konfigurationsschlüssel ist eine durch Trennzeichen getrennte Zeichenfolge. Um Ihre Anwendung hinzuzufügen, fügen Sie eine Zeichenfolge an, die dem Registrierungsschlüssel Ihrer Anwendung unter HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\ ATS entspricht \\ .

### <a name="running-in-a-job"></a>Ausführen in einem Auftrag

Wenn der Registrierungsschlüssel **terminateondesktopswitch** nicht vorhanden ist oder auf einen Wert ungleich 0 (null) festgelegt ist, führt Windows die Anwendung im Kontext eines Auftrags aus und beendet die Anwendung mit jedem Desktop Übergang und startet Sie neu. Wenn Sie in einem Auftrag ausführen, wird sichergestellt, dass nur eine einzelne Instanz der Anwendung zu einem bestimmten Zeitpunkt ausgeführt wird, und die Anwendung muss den Desktop Status nicht überwachen. Zu den Nachteilen der Ausführung von in einem Auftrag gehören:

-   Die Anwendung verursacht einen Startkosten bei jedem Desktop Übergang.
-   Die Anwendung kann nur über das Easy of Access Center gestartet werden.
-   Die Anwendung muss Ihre Einstellungen ständig speichern, da Sie jederzeit durch einen Desktop Übergang beendet werden kann.

Wenn der **terminateondesktopswitch** -Schlüssel vorhanden und auf 0 festgelegt ist, führt Windows die Barrierefreiheits Anwendung nicht in einem Auftrag aus. Dies bietet die folgenden Vorteile:

-   Den Desktop Übergängen sind keine Startkosten zugeordnet.
-   Die Anwendung kann außerhalb der Easy of Access Center gestartet werden.

Zu den Nachteilen, die nicht in einem Auftrag ausgeführt werden, gehören:

-   Da die Anwendung auf Desktop Übergängen nicht neu gestartet wurde, muss Sie erkennen, wenn der aktuelle Desktop inaktiv ist und entsprechend antwortet. Beispielsweise muss die Anwendung die Steuerung der Hardware aufgeben, damit Sie von der sicheren Desktop Version der Anwendung verwendet werden kann, und die Anwendung sollte in den Energiesparmodus wechseln, um die Verwendung von Prozessorressourcen zu vermeiden.
-   Wenn die Anwendung über das Startmenü, den Windows-Explorer oder die Befehlszeile gestartet werden kann, muss das Easy Access Center informiert werden. Weitere Informationen finden Sie unter **Windows-Logo-Taste + U**.
-   Da mehrere Kopien der Anwendung gleichzeitig auf unterschiedlichen Desktops ausgeführt werden können, muss die Anwendung so geschrieben werden, dass mehrere laufende Kopien unterstützt werden.

### <a name="windows-logo-key--u"></a>Windows-Taste + U

Wenn Ihre Barrierefreiheits Anwendung so konfiguriert ist, dass Sie in einem Auftrag ausgeführt wird, sollte der Startcode Ihrer Anwendung einen Aufrufen der [**isprocessinjob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) -Funktion enthalten, um zu bestimmen, ob die Anwendung in einem Auftrag gestartet wird. Wenn dies der Fall ist, sollte die Anwendung das Easy of Access Center starten und dann beenden. Im folgenden Beispiel wird gezeigt, wie **isprocessinjob** aufgerufen wird.


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Wenn die Barrierefreiheits Anwendung so konfiguriert ist, dass Sie außerhalb eines Auftrags ausgeführt wird, sollte Sie die Erleichterung des Zugriffs Centers Benachrichtigen, dass die Anwendung gestartet wird und wie üblich fortgesetzt wird.

Unabhängig davon, wie die Anwendung konfiguriert ist, muss die Anwendung, wenn Sie eine Möglichkeit zum Beenden innerhalb der Anwendung bietet (z. b. eine Schaltfläche zum Schließen), die Benutzerfreundlichkeit des Zugriffs Centers Benachrichtigen, dass Sie beendet wird.

Eine Anwendung benachrichtigt das Easy of Access Center durch Festlegen eines temporären Registrierungsschlüssels und Einfügen der Tastenkombination Windows-Taste + U in den Eingabestream.

Die Anwendung sollte den temporären Schlüssel an folgendem Speicherort erstellen.

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibilitytemp**

Der temporäre Schlüssel muss den gleichen Namen wie der registrierte Anwendungsname aufweisen, z. b. "kontoso \_ Screen Reader \_ v 1.0". Der Wert des Schlüssels ist ein **DWORD** -Wert, der beim Starten auf 0x0003 erfordert festgelegt ist, oder 0x0002, wenn die Anwendung beendet wird.


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



### <a name="windows-logo-key--volume-up"></a>Windows-Taste + Lautstärke

Wenn der Benutzer die Barrierefreiheits Anwendung durch Drücken der Tastenkombination Windows-Taste + aufgerundet (z. b. auf einem Tablet-Gerät) startet, übergibt das Easy of Access Center das folgende Befehlszeilenargument an die Anwendung:

**/hardwarebuttonlaunch**

Die Anwendung kann dieses Argument verwenden, um zu bestimmen, ob normal gestartet werden soll, oder um das Verhalten entsprechend anzupassen.

### <a name="transferring-secure-desktop-settings"></a>Übertragen sicherer Desktop Einstellungen

Wenn Ihre Barrierefreiheits Anwendung den sicheren Desktop unterstützt, können Sie die-Registrierung verwenden, um Einstellungen zu kopieren, wenn die Anwendung auf den sicheren Desktop übergeht. Durch das Kopieren von Einstellungen wird der Übergang zum sicheren Desktop für den Benutzer nahtlos.

Legen Sie zum Kopieren von Einstellungen den Registrierungsschlüssel copysettingstolockeddesktop der Anwendung auf 1 fest, und speichern Sie die Einstellungen im folgenden Registrierungs Speicherort.

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\ atconfig\\<AT Key Name>**

Das Easy Access Center überwacht diesen Registrierungs Speicherort, während die Anwendung ausgeführt wird. Wenn eine Umstellung auf den sicheren Desktop stattfindet, werden die Einstellungen durch das Easy Access Center an denselben Speicherort in der HKCU-Hive-Struktur des sicheren Desktops kopiert. Die Anwendung kann dann die Einstellungen lesen und ihren Status fortsetzen.

Ihre Barrierefreiheits Anwendung sollte Ihre Einstellungen in regelmäßigen Abständen oder immer dann schreiben, wenn sich die Werte ändern. Das Schreiben von Einstellungen beim Beenden der Anwendung funktioniert nicht. Wenn die Anwendung in einem Auftrag ausgeführt wird, wird Sie bei der Umstellung vom sicheren Desktop beendet, bevor der Exitcode ausgeführt werden kann. Wenn die Anwendung nicht in einem Auftrag ausgeführt wird, wird die Anwendung bei der Umstellung vom sicheren Desktop nicht beendet.

### <a name="caution"></a>Achtung

Da die hier beschriebenen Registrierungsschlüssel im Benutzermodus geschrieben werden, sind Sie nicht sicher. Wenn Ihre Barrierefreiheits Anwendung den Inhalt dieser Schlüssel liest, sollte die Daten sorgfältig überprüft und mit Bedacht verwendet werden. Insbesondere sollte Ihre Anwendung eine Überprüfung auf **DWORD** -Werte durchführen, bei Zeichen folgen Längen Vorsicht walten lassen, keine Plug-in-DLL-Namen lesen und keine Befehle ausführen, die in Zeichen folgen gefunden werden.

## <a name="registry-examples"></a>Registrierungs Beispiele

Das folgende Beispiel zeigt die möglichen Registrierungs Werte für ein fiktives Produkt mit dem Namen "CSO Screenreader Version 2,0", dessen lokalisierter Name als Ressource gespeichert wird.

Die Werte in der Tabelle liegen unter folgendem Schlüssel:

**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\ ist \\ Conin so \_ Screen Reader \_ v 2.0**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>@% Systemroot% \system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>BESCHREIBUNG</td>
<td>REG_SZ</td>
<td>@% Systemroot% \system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Simpleprofile</td>
<td>REG_SZ</td>
<td>Screenreader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>Startpara</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>Securedesktopaccommodation</td>
<td>REG_SZ</td>
<td>Narrator</td>
</tr>
</tbody>
</table>



 

Wenn die Anwendung eine Sprachausgabe und eine Bildschirmlupe in einer einzelnen ausführbaren Datei bereitstellt, können die Werte für die Bildschirm Lese Komponente wie folgt aussehen:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>BESCHREIBUNG</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-32</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Simpleprofile</td>
<td>REG_SZ</td>
<td>Screenreader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\ProgrammeFiles\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>Startpara</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

Die Werte für die Bildschirm Vergrößerungs Komponente befinden sich im folgenden Schlüssel:

**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ condesoibility \\ ATS \\ Conto so \_ Lupe \_ v 2.0**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>BESCHREIBUNG</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-42</td>
</tr>
<tr class="odd">
<td>Profil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Simpleprofile</td>
<td>REG_SZ</td>
<td>Vergrößern</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>c:\ProgrammeFiles\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>Startpara</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

