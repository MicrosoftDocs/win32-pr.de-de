---
title: Bewährte Sicherheitsmethoden bei der Spieleentwicklung
description: In diesem Artikel werden bewährte Methoden für die Entwicklung von spielen erläutert.
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba4f02d5e1a2e3da2e50feedd89f085a0c063be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858343"
---
# <a name="best-security-practices-in-game-development"></a>Bewährte Sicherheitsmethoden bei der Spieleentwicklung

In diesem Artikel werden bewährte Methoden für die Entwicklung von spielen erläutert.

-   [Introduction (Einführung)](#introduction)
-   [Beispiele für unsicheren Code](#examples-of-insecure-code)
-   [Möglichkeiten zur Verbesserung der Sicherheit](#ways-to-improve-security)
-   [Zusammenfassung](#summary)

## <a name="introduction"></a>Einführung

Eine wachsende Anzahl von Menschen spielen Online Spiele und Spiele mit Benutzer gemachten Inhalten. Dies bedeutet in Kombination mit der wachsenden Sicherheit des Microsoft Windows-Betriebssystems, dass Spiele ein wachsendes und verlockendes Ziel für Angriffe sind. Spieleentwickler sollten einen starken Schwerpunkt darauf haben, sicherzustellen, dass die Spiele, die Sie veröffentlichen, keine neuen Sicherheitslücken erstellen, die von Angreifern ausgenutzt werden können. Spieleentwickler sind in der Verantwortung, und Sie sind dafür verantwortlich, zu verhindern, dass die Computer Ihrer Kunden von bösartigen Netzwerkdaten, Benutzer Änderungen oder Manipulationen gehackt werden. Wenn eine Schwachstelle ausgenutzt wird, könnte dies dazu führen, dass Kunden und/oder Geld verloren gehen. In diesem Artikel werden einige gängige Methoden und Tools erläutert und erläutert, um die Code Sicherheit zu erhöhen, ohne die Entwicklungszeit zu erhöhen.

Die drei häufigsten Fehler, die ein Entwicklungsteam beim Freigeben eines Produkts hat, sind:

-   Erfordert Administratorrechte. Spiele sollten keine Administratorrechte erfordern. Weitere Informationen finden Sie unter [Benutzerkontensteuerung für Spieleentwickler](./user-account-control-for-game-developers.md).
-   Der automatisierte Schutz wird nicht verwendet. Entwickler verwenden in der Regel nicht **/GS**, **/SAFESEH** oder **/NX**. Die Verwendung dieser Kompilierungs-/LINKFLAGS kann viele grundlegende Sicherheitslücken erkennen oder eliminieren, ohne die Arbeitsauslastung erheblich zu erhöhen. Diese Flags werden weiter unten in diesem Artikel erläutert.
-   Verwenden von unzulässigen APIs. Es gibt viele APIs ("**straupie**", " **straupie**" usw.), die für Programmierer fehleranfällig sind und problemlos Sicherheitslücken erzeugen können. Entwickler sollten diese APIs durch die sicheren Versionen ersetzen. Visual Studio 2005 enthält ein Tool zum Analysieren von Binärdateien, die Objektdateien automatisch auf Verweise auf unsichere APIs überprüfen können. Weitere Informationen zu den Informationen, die mit diesem Tool generiert werden, finden Sie unter [mit den Visual Studio 2005-sicheren C-und C++-Bibliotheken](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) von Martyn Lovell. Außerdem können Sie die gesperrte [. h](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) -Header Datei erhalten, mit der Sie verbotene Funktionen aus dem Code entfernen können.

Jeder der aufgelisteten Fehler ist nicht nur üblich, sondern kann problemlos korrigiert werden, ohne dass sich die Entwicklungs-, Codierungs-oder Funktionsanforderungen erheblich ändern.

## <a name="examples-of-insecure-code"></a>Beispiele für unsicheren Code

Im folgenden finden Sie ein einfaches Beispiel dafür, wie ein Angreifer einen Pufferüberlauf Angriff ausführen kann:


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



Auf der Oberfläche sieht dieser Code OK aus – er ruft schließlich eine sichere Funktion auf. Daten aus dem Netzwerk werden in einen Puffer mit einer Größe von 256 Bytes kopiert. Die Funktion " **strinncpy** " basiert darauf, dass in der Quell Zeichenfolge ein NULL-Terminator gefunden wird oder durch die angegebene Puffer Anzahl beschränkt wird. Das Problem ist, dass die Puffergröße falsch ist. Wenn Daten aus dem Netzwerk nicht überprüft werden oder die Puffergröße falsch ist (wie in diesem Beispiel), könnte ein Angreifer einfach einen großen Puffer bereitstellen, um Stapel Daten nach dem Ende des Puffers mit allen Daten im Netzwerk Paket zu überschreiben. Dadurch kann der Angreifer beliebigen Code ausführen, indem der Anweisungs Zeiger überschrieben und die Rückgabeadresse geändert wird. Die grundlegendste Lektion dieses Beispiels besteht darin, die Eingaben niemals zu vertrauen, bis Sie überprüft wurden.

Auch wenn Daten nicht anfänglich aus dem Netzwerk stammen, besteht weiterhin ein potenzielles Risiko. Die Entwicklung moderner Spiele erfordert viele Personen, die dieselbe Codebasis entwerfen, entwickeln und testen. Es gibt keine Möglichkeit, zu erfahren, wie die-Funktion in Zukunft aufgerufen wird. Fragen Sie sich immer, woher die Daten stammen und was ein Angreifer kontrollieren könnte? Netzwerkbasierte Angriffe sind die gängigsten, Sie sind jedoch nicht die einzigen Methoden zum Erstellen von Sicherheitslücken. Könnte ein Angreifer einen mod erstellen oder eine gespeicherte Datei so bearbeiten, dass eine Sicherheitslücke geöffnet wird? Wie sieht es mit den benutzerdefinierten Bild-und Audiodateien aus? Böswillige Versionen dieser Dateien können im Internet gepostet werden und gefährliche Sicherheitsrisiken für Ihre Kunden verursachen.

Um das Beispiel zu korrigieren, verwenden Sie als Seite "Straub. h" oder "Safe CRT" anstelle von " **trencpy** ". Safe CRT ist eine umfassende Sicherheitsüberprüfung der C-Laufzeit und ist Bestandteil von Visual Studio 2005. Weitere Informationen zu Safe CRT finden Sie unter [Sicherheitserweiterungen in der CRT](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) von Michael Howard.

## <a name="ways-to-improve-security"></a>Möglichkeiten zur Verbesserung der Sicherheit

Es gibt mehrere Möglichkeiten, die Sicherheit im Entwicklungszeitraum zu verbessern. Hier sind einige der besten Möglichkeiten:

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>Informationen zur Sicherheit
</dt> <dd>

Das Buch " *Schreiben von sicherem Code, Second Edition* von Michael Howard und David LeBlanc" bietet eine ausführliche Erläuterung der Strategien und Methoden zum Verhindern von Angriffen und mindern von Exploits. Beginnend mit den Methoden zum Entwerfen der Sicherheit in eine Version für Techniken zum Sichern von Netzwerkanwendungen behandelt das Buch alle Aspekte, die ein Spielentwickler benötigt, um sich selbst, seine Produkte und seine Kunden vor Angreifern zu schützen. Das Buch kann verwendet werden, um eine Kultur der Sicherheit in einem Development Studio zu erhalten. Denken Sie nicht nur an die Code Sicherheit, sondern auch an das Problem eines Entwicklers. Denken Sie an die Sicherheit, die das gesamte Team – vom Programmmanager zum Designer an Entwickler und Tester – berücksichtigen sollte, wenn Sie an einem Projekt arbeiten. Umso größer ist die Wahrscheinlichkeit, dass eine Sicherheitslücke vor der Freigabe abgefangen wird.

Das *Schreiben von sicherem Code, Second Edition,* finden Sie unter [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) . allgemeinere Sicherheitsinformationen finden Sie unter [ausschalten zukünftiger Angriffe durch Verringern der Angriffsfläche](/previous-versions/ms972812(v=msdn.10)) von Michael Howard.

Michael Howard, David LeBlanc und John Viega haben ein weiteres Buch zu dem Thema verfasst, das alle gängigen Betriebssysteme und Programmiersprachen mit dem Titel *19 tödliche Sünden der Software Sicherheit* behandelt.

Sicherheits Präsentationen, die auf Spiele fokussiert sind, finden Sie auf der Downloadseite für [Microsoft XNA Developer-Präsentationen](/previous-versions/dn629515(v=msdn.10)) .

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>Analyse der Bedrohungsmodellierung
</dt> <dd>

Eine Bedrohungs Modellierungs Analyse ist eine gute Möglichkeit, die Systemsicherheit zu bewerten, nicht in einer bestimmten Sprache oder mithilfe eines Tools, sondern in einer umfassenden End-to-End-Methode, die in einigen wenigen Besprechungen ausgeführt werden kann. Wenn ein Thread Modell ordnungsgemäß implementiert ist, kann es alle stärken und Schwächen eines Systems identifizieren, ohne dem Projekt eine beträchtliche Arbeitsauslastung oder Besprechungszeit hinzuzufügen. Die Methode der Bedrohungsmodellierung hebt auch die Vorstellung der Bewertung der Systemsicherheit vor und während des Entwicklungsprozesses hervor, um sicherzustellen, dass eine umfassende Bewertung durchgeführt wird, während Sie sich auf die riskantesten Features konzentriert. Dies kann als Profiler für die Sicherheit betrachtet werden. Wenn Sie nicht auf einer bestimmten Sprache basieren oder sich auf ein bestimmtes Tool verlassen, kann die Bedrohungsmodellierung in jeder Entwicklungsstudio verwendet werden, die an einem beliebigen Projekt in beliebigen Genres arbeitet. Die Bedrohungsmodellierung ist auch eine hervorragende Methode, um die Idee zu verstärken, dass die Sicherheit von allen Benutzern und nicht von einem anderen Problem gelöst wird.

Beachten Sie bei der Bedrohungsmodellierung besonders Folgendes:

-   UDP-Datenquellen
-   Datenquellen, für die keine Authentifizierung erforderlich ist
-   Datenquellen, die im Rahmen der allgemeinen Informationserfassung häufig und normal geprüft werden
-   Alle Möglichkeiten eines Clients, Daten direkt an andere Clients zu senden

Dies sind die Bereiche, die ein gutes Potenzial für Sicherheitslücken aufweisen.

Weitere Informationen zur Bedrohungsmodellierung finden Sie unter [Bedrohungsmodellierung](https://technet.microsoft.com/security/) im MSDN Security Development Center und in The Book [Threat Modeling](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) by Frank Swiderski and Window Snyder.

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>Verhinderung von Datenausführung (/NX)
</dt> <dd>

Ein aktuelles Tool zum verringern mehrerer Exploits ist die Daten Ausführungs Verhinderung (Data Execution Prevention, DEP). Wenn Sie den Switch **/NX** in den Build-Befehl einschließen, markiert Visual Studio Speicherseiten mit Flags, die angeben, ob der Code über die Berechtigung zum Ausführen verfügt. Alle Programme, die versuchen, auf einer Arbeitsspeicher Seite auszuführen, die nicht mit der EXECUTE-Berechtigung gekennzeichnet ist, führen zu einer Zwangs Beendigung des Programms. Die Verhinderung wird auf Prozessor Ebene erzwungen und wirkt sich auf Entwickler aus, die selbst veränderlichen Code oder systemeigene JIT-sprach Compiler verwenden. Zurzeit unterstützen nur die Athlon64-und Opteron-Prozessoren von AMD und der Itanium-Prozessor von Intel und die neuesten Pentium 4-Prozessoren die Ausführungs Verhinderung. es wird jedoch erwartet, dass alle 32-Bit-und 64-Bit-Prozessoren in Zukunft die Ausführungs Verhinderung unterstützen. (Ein von einem Entwickler verwendetes Schema zum Kopieren von Schutzmaßnahmen ist möglicherweise von der Ausführungs Verhinderung betroffen, aber Microsoft hat mit Kopierschutz Anbietern gearbeitet, um die Auswirkungen zu minimieren.) Es empfiehlt sich, DEP zu verwenden.

Weitere Informationen zu DEP finden Sie unter [Daten Ausführungs Verhinderung](../memory/data-execution-prevention.md).

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>Puffer Sicherheitsüberprüfung (/GS) und Image verfügt über sichere Ausnahmehandler (/SAFESEH)
</dt> <dd>

Die *Puffer Sicherheitsüberprüfung*, die durch das Compilerflag " **/GS**" angegeben wird, und das *Image verfügt über sichere Ausnahmehandler*, die durch das Linker-Flag angegeben werden **/SAFESEH** (zuerst in Visual Studio .NET 2003 implementiert), kann die Aufgabe des Entwicklers, den Code zu schützen, etwas leichter machen.

Die Verwendung des **/GS** -Flags bewirkt, dass der Compiler eine Prüfung für einige Formen von Stapel basierten Pufferüberläufen erstellt, die ausgenutzt werden können, um die Rückgabeadresse einer Funktion zu überschreiben. Durch die Verwendung von **/GS** wird nicht jeder potenzielle Pufferüberlauf erkannt, sondern sollte nicht als Catch-All angesehen werden, sondern als eine gute Verteidigungstechnologie.

Die Verwendung des **/SAFESEH** -Flags weist den Linker an, nur eine ausführbare Datei oder dll zu generieren, wenn Sie auch eine Tabelle mit den sicheren Ausnahme Handlern der ausführbaren Datei oder dll generieren kann. Die sichere strukturierte Ausnahmebehandlung (SAFESEH) beseitigt die Ausnahmebehandlung als Ziel von Pufferüberlauf Angriffen, indem sichergestellt wird, dass vor dem Senden einer Ausnahme der Ausnahmehandler in der Funktions Tabelle in der Bilddatei registriert wird. Diese Schutz Vorteile werden mit Windows XP SP2, Windows Server 2003, Windows Vista und Windows 7 ermöglicht. Damit **/SAFESEH** ordnungsgemäß funktioniert, muss es auch in einer All-or-Nothing-Methode verwendet werden. Alle Bibliotheken, die an eine ausführbare Datei oder dll gebundene Code enthalten, müssen mit **/SAFESEH** kompiliert werden, oder die Tabelle wird nicht generiert.

Weitere Informationen zur [Puffer Sicherheitsüberprüfung](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) (**/GS**) und zum [Image sind sichere Ausnahmehandler](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) (**/SAFESEH**) finden Sie in MSDN.

Siehe auch Informationen über das [ **/SDL** -Flag](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019) von Microsoft Visual Studio 2012 und die Erweiterungen von Visual Studio 2012 [für das **/GS** -Flag](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/).

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

PREfast ist ein kostenloses Tool von Microsoft, mit dem Ausführungs Pfade in kompiliertem C oder C++ analysiert werden, um Laufzeitfehler zu finden. Vorfast funktioniert, indem alle Ausführungs Pfade in allen Funktionen durchlaufen und die einzelnen Pfade auf Probleme bewertet werden. Dieses Tool wurde ursprünglich zum Entwickeln von Treibern und anderem Kernel Code verwendet und kann Spiel Entwicklern dabei helfen, Zeit zu sparen, indem einige Fehler vermieden werden, die schwer zu finden sind oder vom Compiler ignoriert werden. Die Verwendung von PREfast ist eine hervorragende Möglichkeit, die Arbeitsauslastung zu reduzieren und die Anstrengungen des Entwicklungsteams und des Testteams zu konzentrieren. PREfast ist in Visual Studio Team Suite und Visual Studio Team Edition for Software Developers als Code Analyse verfügbar, die vom Compilerschalter **/analyze** aktiviert wird. (Diese Option ist auch in der kostenlosen Version des Compilers verfügbar, die im Lieferumfang des Windows Software Development Kit enthalten ist.)

> [!Note]  
> Visual Studio 2012 unterstützt **/analyze** in allen Editionen. Weitere Informationen zur Verfügbarkeit der Code Analyse in allen Editionen von Visual Studio finden Sie unter [Neues in der Code Analyse](/archive/blogs/codeanalysis/?m=20123).

 

Durch die Verwendung von Header Anmerkungen (insbesondere bei Puffer Zeiger Argumenten) kann PREfast zusätzliche Probleme, z. b. Speicher Überschreibungs Fehler, eine häufige Quelle von Abstürzen und potenzielle Sicherheitsrisiken, bereitstellen. Dies erfolgt mithilfe der Standard-Annotation Language (SAL), bei der es sich um eine Form der Markierung für C/C++-Funktionsprototypen handelt, die zusätzliche Informationen zur erwarteten Semantik von Zeiger Argumenten und zur Korrelation mit Längen Parametern, deklarierten Puffergrößen usw. bereitstellen. Alle Header für Windows-Betriebssysteme werden kommentiert, und das Hinzufügen von Sal-Kennzeichen in öffentlichen API-Headern in ihren eigenen Bibliotheken ermöglicht die Ausführung ausführlicherer und aggressiver Prüfungen in Ihrem Client Code für solche APIs. Eine Einführung in Sal und Links zu weiteren Informationen finden Sie im Blogeintrag von Michael Howard, "[A Short Introduction to the Standard Annotation Language (SAL)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)".

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>Windows-Application Verifier
</dt> <dd>

Der Windows-Application Verifier oder AppVerifier kann den Testern helfen, indem er mehrere Funktionen in einem Tool bereitstellt. Der AppVerifier ist ein Tool, das entwickelt wurde, um allgemeine Programmierfehler zu testen. AppVerifier kann die an API-Aufrufe übergebenen Parameter überprüfen, falsche Eingaben einfügen, um die Fehler behandlungsfähigkeit zu überprüfen und Änderungen an der Registrierung und im Dateisystem zu protokollieren. AppVerifier kann auch Pufferüberläufe im Heap erkennen, überprüfen, ob eine Access Control Liste (ACL) ordnungsgemäß definiert wurde, und erzwingt die sichere Verwendung von Socket-APIs. Obwohl es nicht vollständig ist, kann AppVerifier ein Tool in der Toolbox der Tester sein, damit ein Entwicklungsstudio ein qualitativ hochwertiges Produkt veröffentlichen kann.

Weitere Informationen zu Application Verifier finden Sie unter [Application Verifier](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) und [Verwenden von Application Verifier in Ihrem Lebenszyklus der Software Entwicklung](/previous-versions/aa480483(v=msdn.10)) auf MSDN.

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>Testen von Fuzz
</dt> <dd>

*Fuzz-Tests* sind eine halbautomatisierte Testmethode, mit der die aktuellen Testmethoden verbessert werden können. Die zentrale Idee hinter dem Testen von zufälligen Daten besteht darin, eine vollständige Bewertung aller Eingaben durchführen zu lassen, indem zufällige Daten erfasst werden, um herauszufinden, was unterbrochen wird. Dies schließt alle Netzwerkdaten, Moden und gespeicherte Spiele usw. ein. Das Testen von Fuzz ist recht einfach. Ändern Sie einfach wohlgeformte Dateien oder Netzwerkdaten, indem Sie zufällige Bytes einfügen, angrenzende Bytes kippen oder numerische Werte neften. 0xFF, 0xFFFF, 0xFFFFFFFF, 0x00, 0x0000, 0x00000000 und 0x80000000 sind Werte, die für das verfügbar machen von Sicherheitslücken beim Testen von zufälligen Daten geeignet sind. Sie können die resultierenden Interaktions Kombinationen mithilfe von AppVerifier beobachten. Obwohl das fuzzingverfahren nicht vollständig ist, ist es einfach zu implementieren und zu automatisieren, und es kann die komplizierteren und unvorhersehbaren Fehler abfangen.

Weitere Informationen zum Testen von zufälligen Daten finden Sie in der [Gamefest 2007](/previous-versions/dn629515(v=msdn.10)) -Präsentation *praktische Schritte in Game Security*.

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Authenticode-Signierung
</dt> <dd>

Authenticode ist eine Methode, um sicherzustellen, dass ausführbare Dateien, DLL-Dateien und Windows Installer-Pakete (MSI-Dateien), die der Benutzer empfängt, nicht geändert werden, was ein Entwickler veröffentlicht hat. Durch die Verwendung einer Kombination aus kryptografieprinzipien, vertrauenswürdigen Entitäten und Industriestandards überprüft Authenticode die Integrität der ausführbaren Inhalte. Microsoft stellt eine kryptografische API (CryptoAPI) zur Verfügung, die zum automatischen Erkennen von Manipulationen von signiertem Code verwendet werden kann. Wenn nach einer Freigabe ein Sicherheitsfehler auftritt, kann ein Zertifikat widerrufen werden, und der gesamte mit diesem Zertifikat signierte Code wird nicht mehr authentifiziert. Durch das Aufheben eines Zertifikats wird die Überprüfung aller mit diesem Zertifikat signierten Titel aufgehoben. Windows wurde für die Verwendung mit Authenticode-Signierung entwickelt und warnt einen Benutzer über nicht signierten Code in bestimmten Situationen, die den PC eines Benutzers für Angriffe verfügbar machen könnten.

Authenticode sollte nicht als Methode zur Vermeidung von Sicherheitsproblemen angesehen werden, sondern eine Methode zum Erkennen von Manipulationen, nachdem eine ausführbare Datei freigegeben wurde. Eine ausführbare Datei oder dll, die ein ausnutzbares Sicherheitsproblem enthält, kann mit Authenticode signiert und überprüft werden. das Sicherheitsproblem wird jedoch weiterhin im neuen System eingeführt. Erst nachdem ein Produkt oder ein Update als sicher überprüft wurde, sollte der Code signiert werden, um Benutzern zu gewährleisten, dass Sie über ein Release verfügen, das noch nicht manipuliert wurde.

Selbst wenn ein Entwickler der Meinung ist, dass es keine Gefahr gibt, dass seine Releases geändert werden, basieren andere Technologien und Dienste auf Authenticode. Die Code Signierung ist einfach zu integrieren und zu automatisieren. Es gibt keinen Grund dafür, dass Entwickler ihre Releases nicht signiert haben.

Weitere Informationen zur Authenticode-Signierung finden Sie unter [Authenticode-Signierung für Spieleentwickler](./authenticode-signing-for-game-developers.md).

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>Minimieren von Berechtigungen
</dt> <dd>

In allgemeinen sollten Prozesse mit dem minimalen Satz von Berechtigungen ausgeführt werden, die für den Betrieb erforderlich sind. Unter Windows Vista und Windows 7 wird dies mithilfe der [Benutzerkontensteuerung](./user-account-control-for-game-developers.md)erreicht, sodass das Spiel als Standard Benutzer und nicht als Administrator ausgeführt werden kann. Bei Windows XP werden Spiele üblicherweise immer als Administrator ausgeführt. Auch unter Windows Vista und Windows 7 ist es manchmal erforderlich, für bestimmte Vorgänge auf vollständige Administratorrechte zu erhöhen.

In Fällen, in denen der Prozess mit vollständigen Administratorrechten ausgeführt wird, sind in der Regel nur wenige Rechte erforderlich, die über die eines Standard Benutzers hinausgehen. Der Administrator Zugriff umfasst viele Rechte, die nicht von legitimer Code benötigt werden, aber von einem Angreifer durch eine gewisse Schwäche des Prozesses verwendet werden können. Beispiele für solche Rechte sind z. b. "Take Take Ownership", "SE Debug", "SE Create Token", "SE", "SE", "SE Security", "SE Load Driver", "SE SYSTEMTIME", "SE Backup", "SE \_ Restore" \_ \_ \_ , " \_ \_ \_ \_ \_ \_ \_ \_ \_ SE Shutdown" und " \_ SE \_ Audit [](../secauthz/privilege-constants.md)"

Obwohl ein Prozess nach dem Start keine weiteren Rechte mehr erhält, kann er problemlos Rechte erhalten. Beim Start kann der Prozess sofort Win32-APIs verwenden, um Rechte zu entfernen, die nicht erforderlich sind.

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>Verwenden von Windows-Sicherheits Features
</dt> <dd>

Windows Vista und Windows 7 enthalten eine Reihe neuer Features, die die Code Sicherheit verbessern. Die [Benutzerkontensteuerung](./user-account-control-for-game-developers.md) ist sicherlich das wichtigste, das Sie verstehen und berücksichtigen können, aber es gibt auch noch weitere Features. Zusätzlich zu den Windows XP SP2-Technologien wie Windows-Firewall, Daten Ausführungs Verhinderung, Puffer Sicherheitsüberprüfung und sicheren Ausnahme Handlern, die auch unter Windows Vista und Windows 7 verfügbar sind, gibt es drei neuere Sicherheitsfeatures, die berücksichtigt werden müssen:

-   Das Feature für die zufällige Funktion des Adressraum Layouts. Dies wird durch Verknüpfung mit der Option **/DynamicBase** in Visual Studio 2005 Service Pack 1 oder Visual Studio 2008 ermöglicht. Dies bewirkt, dass das System die Positionen von vielen der Schlüsselsystem-DLLs im Prozessbereich angleicht, sodass es schwieriger ist, ausnutzbare Angriffs Programme zu schreiben, die weitgehend über das Internet verteilt werden. Dieses Linker-Flag wird von Windows XP und älteren Versionen von Windows ignoriert.
-   Heap Beschädigungen können zu einer vollständigen Klasse von Sicherheits Exploits führen, sodass das Speichersystem von Windows Vista und Windows 7 nun einen Modus unterstützt, der den Prozess beendet, wenn eine Heap Beschädigung erkannt wird. Durch das Aufrufen von [**HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation) mit **heapenabletermivorgänger oncorruption** wird dieses Verhalten übernommen. Dieser Rückruf schlägt unter Windows XP und einer älteren Version von Windows fehl.
-   Beim Schreiben von Diensten können Sie mithilfe einer neuen Funktion konfiguriert werden, um anzugeben, welche Privilegien tatsächlich erforderlich sind, und um den Ressourcen Zugriff auf eine bestimmte sid einzuschränken. Dies erfolgt über [ChangeSeviceConfig2](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a), mithilfe der Dienst \_ Konfiguration \_ erforderliche \_ Berechtigungen \_ Informationen und Dienst \_ Konfigurations \_ Dienst- \_ sid- \_ Informationen.

</dd> </dl>

## <a name="summary"></a>Zusammenfassung

Die Entwicklung eines Spiels für den aktuellen und den zukünftigen Marketplace ist kostspielig und zeitaufwändig. Das Freigeben eines Spiels mit Sicherheitsproblemen kostet letztendlich mehr Geld und Zeit, um ordnungsgemäß zu beheben. Daher ist es in den Interessen aller Spielentwickler, Tools und Techniken zu integrieren, um Sicherheits Exploits vor der Veröffentlichung zu entschärfen.

Die Informationen in diesem Artikel sind nur eine Einführung in die Möglichkeiten von Entwicklungsstudio, um sich selbst und ihre Kunden zu unterstützen. Weitere Informationen zu allgemeinen Sicherheitsmethoden und Sicherheitsinformationen finden Sie im [Microsoft Security Developer Center](https://technet.microsoft.com/security/).

 

 