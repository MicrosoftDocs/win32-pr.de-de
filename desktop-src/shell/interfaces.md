---
description: In diesem Abschnitt werden die Windows-Shellschnittstellen beschrieben.
title: 'Shellschnittstellen '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 05223970-14f5-44c2-937b-07826b8aecf9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 23bd87e86ba9e30ce443616920326bf37aba6d2c
ms.sourcegitcommit: 9a614d8ce23dcca88873148683d9ec7d38be57b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2020
ms.locfileid: "104391279"
---
# <a name="shell-interfaces"></a>Shellschnittstellen 

In diesem Abschnitt werden die Windows-Shellschnittstellen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>Iaccessibleobject</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die von einer Barrierefreiheits Anwendung verwendet werden kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>Iaccessibilitydockingservice</strong></a><br/></td>
<td>Dockt ein einzelnes Barrierefreiheits-App-Fenster am unteren Rand eines Bildschirms an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>Iaccessibilitydockingservicecallback</strong></a><br/></td>
<td>Informiert eine Barrierefreiheits-App darüber, dass Ihr Fenster nicht angedockt ist.<br/></td>
</tr>
<tr class="even">
<td><a href="iaclcustommru.md"><strong>Iaclcustommru</strong></a><br/></td>
<td>Macht Methoden verfügbar, die zum Initialisieren einer zuletzt verwendeten (MRU-) Liste für ein Objekt für die automatische Vervollständigung verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>Iaclist</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die Effizienz der automatischen <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>Vervollständigung</strong></a> verbessert, wenn die Kandidaten Zeichenfolgen in einer Hierarchie organisiert sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>iaclist</strong></a> -Schnittstelle, damit Clients eines Auto Vervollständigen-Objekts Optionsflags abrufen und festlegen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>Iaktionprogress</strong></a><br/></td>
<td>Stellt die abstrakte Basisklasse dar, von der Fortschritt gesteuerte Vorgänge erben können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>Iaktionprogressdialog</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein Status Dialogfeld initialisieren und beenden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>Iapplicationactivationmanager</strong></a><br/></td>
<td>Stellt Methoden bereit, die Windows Store-Apps für die Start-, Datei-und Protokoll <a href="/previous-versions/windows/apps/hh464906(v=win.10)">Erweiterungen</a>aktivieren. Diese Schnittstelle wird normalerweise in Debuggern und Entwurfs Tools verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>Iapplicationassociationregistration</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Standardanwendungen für bestimmte Datei Zuordnungs <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>Typen</strong></a>und Protokolle auf einer bestimmten Zuordnungs <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>Ebene</strong></a>abgefragt und festgelegt werden. <br/>
<blockquote>
[!Note]<br />
Ab Windows 8 ist die einzige Funktion, die für diese Schnittstelle unterstützt wird, " <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>querycurrentdefault</strong></a>".
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>Iapplicationassociationregistrationui</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die ein Dialogfeld für die erweiterte Zuordnung öffnet, über das der Benutzer seine Zuordnungen anpassen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>Iapplicationdesignmodesettings</strong></a><br/></td>
<td>Ermöglicht Entwicklungs Tool Anwendungen das dynamische spoup von System-und Benutzer Zuständen, wie z. b. systemeigene Anzeige Auflösung, Skalierungsfaktor für Geräte und Anwendungs Ansichts Zustand, zum Testen von Windows Store-Apps, die im Entwurfs Modus ausgeführt werden, für eine Vielzahl von Formfaktoren, ohne dass die tatsächliche Hardware benötigt wird. Ermöglicht außerdem das Testen von Änderungen im normalerweise vom Benutzer kontrollierten Zustand, um Windows Store-Apps in einer Vielzahl von Szenarien zu testen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a><br/></td>
<td>Ermöglicht Entwicklungs Tool Anwendungen das dynamische Steuern von System-und Benutzer Zuständen, wie z. b. systemeigene Anzeige Auflösung, Skalierungsfaktor für Geräte und das Layout von Anwendungs Sichten, die an Windows Store-Apps gemeldet werden, um Windows Store-Apps, die im Entwurfs Modus ausgeführt werden, für eine Vielzahl von Formfaktoren zu testen, ohne die tatsächliche Hardware zu benötigen. Ermöglicht außerdem das Testen von Änderungen im normalerweise vom Benutzer kontrollierten Zustand, um Windows Store-Apps in einer Vielzahl von Szenarien zu testen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>Iapplicationdestination</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es einer Anwendung ermöglichen, ein oder alle Ziele aus den <strong>aktuellen</strong> oder <strong>häufigen</strong> Kategorien in einer Sprung Liste zu entfernen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>Iapplicationdocumentlists</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung den Inhalt der <strong>aktuellen</strong> oder <strong>häufigen</strong> Kategorien in einer Sprung Liste abrufen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>Iapppublisher</strong></a><br/></td>
<td>Macht Methoden zum Veröffentlichen von Anwendungen über die Option "Software <strong>" in der</strong> Systemsteuerung verfügbar. Dies ist die grundlegende Schnittstelle, die für diesen Zweck implementiert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>Iappvisibility</strong></a><br/></td>
<td>Stellt Funktionen bereit, um zu bestimmen, ob in der Anzeige Windows Store-Apps angezeigt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>Iappvisibilityevents</strong></a><br/></td>
<td>Ermöglicht Anwendungen das Empfangen von Benachrichtigungen über Zustandsänderungen in einer Anzeige und von Änderungen in der Sichtbarkeit des Start Bildschirms.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>Iassochandler</strong></a><br/></td>
<td>Macht Methoden für Vorgänge mit einem Dialogfeld oder einem Menü für die Datei Zuordnung verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>Iassochandlerinvoker</strong></a><br/></td>
<td>Macht Methoden verfügbar, die einen zugeordneten Anwendungs Handler aufrufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a><br/></td>
<td>Macht Methoden verfügbar, die mit Client Anwendungen verwendet werden können, um eine Benutzerumgebung bereitzustellen, die das sichere herunterladen und Austauschen von Dateien durch e-Mail-und Messaging Anlagen ermöglicht<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>Iautocomplete</strong></a><br/></td>
<td>Verfügbar gemacht durch das Auto Vervollständigen-Objekt (CLSID_AutoComplete). Diese Schnittstelle ermöglicht es Anwendungen, das-Objekt zu initialisieren, zu aktivieren und zu deaktivieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a><br/></td>
<td>Erweitert <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>iautocomplete</strong></a>. Diese Schnittstelle ermöglicht Clients des Auto Vervollständigen-Objekts das Abrufen und Festlegen einer Reihe von Optionen, die die Funktionsweise der automatischen Vervollständigung steuern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>Iautocompletedropdown</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es Clients ermöglichen, den Anzeige Zustand der Auto Vervollständigen-Dropdown Liste zurückzusetzen oder abzufragen, die mögliche Vervollständigungen für eine Zeichenfolge enthält, die der Benutzer in einem Bearbeitungs Steuerelement eingegeben hat.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>Ibandhost</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Bänder erstellt und zerstört und deren Verfügbarkeit spezifiinterpretiert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>Ibandsite</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Band Objekte steuern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>Ibrowserframeoptions</strong></a><br/></td>
<td>Ermöglicht einem Browser oder Host, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a> zu Fragen, welche Art von Ansichts Verhalten unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>Ikategorizer</strong></a><br/></td>
<td>Macht Methoden verfügbar, die zum Abrufen von Informationen über elementbezeichnerlisten verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>Icategoryprovider</strong></a><br/></td>
<td>Macht eine Liste von kategorierern verfügbar, die bei einem <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>registriert sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>Icdburn</strong></a><br/></td>
<td>Macht Methoden verfügbar, die bestimmen, ob ein System über Hardware zum Schreiben auf CD, den Laufwerk Buchstaben eines CD Writer-Geräts und eine programmgesteuerte Einleitung einer CD-Schreib Sitzung verfügt. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>Icolumnmanager</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Überprüfung und Bearbeitung von Spalten in der Detailansicht von Windows-Explorer aktivieren. Auf jede Spalte wird durch eine <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> -Struktur verwiesen, die eine Eigenschaft benennt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>Icommdlgbrowser</strong></a><br/></td>
<td>Wird von den Dialogfeldern für die gemeinsame Datei verfügbar gemacht, die beim Hosten eines shellbrowsers verwendet werden. Wenn dies unterstützt wird, macht <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>icommdlgbrowser</strong></a> Methoden verfügbar, mit denen eine shellansicht verschiedene Fälle behandeln kann, die in einem Dialogfeld ein anderes Verhalten erfordern als in einer normalen shellansicht. Sie erhalten einen <strong>icommdlgbrowser</strong> -Schnittstellen Zeiger, indem Sie <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> für das <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>ishellbrowser</strong></a> -Objekt aufrufen. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a><br/></td>
<td>Erweitert die Funktionen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>icommdlgbrowser</strong></a>. Diese Schnittstelle wird von den Dialogfeldern für die gemeinsame Datei angezeigt, wenn Sie einen ShellBrowser hosten. Ein Zeiger auf <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a> kann durch Aufrufen von <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> für das <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>ishellbrowser</strong></a> -Objekt abgerufen werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a><br/></td>
<td>Erweitert die Funktionen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>und wird beim Hosten eines shellbrowsers von den Dialogfeldern für die gemeinsame Datei verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>Icomputerinfochangenotify</strong></a><br/></td>
<td>Diese Schnittstelle ist möglicherweise in späteren Versionen von Windows nicht vorhanden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>Iconnectablekredentialprovidercredential</strong></a><br/></td>
<td>Macht Methoden zum Verbinden und trennen von <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>iconnectablekredentialprovidercredential</strong></a> -Objekten verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>Icontactmanagerinterop</strong></a><br/></td>
<td>Ermöglicht den Zugriff auf <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> -Methoden in einer APP, die mehrere Fenster verwaltet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein einem Shellobjekt zugeordnetes Kontextmenü erstellen oder zusammenführen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein Kontextmenü (Kontextmenü) erstellen oder zusammenführen, das einem Shellobjekt zugeordnet ist. Erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> durch Hinzufügen einer Methode, die es Client Objekten ermöglicht, Nachrichten zu verarbeiten, die mit vom Besitzer gezeichneten Menü Elementen verknüpft sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>IContextMenu3</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein einem Shellobjekt zugeordnetes Kontextmenü erstellen oder zusammenführen. Ermöglicht Client Objekten das Verarbeiten von Nachrichten, die mit vom Besitzer gezeichneten Menü Elementen verknüpft sind, und erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a> durch akzeptieren eines Rückgabewerts aus der Nachrichtenverarbeitung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>Icontextmenucb</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die den Rückruf eines Kontextmenüs ermöglicht. Beispielsweise, um einem <strong>MenuItem</strong> , das eine Erhöhung erfordert, ein Schild Symbol hinzuzufügen.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>Icontrolmarkup</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>Icopyhook</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen <em>kopierhook-Handler</em>erstellt. Ein Kopier-Hook-Handler ist eine Shellerweiterung, mit der bestimmt wird, ob ein Shellordner oder ein Drucker Objekt verschoben, kopiert, umbenannt oder gelöscht werden kann. Die Shell Ruft die <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>icopyhook:: copycallback</strong></a> -Methode vor dem Ausführen eines dieser Vorgänge auf.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>Ikreateobject</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die ein Objekt einer angegebenen Klasse erstellt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>Ikreatingprocess</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> verwendet, damit der Aufrufer einige Parameter des Prozesses ändern kann, der erstellt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>Ikreateprocessinputs</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ikreatingprocess</strong></a> -Schnittstelle verwendet, um einige Parameter des Prozesses zu ändern, der erstellt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>Ikredentialprovider</strong></a><br/></td>
<td>Macht Methoden verfügbar, die beim Setup und bei der Bearbeitung eines Anmelde Informationsanbieters verwendet werden. Alle Anmelde Informationsanbieter müssen diese Schnittstelle implementieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Behandlung von Anmelde Informationen ermöglichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ikredentialprovidercredential</strong></a> -Schnittstelle durch Hinzufügen einer Methode, die die Sicherheits-ID (SID) eines Benutzers abruft. Die Anmelde Informationen sind diesem Benutzer zugeordnet und können unter der Kachel des Benutzers gruppiert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a><br/></td>
<td>Stellt einen asynchronen Rückrufmechanismus bereit, der von Anmelde Informationen verwendet wird, um Sie über Status-oder Text Änderungs Ereignisse in der Anmelde Benutzeroberfläche oder der Benutzeroberfläche für Anmelde Informationen zu benachrichtigen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ikredentialproviderfordentialevents</strong></a> -Schnittstelle durch Hinzufügen von Methoden, die das Batch-Aktualisieren von Feldern auf der Benutzeroberfläche der Benutzeroberfläche oder Anmelde Informationen ermöglichen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>Ikredentialproviderkredentialwithfieldoptions</strong></a><br/></td>
<td>Stellt eine Methode bereit, die es dem Anmelde Informationsanbieter-Framework ermöglicht, zu bestimmen, ob Sie die Option eines Felds in einer Anmelde-oder Anmelde Benutzeroberfläche angepasst haben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a><br/></td>
<td>Stellt einen asynchronen Rückrufmechanismus bereit, der von einem Anmelde Informationsanbieter verwendet wird, um ihn über Änderungen in der Liste der Anmelde Informationen oder ihrer Felder zu benachrichtigen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>Ikredentialproviderfilter</strong></a><br/></td>
<td>Wird verwendet, um Anmelde Informationsanbieter anhand der zur Laufzeit verfügbaren Informationen dynamisch zu filtern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>Ikredentialprovidersetuserarray</strong></a><br/></td>
<td>Stellt eine Methode bereit, mit der ein Anmelde Informationsanbieter die Gruppe von Benutzern empfangen kann, die auf der Anmelde Benutzeroberfläche für Anmelde Informationen oder Anmelde Informationen angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>Ikredentialprovideruser</strong></a><br/></td>
<td>Stellt Methoden bereit, mit denen bestimmte Eigenschaften eines einzelnen Benutzers abgerufen werden, der in einer Anmelde-oder Anmelde Benutzeroberfläche enthalten ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>Ikredentialprovideruserarray</strong></a><br/></td>
<td>Stellt die Gruppe von Benutzern dar, die in der Benutzeroberfläche für Anmelde-oder Anmelde Informationen angezeigt werden. Diese Informationen ermöglichen dem Anmelde Informationsanbieter das Auflisten des Satzes zum Abrufen von Eigenschafts Informationen zu den einzelnen Benutzern, um Felder aufzufüllen oder den Satz zu filtern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>Ihapptitem</strong></a><br/></td>
<td>Wird durch Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> für ein Element abgerufen. Wenn das Element eine Momentaufnahme eines Elements zu einem früheren Zeitpunkt darstellt, wird diese Schnittstelle die aktuelle Version des Elements abrufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>Icurrentworkingdirectory</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es einem Client ermöglichen, das aktuelle Arbeitsverzeichnis eines Objekts abzurufen oder festzulegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung eine benutzerdefinierte Sprung Liste, einschließlich der Ziele und Aufgaben, für die Anzeige auf der Taskleiste bereitstellen kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>Idataobjectasynccapability</strong></a><br/></td>
<td>Aktiviert Schnittstellen, die in der Regel synchron sind, um asynchron zu funktionieren. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist die aktuelle, umbenannte Version von <a href="/previous-versions//bb776309(v=vs.85)"><strong>iasyncoperation</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>Idataobjectprovider</strong></a><br/></td>
<td>Stellt Methoden bereit, die es Ihnen ermöglichen, die <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject-Schnittstelle</strong></a>eines <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">DataPackage</a> -Objekts festzulegen oder abzurufen, das das DataPackage verwendet, um die Interoperabilität zu unterstützen. Das DataPackage-Objekt wird von einer App verwendet, um Daten für eine andere APP bereitzustellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>Idatatransfermanagerinterop</strong></a><br/></td>
<td>Ermöglicht den Zugriff auf <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>datatransfermanager</strong></a> -Methoden in einer Windows Store-App, die mehrere Fenster verwaltet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>Idefaultextracticonfiguration</strong></a><br/></td>
<td>Macht Methoden zum Festlegen von Standardsymbolen verfügbar, die einem Objekt zugeordnet sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>Idefehlerfoldermenuinitialize</strong></a><br/></td>
<td>Stellt Methoden bereit, mit denen Kontextmenü Informationen angezeigt und festgelegt werden. Diese Informationen sind identisch mit denen, die für " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>shkreatedefaultcontextmenu</strong></a> " über die <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>defcontextmenu</strong></a> -Struktur bereitgestellt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>Idelayedpropertystorefactory</strong></a><br/></td>
<td>Macht eine Methode verfügbar, mit der ein angegebenes <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Objekt erstellt werden kann, wenn der Eigenschaften Zugriff potenziell langsam ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>Idelegatefolder</strong></a><br/></td>
<td>Macht eine Methode verfügbar, über die einem delegatordner die <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> -Schnittstelle zugewiesen wird, die zum Zuordnen und Freigeben von Element-IDs erforderlich ist<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>Idelegateitem</strong></a><br/></td>
<td>Dient zum Abrufen der unmittelbar zugrunde liegenden Darstellung eines Element Pfads.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>Idesktopgadget</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die das programmgesteuerte Hinzufügen eines installierten Gadgets zum Desktop des Benutzers ermöglicht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>Idesktopwallpaper</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>Idestinationstreamfactory</strong></a><br/></td>
<td>Macht eine Methode zum manuellen Kopieren eines Streams oder einer Datei verfügbar, bevor Änderungen auf Eigenschaften angewendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>Idisplayitem</strong></a><br/></td>
<td>Macht Methoden verfügbar, die eine Version des aktuellen Elements suchen, das zum Abrufen von Anzeigeeigenschaften verwendet werden soll, z. b. der Elementname, die auf der Benutzeroberfläche angezeigt werden. Wird von den Dialogfeldern der Kopier-Engine verwendet, um der Benutzeroberfläche ein entsprechendes anzuzeigende Element bereitzustellen. Wenn keine andere Version gefunden werden kann, wird das aktuelle Element verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>Idockingwindow</strong></a><br/></td>
<td>Macht Methoden verfügbar, die das Andock Fenster Objekt von Änderungen benachrichtigen, einschließlich Anzeige, ausblenden und bevorstehender Entfernung. Diese Schnittstelle wird von Fenster Objekten implementiert, die innerhalb des Rahmen Raums eines Windows-Explorer-Fensters angedockt werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>Idockingwindowframe</strong></a><br/></td>
<td>Macht Methoden verfügbar, die das Hinzufügen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>idockingwindow</strong></a> -Objekten zu einem Frame unterstützen. Wird vom Browser implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>Idockingwindowsite</strong></a><br/></td>
<td>Macht Methoden verfügbar, die den Rahmen Bereich für ein oder mehrere <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>idockingwindow</strong></a> -Objekte verwalten. Diese Schnittstelle wird vom Browser implementiert und ähnelt der <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>iolumplaceuiwindow</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>Idragsourcehelper</strong></a><br/></td>
<td>Wird von der Shell bereitgestellt, damit eine Anwendung das Bild angeben kann, das während eines shelldrag & Drop-Vorgangs angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>idragsourcehelper</strong></a>Funktionalität hinzufügt. Diese Methode legt die Eigenschaften eines Drag & Drop-Vorgangs auf ein <strong>idragsourcehelper</strong> -Objekt fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>Idroptargethelper</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Ablage Ziele ein Drag-Bild anzeigen können, während sich das Bild über dem Zielfenster befindet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>Idynamichwhandler</strong></a><br/></td>
<td>Wird von "AutoPlay" aufgerufen. Macht Methoden verfügbar, die dynamische Informationen bezüglich eines registrierten Handlers erhalten, bevor er für den Benutzer angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>Ienumassochandlers</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die Enumeration einer Auflistung von Handlern ermöglicht, die bestimmten Dateinamen Erweiterungen zugeordnet sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>Ienumerableview</strong></a><br/></td>
<td>Macht Methoden verfügbar, die den Inhalt einer Ansicht aufzählen und nach dem Abschluss der Enumeration vom Rückruf benachrichtigt werden. Mit dieser Schnittstelle können Clients einer Ansicht versuchen, die Liste der Ordnerinhalte der Ansicht freizugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>Ieinumexplorercommand</strong></a><br/></td>
<td>Wird von einem <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>bereitgestellt. Diese Schnittstelle enthält die Enumeration von Befehlen, die in der Befehlsleiste abgelegt werden sollen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>Iumumextrasearch</strong></a><br/></td>
<td>Ein Standard-OLE-Enumerator, der von einem Client verwendet wird, um die verfügbaren Such Objekte für einen Ordner zu bestimmen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>Ienumfullidlist</strong></a><br/></td>
<td>Macht einen Standardsatz von Methoden verfügbar, die die Zeiger auf elementbezeichnerlisten (pidls) der Elemente in einem Shellordner auflisten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>Ienumittellist</strong></a><br/></td>
<td>Macht einen Standardsatz von Methoden verfügbar, mit denen die pidls der Elemente in einem Shellordner aufgelistet werden. Wenn die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: enujubjects</strong></a> -Methode eines Ordners aufgerufen wird, erstellt Sie ein Enumerationsobjekt und übergibt einen Zeiger an die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>ienumittellist</strong></a> -Schnittstelle des Objekts zurück an die aufrufende Anwendung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>Iumumubjects</strong></a><br/></td>
<td>Macht Methoden zum Aufzählen unbekannter Objekte verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>Ienumpublishedapps</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen veröffentlichte Anwendungen zum Hinzufügen/Entfernen von Programmen in der Systemsteuerung aufgelistet werden. Das Objekt, das diese Schnittstelle verfügbar macht, wird über <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>iapppublisher:: enumapps</strong></a>angefordert. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>Ienumlesrückruf</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen die Ansicht den Implementierer benachrichtigen kann, wenn die Enumeration abgeschlossen ist. Die Ansicht ruft diese Methode auf, um dem Implementierer mitzuteilen, dass die Enumeration über <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>ienumerableview:: kreateenumerumittellistfromcontent</strong></a>abgerufen werden kann. Der-Rückruf ermöglicht dem Implementierer das Freigeben der views-Enumeration.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>Ienumresources</strong></a><br/></td>
<td>Macht ressourcenenumerationsmethoden verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>Ienumshellitems</strong></a><br/></td>
<td>Macht die Enumeration von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Schnittstellen verfügbar. Diese Schnittstelle wird in der Regel durch Aufrufen der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>ienumshellitems</strong></a> -Methode abgerufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>Ienumsyncmgrconflict</strong></a><br/></td>
<td>Machtkonflikt Enumerationsmethoden verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>Ienumsyncmgrevents</strong></a><br/></td>
<td>Macht Enumerationsmethoden für Synchronisierungs Ereignisse verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>Ienumsyncmgrsyncitems</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen die vom-Handler verwalteten Synchronisierungs Element Objekte aufgelistet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>Iexecutecommand</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen ein angegebener Zustand oder Parameter, der mit dem Befehls Verb verknüpft ist, sowie eine Methode zum Aufrufen dieses Verbs festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>Iexecutecommandapplicationhostenvironment</strong></a><br/></td>
<td>Stellt eine einzelne Methode bereit, die es einer Anwendung ermöglicht, zu bestimmen, ob sich der Host im Desktop-oder im immersiven Modus befindet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>Iexecutecommandhost</strong></a><br/></td>
<td>Stellt eine Methode bereit, die einem <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>-basierten shellverb Handler ermöglicht, den Benutzeroberflächen Modus der Host Komponente abzufragen, von der aus die Anwendung aufgerufen wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> ist ein Browser Objekt, das entweder navigiert werden kann oder das eine Ansicht eines Datenobjekts hosten kann. Als Browser Objekt mit vollem Funktionsumfang wird auch ein automatisches Reiseprotokoll unterstützt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>Iexplorerbrowserevents</strong></a><br/></td>
<td>Macht Methoden für Benachrichtigungen über Browser Navigation und Ansichts Erstellungs Ereignisse von Explorer verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Befehls Darstellung erhalten, Unterbefehle aufzählen oder den Befehl aufrufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a><br/></td>
<td>Macht Methoden zum Erstellen von Explorer-Befehlen und Befehls Enumeratoren verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>Iexplorercommandstate</strong></a><br/></td>
<td>Macht eine einzelne Methode verfügbar, die den Abruf des Befehls Zustands ermöglicht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>Iexplorerpanevisibility</strong></a><br/></td>
<td>Wird in Windows-Explorer durch eine <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> -Implementierung verwendet, um Vorschläge für die Sichtbarkeit der Bereiche anzuzeigen. Außerdem kann ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> -Host diese Schnittstelle verwenden, um Informationen über die Sichtbarkeit des Bereichs bereitzustellen. Der Host muss <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> mit <strong>SID_ExplorerPaneVisibility</strong> als Dienst-ID implementieren. Der Host muss sich in der Standort Kette befinden. <br/> Die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>iexplorerpanevisibility</strong></a> -Implementierung wird aus dem Shellordner abgerufen. Der Shellordner wird wiederum aus der Ansicht abgerufen. Eine Namespace Erweiterung kann sich für die Bereitstellung einer benutzerdefinierten Ansicht (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a>) entscheiden, anstatt das Systemordner View-Objekt (defview) zu verwenden. In diesem Fall muss die <strong>ishellview</strong> -Implementierung eine Implementierung von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>ifolderview:: GetFolder</strong></a> enthalten, um das <strong>iexplorerpanevisibility</strong> -Objekt zurückzugeben.<br/> Eine Namespace Erweiterung kann eine benutzerdefinierte Ansicht bereitstellen, indem Sie <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a> selbst implementiert, anstatt das Systemordner View-Objekt (defview) zu verwenden. In diesem Fall muss die <strong>ishellview</strong> -Implementierung eine Implementierung von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>ifolderview:: GetFolder</strong></a> enthalten, damit <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>iexplorerpanevisibility</strong></a> verwendet werden kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>Iextracticon</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es einem Client ermöglichen, das Symbol abzurufen, das einem der-Objekte in einem Ordner zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>Iextractimage</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein Miniaturbild aus einem Shellordner anfordern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a><br/></td>
<td>Erweitert die Funktionen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>iextractimage</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>Ifiledialog</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Ergebnisse im allgemeinen Datei Dialogfeld initialisiert, angezeigt und angezeigt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>ifiledialog</strong></a> -Schnittstelle durch Bereitstellen von Methoden, die es dem Aufrufer ermöglichen, einen bestimmten, eingeschränkten Speicherort zu benennen, der im allgemeinen Datei Dialogfeld durchsucht werden kann, und alternativen Text anzugeben, der als Bezeichnung auf der Schaltfläche <strong>Abbrechen</strong> angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>Ifiledialogcontrolevents</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung über Ereignisse im Zusammenhang mit Steuerelementen benachrichtigt werden kann, die von der Anwendung zu einem gemeinsamen Datei Dialogfeld hinzugefügt wurden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung einem allgemeinen Datei Dialogfeld Steuerelemente hinzufügen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Benachrichtigungen über Ereignisse innerhalb eines allgemeinen Datei Dialogfelds zugelassen werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>Ifleisinuse</strong></a><br/></td>
<td>Macht Methoden verfügbar, die aufgerufen werden können, um Informationen zu erhalten oder eine Datei zu schließen, die von einer anderen Anwendung verwendet wird. Wenn eine Anwendung versucht, auf eine Datei zuzugreifen, und diese Datei bereits verwendet wird, kann Sie die Methoden dieser Schnittstelle verwenden, um Informationen zu erfassen, die dem Benutzer in einem Dialogfeld angezeigt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>ifiledialog</strong></a> -Schnittstelle durch Hinzufügen spezifischer Methoden zum Dialogfeld "Öffnen".<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a><br/></td>
<td>Macht Methoden zum Kopieren, verschieben, umbenennen, erstellen und Löschen von shellelementen sowie Methoden zum Bereitstellen von Fortschritts-und Fehler Dialogfeldern verfügbar. Diese Schnittstelle ersetzt die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> -Funktion.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein umfassendes Benachrichtigungssystem bereitstellen, das von Aufrufern von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> verwendet wird, um die Details der Vorgänge zu überwachen, die durch diese Schnittstelle<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>ifiledialog</strong></a> -Schnittstelle durch Hinzufügen spezifischer Methoden zum Dialogfeld "Speichern", die diejenigen enthalten, die Unterstützung für die Auflistung von Metadaten bereitstellen, die in der Datei beibehalten werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>Ifilesyncmergehandler</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>Ifilesystembinddata</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Dateisystem Informationen zum Optimieren von IShellFolder-aufrufen gespeichert werden <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>::P artardisplayname</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a><br/></td>
<td>Erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>ifilesystembinddata</strong></a>, das Dateisystem Informationen zum Optimieren von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder-aufrufen speichert::P arsetdisplayname</strong></a>. Diese Schnittstelle fügt die erstellbarkeits Gruppe oder die Get-Datei-ID oder die Verbindungs Klassen-ID (CLSID) hinzu<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/schema-library-iconreference"><strong>Ifileviewer</strong></a><br/></td>
<td>Macht Methoden verfügbar, die eine Schnittstelle angeben, mit der ein registrierter Datei-Viewer benachrichtigt werden kann, wenn eine Datei angezeigt oder gedruckt werden muss.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>Ifileviewersite</strong></a><br/></td>
<td>Macht Methoden verfügbar, die eine Schnittstelle angeben, die einem Datei-Viewer das Abrufen des Handles für das aktuelle angeheftete Fenster oder das Festlegen eines neuen angehefteten Fensters ermöglicht. Das angeheftete Fenster ist das Fenster, in dem der aktuelle Datei-Viewer eine Datei anzeigt. Wenn der Benutzer eine neue Datei zum anzeigen auswählt, weist die Shell den Datei-Viewer an, die neue Datei im angehefteten Fenster anzuzeigen, anstatt ein neues Fenster zu erstellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>Ifolderfilter</strong></a><br/></td>
<td>Wird von einem Client verfügbar gemacht, um anzugeben, wie die Enumeration eines shellordners von einer Serveranwendung gefiltert werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>Ifolderfiltersite</strong></a><br/></td>
<td>Wird von einem Host exportiert, damit Clients festlegen können, wie eine shellordnerenumeration gefiltert werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>Ifolderview</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen zu den Anzeigeoptionen eines Ordners abrufen, bestimmte Elemente in diesem Ordner auswählen und den Ansichtsmodus des Ordners festlegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen zu den Anzeigeoptionen eines Ordners abrufen, bestimmte Elemente in diesem Ordner auswählen und den Ansichtsmodus des Ordners festlegen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>Ifolderviewhost</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>ifolderview</strong></a> -Objekt in einem Fenster hostet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>Ifolderviewoptions</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Steuerung der Optionen für die Ordneransicht für die Ansichten Windows 7 und höher ermöglichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>Ifolderviewsettings</strong></a><br/></td>
<td>Macht Methoden zum Abrufen der Ordner Ansichts Einstellungen verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>Iframeworkinputpane</strong></a><br/></td>
<td>Stellt Methoden bereit, mit denen Apps über Zustandsänderungen und den Speicherort für den Eingabebereich informiert werden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>Iframeworkinputpanehandler</strong></a><br/></td>
<td>Ermöglicht das Benachrichtigen einer APP, wenn der Eingabebereich (Tastatur oder Handschrift Bereich) angezeigt oder ausgeblendet wird. Dadurch kann das App-Fenster seine Anzeige anpassen, sodass keine Eingabe Bereiche (z. b. ein Textfeld) durch den Eingabebereich verdeckt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>Ihandleractivationhost</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>Ihandlerinfo</strong></a><br/></td>
<td>Stellt Methoden bereit, die Informationen über den Handler für Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>ihandleractivationhost</strong></a> -Schnittstelle bereitstellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>Ihomegroup</strong></a><br/></td>
<td>Macht Methoden verfügbar, die den Status der Heim Netzgruppen Mitgliedschaft eines Computers bestimmen und den Freigabe-Assistenten anzeigen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>Ihweventhandler</strong></a><br/></td>
<td>Wird von der automatischen Wiedergabe aufgerufen, um die Verarbeitung registrierter Medientypen zu implementieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>ihweventhandler</strong></a> -Schnittstelle so, dass die Benutzerkontensteuerung (User Account Control, UAC) für Geräte Handler adressiert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>Iidentityname</strong></a><br/></td>
<td>Macht Methoden zum Vergleichen von zwei Elementen verfügbar, um zu sehen, ob Sie identisch sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>Iimagerecompress</strong></a><br/></td>
<td>Macht eine Methode verfügbar, mit der Bilder erneut komprimiert werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>Iinitializecommand</strong></a><br/></td>
<td>Macht eine einzelne Methode verfügbar, die zum Initialisieren von Objekten verwendet wird, die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>iexplorercommandstate</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>iexecutecommand</strong></a> oder <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> mit dem von der Anwendung angegebenen Befehlsnamen und den zugehörigen registrierten Eigenschaften implementieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>"Iinitializenetworkfolder"</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die CLSID_NetworkPlaces der Netzwerkdaten Quelle initialisiert, wie angegeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>Iinitializewithbindctx</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen Handler initialisiert, z. b. einen Eigenschafts Handler, einen Miniatur Ansichts Handler oder einen Vorschau Handler mit einem Bindungs Kontext.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a><br/></td>
<td>Macht eine Methode verfügbar, um einen Handler zu initialisieren, z. b. einen Eigenschafts Handler, einen Miniatur Ansichts Handler oder einen Vorschau Handler mit einem Dateipfad.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die zum Initialisieren eines Handlers verwendet wird, z. b. einen Eigenschafts Handler, einen Miniatur Ansichts Handler oder einen Vorschau Handler mit einem <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>Iinitializewithpropertystore</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen Handler, z. b. einen Eigenschafts Handler, einen Miniatur Ansichts Handler oder einen Vorschau Handler, mit einem Eigenschaften Speicher initialisiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen Handler, z. b. einen Eigenschafts Handler, einen Miniatur Ansichts Handler oder einen Vorschau Handler, mit einem Stream initialisiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>Iinitializewithwindow</strong></a><br/></td>
<td>Macht eine Methode verfügbar, über die ein Client einem Windows-Runtime Objekt, das in einer Desktop Anwendung verwendet wird, ein Besitzer Fenster bereitstellen kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>Iinputobject</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die UI-Aktivierung und-Prozessbeschleunigung für ein Benutzereingabe Objekt ändern, das in der Shell enthalten ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>iinputobject</strong></a> durch die Handhabung von globalen Accelerators erweitert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>Iinputobjectsite</strong></a><br/></td>
<td>Macht eine Methode verfügbar, mit der Fokus Änderungen für ein in der Shell enthaltenes Benutzereingabe Objekt kommuniziert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>Iinputpanelconfiguration</strong></a><br/></td>
<td>Stellt Funktionen für Desktop-Apps bereit, um den in Windows Store-Apps verwendeten Fokus Verfolgungs Mechanismus zu abonnieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>Iinputpanelinvocationconfiguration</strong></a><br/></td>
<td>Hiermit können Windows Store-Apps das automatische Aufruf Verhalten ablehnen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>Iiocancelinformation</strong></a><br/></td>
<td>Macht Methoden zum Bereitstellen einer Abbruch Fenster Meldung an den Prozess Thread im Status Dialogfeld verfügbar. <br/> Diese Schnittstelle ermöglicht es dem Status Dialogfeld, eine Thread Nachricht über <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> an den Arbeits Thread zu senden, um die Vorgänge abzubrechen. Der Arbeits Thread muss die Nachrichten Warteschlange in regelmäßigen Abständen über <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>, per <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>Peer Message</strong></a> oder <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>überprüfen.<br/> Die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>iiocancelinformation:: setcancelinformation</strong></a> -Methode teilt dem Fortschritts Dialogfeld mit, welche Thread-ID und welche Nachricht <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> angezeigt wird, wenn der Benutzer auf <strong>Abbrechen</strong>klickt. Die Thread-ID &quot; NULL &quot; deaktiviert den Sendevorgang für die Cancel-Nachricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>Iitemnamelimits</strong></a><br/></td>
<td>Ruft eine Liste gültiger und ungültiger Zeichen oder die maximale Länge eines Namens im-Namespace ab. Verwenden Sie diese Schnittstelle zum Überprüfen von Validierung und Übersetzung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>Iknownfolder</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung Informationen über die Kategorie, den Typ, die GUID, den PIDL-Wert, die Umleitungs Funktionen und die Definition eines bekannten Ordners abrufen kann. Sie stellt eine Methode für das Abrufen des <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekts eines bekannten Ordners bereit. Außerdem werden Methoden bereitstellt, um den Pfad des bekannten Ordners zu erhalten oder festzulegen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>Iknownfoldermanager</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen vorhandene bekannte Ordner erstellt, aufgelistet oder verwaltet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>Ilaunchsourceappusermodelid</strong></a><br/></td>
<td>Stellt eine Methode zum Abrufen einer <a href="appids.md">appusermodelid</a>bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>Ilaunchsourceviewsizepreference</strong></a><br/></td>
<td>Stellt Methoden zum Abrufen von Informationen über die Quell Anwendung bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>Ilaunchtargetmonitor</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>Ilaunchtargetviewsizepreference</strong></a><br/></td>
<td>Stellt eine Methode zum Abrufen der bevorzugten Ansichts Größe für ein neues Anwendungsfenster bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>Imarkupcallback</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>Imendupopup</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>Imendupopup</strong></a> kann geändert werden oder nicht verfügbar sein.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>Imodalwindow</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die ein modales Fenster darstellt. Diese Schnittstelle wird im Windows XP Passport-Assistenten verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="imultimonitordockingsite.md"><strong>Imultimonitordockingsite</strong></a><br/></td>
<td>Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste in einem System mit mehreren Monitoren enthält. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>Inamedpropertybag</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein Objekt mit einem angegebenen Eigenschaften Behälter bereitstellen, in dem das Objekt seine Eigenschaften speichern kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>Inamedpropertystore</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen benannte Eigenschaften erhalten und festgelegt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>Inamespacetreeaccessible</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Barrierefreiheits Aktionen für ein shellelement aus einem Namespace Struktur-Steuerelement ausführen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>Inamespacetreecontrol</strong></a><br/></td>
<td>Macht Methoden verfügbar, die zum Anzeigen und Bearbeiten von Knoten in einer Struktur von shellelementen verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>inamespacetreecontrol</strong></a> -Schnittstelle durch Bereitstellen von Methoden, die die Anzeige Stile von TreeView-Steuerelementen für die Verwendung mit Shell-Namespace Elementen aufrufen und festlegen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>Inamespacetreecontrolcustomdraw</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen der Benutzer ein benutzerdefiniertes Namespace Struktur-Steuerelement und seine Elemente zeichnen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>Inamespacetreecontroldrophandler</strong></a><br/></td>
<td>Macht Handlermethoden für Drag & Drop verfügbar. Wird vom Namespace Struktur-Steuerelement verwendet, um den Client über alle Drag & Drop-Vorgänge im Steuerelement zu benachrichtigen. Bietet eine Möglichkeit für einen Client, einen Drop-Vorgang abzufangen und eine eigene Aktion auszuführen oder den gewünschten Ablage Effekt zurückzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>Inamespacetreecontrolevents</strong></a><br/></td>
<td>Macht Methoden für die Behandlung von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>inamespacetreecontrol</strong></a> -Ereignissen verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>Inamespacetreecontrolfolderfunktionen</strong></a><br/></td>
<td>Macht eine einzelne Methode verfügbar, die den Status der Filter Unterstützung für <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System. ispinnedtonamespacetree</a> eines Ordners abruft.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>Inamespacewalk</strong></a><br/></td>
<td>Macht Methoden verfügbar, die einen Namespace aus einem angegebenen Stamm Knoten durchlaufen. Die Tiefe der exemplarischen Vorgehensweise wird angegeben, und es wird ein optionales Array zurückgegeben, das die IDs aller übergingen Knoten enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>Inamespacewalkcb</strong></a><br/></td>
<td>Eine Rückruf Schnittstelle zur Offenlegung von Methoden, die mit <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>inamespacewalk</strong></a>verwendet werden. Nach dem Ausführen einer exemplarischen Vorgehensweise mit <strong>inamespacewalk</strong>wird ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> -Objekt, das die übergeordneten Knoten darstellt, an die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>inamespacewalkcb</strong></a> -Methoden übergeben. Welche Methoden diese Methoden mit den Informationen ausführen, hängt von dem Objekt ab, das Sie implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a><br/></td>
<td>Erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>inamespacewalkcb</strong></a> um eine Methode, die erforderlich ist, um einen Namespace-Walk abzuschließen. Mit dieser Methode werden die während des Durchlaufs gesammelten Daten entfernt. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>Inewmenuclient</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Elemente in einem Windows 7-Menü bearbeitet werden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>Inewshortcuthook</strong></a><br/></td>
<td>Macht Methoden zum Erstellen einer neuen Internet Verknüpfung verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die bestimmt, ob ein Fenster, das von einem anderen Fenster gestartet wird, angezeigt oder blockiert werden soll, sodass Popup Fenster gesteuert werden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>Inotifyreplica</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die dem Ersteller eines Objekts die Möglichkeit bietet, das Objekt zu benachrichtigen, dass es möglicherweise einer nachfolgenden Abstimmung unterliegt. Der Aktentasche-Rückruf ist für die Implementierung dieser Schnittstelle verantwortlich.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>Iobjectarray</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Clients auf Elemente in einer Auflistung von Objekten, die <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>unterstützen, zugreifen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>Iobjectcollection</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>iobjectarray</strong></a> -Schnittstelle durch Bereitstellen von Methoden, die Clients das Hinzufügen und Entfernen von Objekten ermöglichen, die <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> in einer Auflistung unterstützen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>Iobjectprovider</strong></a><br/></td>
<td>Macht eine Methode verfügbar, um Objekte zu ermitteln, die mit einer <strong>GUID</strong> aus einem anderen Objekt benannt werden. Anders als bei <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> delegiert diese Schnittstelle ihre Funktionalität nicht an andere Objekte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>Iobjectwithappusermodelid</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Implementierer eines benutzerdefinierten <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>iassochandler</strong></a> -Objekts Zugriff auf seine explizite Anwendungsmodell-ID (appusermodelid) bereitstellen kann. Diese Informationen werden verwendet, um zu bestimmen, ob ein bestimmter Dateityp zur Sprung Liste einer Anwendung hinzugefügt werden kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>Iobjectwithbackreferences</strong></a><br/></td>
<td>Stellt eine Methode für die Interaktion mit Rück verweisen dar, die von einem-Objekt gehalten werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>Iobjectwithcancelevent</strong></a><br/></td>
<td>Stellt einen Aufrufer mit einem Ereignis bereit, das vom aufgerufenen Objekt signalisiert wird, um den Abbruch einer Aufgabe anzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>Iobjectwithfolderenummode</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen enumerationsmodi eines analysierten Elements erhalten und festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>Iobjectwithprogid</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Zugriff auf die ProgID bereitstellen, die einem Objekt zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>Iobjectwithpropertykey</strong></a><br/></td>
<td>Macht Methoden zum erhalten und Festlegen des Eigenschafts Schlüssels verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>Iobjectwithselection</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen ausgewählte, von einem shellelementarray dargestellte Elemente angezeigt oder festgelegt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>Iobjmgr</strong></a><br/></td>
<td>Macht Methoden verfügbar, die einem Client das Anfügen oder Entfernen eines Objekts aus einer Auflistung von Objekten ermöglichen, die von einem Server Objekt verwaltet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>Iopencontrolpanel</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen der Ansichts Zustand der Systemsteuerung, der Pfad der einzelnen System Steuerungselemente, und das Öffnen der Systemsteuerung selbst oder eines einzelnen System Steuerungs Elements abgerufen wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>Iopensearchsource</strong></a><br/></td>
<td>Macht eine Methode verfügbar, um Suchergebnisse aus einer benutzerdefinierten Client seitigen OpenSearch-Datenquelle zu erhalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>Ioperationsprogressdialog</strong></a><br/></td>
<td>Macht Methoden verfügbar, um ein Status Dialogfeld zu erhalten, festzulegen und abzufragen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>Ipackagedebugsettings</strong></a><br/></td>
<td>Ermöglicht Debugger-Entwicklern, den Lebenszyklus einer Windows Store-App zu steuern, z. b. das Anhalten oder fortsetzen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>Ipackageexecutionstatus-Eigenschaft</strong></a><br/></td>
<td>Ermöglicht das Empfangen von Benachrichtigungen zum Ändern des Paket Zustands während des Debuggens von Windows Store<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>Ipartanditem</strong></a><br/></td>
<td>Macht Methoden verfügbar, die das übergeordnete Element und die untergeordnete ID des übergeordneten Elements erhalten und festlegen. Obwohl <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>iparser</strong></a> in der Regel auf ishellitems implementiert ist, ist es nicht spezifisch für <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>Iccandkreateitem</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>Ipersistfolder</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die shellordnerobjekte initialisiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen aus shellordnerobjekten abrufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>ipersistfolder</strong></a> -und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> -Schnittstellen, indem es einem Ordner Objekt ermöglicht, eine nicht standardmäßige Behandlung von Ordner Verknüpfungen zu implementieren<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>Ipersistidlist</strong></a><br/></td>
<td>Macht Methoden verfügbar, die zum Beibehalten von elementbezeichnerlisten verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>Ipersistserializedpropstorage</strong></a><br/></td>
<td>Macht Methoden verfügbar, um serialisierte Eigenschafts Speicherdaten für die spätere Verwendung zu speichern und persistente Daten in einer neuen Eigenschafts Speicher Instanz wiederherzustellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a><br/></td>
<td>Macht Methoden verfügbar, um serialisierte Eigenschafts Speicherdaten für die spätere Verwendung zu speichern und persistente Daten in einer neuen Eigenschafts Speicher Instanz wiederherzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>Iplaybackmanager</strong></a><br/></td>
<td>Stellt Methoden bereit, die Medienanwendungen die Kommunikation mit dem Windows-Wiedergabe-Manager ermöglichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>Iplaybackmanagerevents</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a><br/></td>
<td>Macht Methoden für die Anzeige umfassender Vorschau Versionen verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a><br/></td>
<td>Ermöglicht es Vorschau Handlern, Tastenkombinationen an den Host zu übergeben. Diese Schnittstelle ruft eine Liste von Tastenkombinationen ab und weist den Host an, eine Tastenkombination zu verarbeiten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a><br/></td>
<td>Macht Methoden zum Anwenden von Farb-und Schriftart Informationen auf Vorschau Handler verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>Ipreviewitem</strong></a><br/></td>
<td>Identifiziert ein Element, das im Vorschaufenster angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>Ipreviousversionsinfo</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die eine Überprüfung auf vorherige Versionen von Server Dateien oder Ordnern durchführen, die von der mit Windows Server 2003 bereitgestellten <em>Schatten Kopien</em> -Technologie zum Zwecke der Neuversion gespeichert wurden.<br/></td>
</tr>
<tr class="odd">
<td><a href="iprivateidentitymanager.md"><strong>Iprivateidentitymanager</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>Iprofferservice</strong></a><br/></td>
<td>Macht einen allgemeinen Mechanismus für-Objekte verfügbar, um anderen Objekten auf demselben Host Dienste anzubieten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>Iprogressdialog</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Optionen für eine Anwendung bereitstellen, um ein Status Dialogfeld anzuzeigen. Diese Schnittstelle wird durch das Status Dialogfeld Objekt (CLSID_ProgressDialog) exportiert. Dieses Objekt ist eine generische Methode, um einem Benutzer anzuzeigen, wie ein Vorgang fortgesetzt wird. Sie wird in der Regel verwendet, wenn eine große Anzahl von Dateien gelöscht, hochgeladen, kopiert, verschoben oder heruntergeladen wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>Ipublishedapp</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Anwendungen zum Hinzufügen/Entfernen von Programmen in der Systemsteuerung darstellen. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>ipublishedapp</strong></a> -Schnittstelle durch Bereitstellen einer zusätzlichen Installationsmethode.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>Ipublishingwizard</strong></a><br/></td>
<td>Macht Methoden zum Arbeiten mit dem Online Druck-Assistenten, dem Webpublishing-Assistenten und dem Assistenten zum Hinzufügen von Netzwerk Stellen verfügbar. In Windows Vista unterstützt <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>ipublishingwizard</strong></a> den Webpublishing-Assistenten oder den Online Druck-Assistenten nicht mehr.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>Iqueryzuordnungen</strong></a><br/></td>
<td>Macht Methoden verfügbar, die den Prozess des Abrufens von in der Registrierung gespeicherten Informationen in Verbindung mit dem Definieren eines Dateityps oder Protokolls und dem zuordnen zu einer Anwendung vereinfachen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>Iquerycancelautoplay</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die automatisch <a href="autorun2k-intro.md">AutoPlay</a> oder <a href="autoplay.md">Autorun</a>überschreibt. Auf diese Weise können Sie den Speicherort und den Typ des Inhalts anpassen, der beim Einfügen von Medien gestartet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>Iquerycodepage</strong></a><br/></td>
<td>Ruft den numerischen Wert (Code Page Bezeichner) der ANSI-Codepage ab und legt diesen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>Iquerycontinue</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen einfachen Standardmechanismus für-Objekte bereitstellt, mit dem ein Client eine Berechtigung zum Fortsetzen eines Vorgangs abfragt. Clients von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>iusernotification</strong></a>müssen z. b. eine Implementierung von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>iquerycontinue</strong></a> an die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>iusernotification:: Show</strong></a> -Methode übergeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>Iquerycontinuewithstatus</strong></a><br/></td>
<td>Macht Methoden verfügbar, die einen Standardmechanismus für Anmelde Informationsanbieter bereitstellen, um <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>querycontinue</strong></a> aufzurufen, während versucht wird, eine Verbindung mit dem Netzwerk herzustellen. Anmelde Informationsanbieter können diese Schnittstelle auch zum Anzeigen von Meldungen für den Benutzer verwenden, wenn Sie versuchen, eine Netzwerkverbindung herzustellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>Iqueryinfo</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Shell zum Abrufen von Flags und infotip-Informationen für ein Element verwendet, das sich in einer <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> -Implementierung befindet. Info-Tipps werden normalerweise in <a href="/windows/desktop/Controls/tooltip-controls">einem</a> QuickInfo-Steuerelement angezeigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>Irelateditem</strong></a><br/></td>
<td>Macht Methoden verfügbar, die verwandte Elemente mit bestimmten Beziehungen ableiten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>Iremotecomputer</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die eine Namespace Erweiterung auflistet oder initialisiert, wenn Sie für ein Remote Objekt aufgerufen wird. Diese Schnittstelle wird z. b. verwendet, um den virtuellen Ordner für Remote Drucker zu initialisieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>Iresolveshelllink</strong></a><br/></td>
<td>Macht eine Methode verfügbar, mit der eine Anwendung anfordern kann, dass ein shellordnerobjekt einen Link für eines ihrer Elemente auflöst.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>Iresulsordner</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Elemente aus einem Datenobjekt enthalten.<br/> Ein <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>iresulsorfolder</strong></a> -Ordner ist ein Ordner, der Elemente von allen über dem Namespace speichern und für den Benutzer in einem einzelnen Ordner darstellen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a><br/></td>
<td>Eine frei Thread Schnittstelle, die von einem-Objekt verfügbar gemacht werden kann, um die Ausführung von Vorgängen in einem Hintergrund Thread zuzulassen. Wenn z. b. die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>iextractimage:: getLocation</strong></a> -Methode E_PENDING zurückgibt, kann die aufrufenden Anwendung das Bild in einem Hintergrund Thread extrahieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>Isearchboxinfo</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen der Aufrufer die in ein Suchfeld eingegebenen Informationen abrufen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>Isearchcontext</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Anpassungs Informationen an die Suchhooks leiten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>Isearchfolderitemfactory</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Suchordner erstellt und geändert werden. Die Set-Methoden werden zuerst aufgerufen, um die Parameter für die Suche einzurichten. Wenn Sie nicht aufgerufen werden, werden stattdessen Standardwerte verwendet. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>Isearchfolderitemfactory:: getidlist</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>isearchfolderitemfactory:: getshellitem</strong></a> geben die beiden Formen der Suche zurück, die von diesen Parametern angegeben werden. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>Isharedbitmap</strong></a><br/></td>
<td>Macht Speicher effiziente Methoden für den Zugriff auf Bitmaps verfügbar. Diese Schnittstelle wird als schlanker Wrapper um HBITMAP-Objekte verwendet, sodass diese Objekte auf eine Verweis Zählung verweisen und vor der Änderung ihrer zugrunde liegenden Daten geschützt werden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>Isharingconfigurationmanager</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen zu den Standard Freigabe Einstellungen eines Computers für den <strong>Benutzer</strong> ( <code>C:\Users</code> ) oder den <strong>öffentlichen</strong> Ordner () festlegen und Abrufen <code>C:\Users\Public</code> . Stellt außerdem einen Satz von Methoden zur Verfügung, die die Steuerung der Druckerfreigabe ermöglichen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>Ishellapp</strong></a><br/></td>
<td>Macht Methoden verfügbar, die allgemeine Informationen zu einer Anwendung für die Anwendung "Programme hinzufügen/entfernen" bereitstellen. Sie können Sie nicht außerhalb der Anwendung Programme hinzufügen/entfernen verwenden. Die von dieser Schnittstelle vorgegebenen Informationen enthalten eine Liste der unterstützten Verwaltungs Aktionen und ob die Anwendung zurzeit installiert ist. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>Ishellbrowser</strong></a><br/></td>
<td>Wird von Hosts von shellsichten (Objekte, die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a>implementieren) implementiert. Macht Methoden verfügbar, die Dienste für die Ansicht bereitstellen, die Sie gehostet, und andere Objekte, die im Kontext des Explorer-Fensters ausgeführt werden. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>Ishellchangenotify</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die eine Shellnamespace-Erweiterung benachrichtigt, wenn sich die ID eines Elements geändert hat.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>Ishelldetails</strong></a><br/></td>
<td>Verfügbar gemacht von shellordnern, um ausführliche Informationen zu den Elementen in einem Ordner bereitzustellen. Dies sind die gleichen Informationen, die von Windows Explorer angezeigt werden, wenn die Ansicht des Ordners auf Details festgelegt ist. Für Windows 2000-Systeme und spätere Systeme wird <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>ishelldetails</strong></a> von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>abgelöst.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>Ishellextinit</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die Shellerweiterungen für Eigenschaften Blätter, Kontextmenüs und Drag & Drop-Handler initialisiert (Erweiterungen, die Elemente zu Kontextmenüs bei nicht standardmäßigen Drag & Drop-Vorgängen hinzufügen).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a><br/></td>
<td>Werden von allen Shell-Namespace-Ordner Objekten verfügbar gemacht, werden die zugehörigen Methoden zum Verwalten von Ordnern verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a><br/></td>
<td>Erweitert die Funktionen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>. Die zugehörigen Methoden bieten eine Vielzahl von Informationen über den Inhalt eines shellordners.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfoldersearchable.md"><strong>Ishellfoldersearchable</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="ishellfoldersearchablecallback.md"><strong>Ishellfoldersearchablecallback</strong></a><br/></td>
<td>Macht Rückruf Routinen zum Überwachen des Suchprozesses verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>Ishellfolderviewcb</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die Kommunikation zwischen Windows-Explorer und einer Ordneransicht ermöglicht, die mithilfe des Systemordner View-Objekts implementiert wurde (das <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a> -Objekt, das über <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>shkreateshellfolderview</strong></a>zurückgegeben wurde), sodass die Ordneransicht über Ereignisse benachrichtigt und seine Ansicht entsprechend geändert werden kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>Ishellfolderviewdual</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen die Ansicht geändert und Elemente im aktuellen Ordner ausgewählt werden. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen die Ansicht geändert und Elemente im aktuellen Ordner ausgewählt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen die aktuelle Ordneransicht geändert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfolderviewtype.md"><strong>Ishellfolderviewtype</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen ein Shellordner verschiedene Ansichten für seinen Inhalt unterstützt (verschiedene hierarchische Layouts der Daten).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>Ishellicon</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen Symbol Index für ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> -Objekt abruft. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>Ishellikooverlay</strong></a><br/></td>
<td>Macht Methoden verfügbar, die von einer Namespace Erweiterung zum Angeben von Symbol Überlagerungen für die darin enthaltenen Objekte verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>Ishellienoverlayidentifier</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die gesamte Kommunikation zwischen Symbol Überlagerungs Handlern und der-Shell verarbeiten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>Ishellimagedataabort</strong></a><br/></td>
<td>Macht eine einzelne Methode verfügbar, mit der <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>ishellimagedata</strong></a> -Prozesse abgebrochen werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>Ishellimagedatafactory</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>ishellimagedata</strong></a> -Instanzen basierend auf verschiedenen Bildquellen erstellt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen zu einem shellelement abrufen. <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> sind die bevorzugten Darstellungen von Elementen in neuem Code.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a><br/></td>
<td>Erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> mit Methoden, die verschiedene Eigenschaftswerte des Elements abrufen. <strong>IShellItem</strong> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> sind die bevorzugten Darstellungen von Elementen in neuem Code.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>Ishellitemarray</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>shellelementarrays</strong></a> erstellt und bearbeitet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>Ishellitemfilter</strong></a><br/></td>
<td>Wird von einem Client verfügbar gemacht, um anzugeben, wie die Enumeration eines <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>shellelements</strong></a> von einer Serveranwendung gefiltert werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>Ishellitemimagefactory</strong></a><br/></td>
<td>Macht eine Methode verfügbar, um entweder Symbole oder Miniaturansichten für shellelemente zurückzugeben. Wenn keine Miniaturansicht oder kein Symbol für das angeforderte Element verfügbar ist, kann ein pro-Klasse-Symbol von der Shell bereitgestellt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>Ishellitemresources</strong></a><br/></td>
<td>Macht Methoden zum Bearbeiten und Abfragen von shellelementressourcen verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>Ishelllibrary</strong></a><br/></td>
<td>Macht Methoden zum Erstellen und Verwalten von Bibliotheken verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen shelllinks erstellt, geändert und aufgelöst werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>Ishelllinkdatalist</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung zusätzliche Datenblöcke an einen <a href="/windows/desktop/shell/links">shelllink</a>anfügen kann. Mit diesen Methoden werden Datenblöcke hinzugefügt, kopiert oder entfernt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>Ishellmenu</strong></a><br/></td>
<td>Macht Methoden verfügbar, die mit shellmenüs wie dem <strong>Startmenü</strong> und dem Menü " <strong>Favoriten</strong> " interagieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>Ishellmenucallback</strong></a><br/></td>
<td>Eine Rückruf Schnittstelle, die eine Methode verfügbar macht, die Nachrichten von einem Menüband empfängt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>Ishellpropsheetext</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen ein Eigenschaften Blatt Handler Seiten im Eigenschaften Blatt hinzufügen oder ersetzen kann, die für ein Datei Objekt angezeigt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>Ishellrundll</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>Ishellview</strong></a><br/></td>
<td>Macht Methoden verfügbar, die eine Ansicht in den Windows-Explorer-oder-Ordner Fenstern darstellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a><br/></td>
<td>Erweitert die Funktionen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a><br/></td>
<td>Erweitert die Funktionen von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> durch Bereitstellen einer Methode zum Ersetzen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2:: CreateViewWindow2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a><br/></td>
<td>Ermöglicht den Zugriff auf die Auflistung von geöffneten shellfenstern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>Istartmenupinnedlist</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die eine Anwendungs Verknüpfung im <strong>Startmenü</strong> oder in der Taskleiste aufsetzt.<br/></td>
</tr>
<tr class="odd">
<td><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>Istorageprovidercopyhook</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>Istorageproviderhandler</strong></a><br/></td>
<td>Ruft den <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>istorageproviderpropertyhandler</strong></a> ab, der einer bestimmten Datei oder einem Ordner zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>Istorageproviderpropertyhandler</strong></a><br/></td>
<td>Stellt eine Auflistung von Eigenschaften bereit, die einer Datei oder einem Ordner zugeordnet sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>Istreamasync</strong></a><br/></td>
<td>Macht Methoden zum Verwalten von Eingabe/Ausgabe (e/a) für einen asynchronen Datenstrom verfügbar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>Istreamunbufferedinfo</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die Sektorgröße als Unterstützung für Byte-Ausrichtung bestimmt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>Isuspensiondependencymanager</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>Isyncmgrconflict</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen zu einem Konflikt bereitstellen, der aus einem Konflikt Speicher abgerufen wurde, und ermöglicht es, den Konflikt aufzulösen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>Isyncmgrconflictfolder</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die Konflikt-ID-Liste für ein Konflikt Objekt abruft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>Isyncmgrconflictitems</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Konflikt Elementdaten und die Element Anzahl erhalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>Isyncmgrconflictpresenter</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die einen Konflikt für den Benutzer darstellt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>Isyncmgrconflictresolutionitems</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Element Informationen und die Element Anzahl erhalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>Isyncmgrconflictresolveingefo</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Informationen über die Konfliktlösung des Synchronisierungs-Managers erhalten und festlegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>Isyncmgrconflictstore</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es einem Handler ermöglichen, Konflikte bereitzustellen, die im Ordner Konflikte angezeigt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>Isyncmgrcontrol</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es einer Anwendung oder einem Handler ermöglichen, eine Synchronisierung zu starten oder zu beenden, das Synchronisierungs Center über Änderungen am Satz von Handlern oder Elementen zu benachrichtigen oder über Änderungen an Eigenschafts Werten zu benachrichtigen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>Isyncmgrenumitems</strong></a><br/></td>
<td>Macht Methoden verfügbar, die durch ein Array von <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>syncmgritem</strong></a> -Strukturen aufgezählt werden. Jede dieser Strukturen stellt Informationen zu einem Element bereit, das synchronisiert werden kann. <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>Isyncmgrenumitems</strong></a> verfügt über dieselben Methoden wie alle standardmäßigen Enumeratorschnittstellen: Next, Skip, Reset und Clone.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>Isyncmgrevent</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Daten aus einem Ereignisspeicher abrufen. Mit einem Ereignisspeicher kann das Synchronisierungs Center einen Enumerator aller Ereignisse im Speicher abrufen und einzelne Ereignisse abrufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>Isyncmgreventlinkuioperation</strong></a><br/></td>
<td>Stellt eine Methode bereit, die aufgerufen wird, wenn auf Ereignis Verknüpfungen im Ordner Synchronisierungs Ergebnisse geklickt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>Isyncmgreventstore</strong></a><br/></td>
<td>Macht Methoden verfügbar, die es einem Handler ermöglichen, seinen eigenen Ereignisspeicher bereitzustellen und seine eigenen Synchronisierungs Ereignisse zu verwalten, anstatt den standardmäßigen Synchronisierungs Center-Ereignisspeicher zu verwenden. Diese Ereignisse werden im Ordner Synchronisierungs Ergebnisse angezeigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>Isyncmgrhandler</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die von einem Synchronisierungs Handler implementierte primäre Schnittstelle bilden. Das Synchronisierungs Center erstellt eine Instanz des Handlers über diese Schnittstelle, um Eigenschaften zu erhalten, Synchronisierungs Elemente aufzuzählen und den Status zu ändern. Das Synchronisierungs Center erstellt eine separate Instanz des Handlers in einem separaten Thread, um eine Synchronisierung oder einen UI-Vorgang auszuführen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>Isyncmgrhandlercollection</strong></a><br/></td>
<td>Macht Methoden verfügbar, die einen Enumerator von synchronisierungshandlerids bereitstellen und diese Synchronisierungs Handler instanziieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>Isyncmgrhandlerinfo</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen ein Handler Eigenschaften-und Zustandsinformationen für das Synchronisierungs Center bereitstellen kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>Isyncmgrregister</strong></a><br/></td>
<td>Macht Methoden verfügbar, sodass eine Anwendung beim Synchronisierungs-Manager registriert werden kann. Dies kann entweder über die <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>isyncmgrregister</strong></a> -Schnittstelle oder durch die direkte Registrierung in der Registrierung erreicht werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>Isyncmgrresolutionhandler</strong></a><br/></td>
<td>Macht Methoden verfügbar, die das Synchronisieren von Konflikten verwalten. Implementieren Sie diese Schnittstelle, um einen Synchronisierungs Konflikt Handler zu erstellen. Die Benutzeroberfläche für die Konflikt Auflösung ruft diese Schnittstelle auf, um den Konflikt aufzulösen, der dem Benutzer angezeigt wird. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>Isyncmgrschedulewizarduioperation</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die es einem Handler ermöglicht, den Synchronisierungs Zeitplan-Assistenten für den Handler anzuzeigen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>Isyncmgrsessioncreator</strong></a><br/></td>
<td>Macht eine einzelne Methode verfügbar, über die ein Handler oder eine externe Anwendung das Synchronisierungs Center benachrichtigen kann, dass die Synchronisierung begonnen hat, sowie den Status und Ereignisse melden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>Isyncmgrsynccallback</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen ein Synchronisierungs Prozess den Status und die Ereignisse an das Synchronisierungs Center melden kann, oder um abzufragen, ob der Prozess abgebrochen wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>Isyncmgrsync</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen die registrierte Anwendung oder der registrierte Dienst Benachrichtigungen von der Synchronisierungs Verwaltung empfangen kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>Isyncmgrsynchronizecallback</strong></a><br/></td>
<td>Macht Methoden verfügbar, die den Synchronisierungs Prozess verwalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>Isyncmgrsynchronizeingevoke</strong></a><br/></td>
<td>Macht Methoden verfügbar, die einer registrierten Anwendung ermöglichen, den Synchronisierungs-Manager zum Aktualisieren von Elementen aufzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>Isyncmgrsyncitem</strong></a><br/></td>
<td>Macht Methoden verfügbar, die auf Informationen von einem einzelnen Synchronisierungs Element reagieren und diese abrufen, sodass Handler Synchronisierungs Elemente als unabhängige Objekte verwalten können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>Isyncmgrsyncitemcontainer</strong></a><br/></td>
<td>Macht Methoden verfügbar, die den Handlern Informationen zu den darin enthaltenen Elementen bereitstellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>Isyncmgrsynciteminfo</strong></a><br/></td>
<td>Macht Methoden verfügbar, die Eigenschafts-und Zustandsinformationen für ein einzelnes Synchronisierungs Element bereitstellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>Isyncmgrsynkresult</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die Anwendungen, die <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>isyncmgrcontrol</strong></a> aufrufen, verwenden können, um das Ergebnis eines <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>isyncmgrcontrol:: starthandlersync</strong></a> -oder <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>isyncmgrcontrol:: startitemsync</strong></a> -Aufrufs abzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>Isyncmgruioperation</strong></a><br/></td>
<td>Macht eine Methode verfügbar, über die ein Synchronisierungs Handler oder ein Synchronisierungs Element ein UI-Objekt anzeigen kann, wenn dies von Sync Center angefordert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Taskleiste steuern. Sie ermöglicht es Ihnen, Elemente auf der Taskleiste dynamisch hinzuzufügen, zu entfernen und zu aktivieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>itaskbarlist</strong></a> -Schnittstelle, indem eine Methode verfügbar gemacht wird, um ein Fenster als voll Bild Anzeige zu markieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a><br/></td>
<td>Erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> durch das verfügbar machen von Methoden, die die vereinheitlichte Schaltfläche "Start" und "Switch" der Taskleiste unterstützen Diese Funktion umfasst Miniaturansichten und switchziele basierend auf einzelnen Registerkarten in einer Anwendung im Registerkarten Format, Miniatur Ansichts Symbolleisten, Benachrichtigungs-und Status Überlagerungen und Status Indikatoren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a><br/></td>
<td>Erweitert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> durch Bereitstellen einer Methode, die es dem Aufrufer ermöglicht, zwei Eigenschaftswerte für die Registerkarte "Miniaturansicht" und "Peek"<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>Ithumbnailcache</strong></a><br/></td>
<td>Macht Methoden für einen System-Miniatur Ansichts Cache verfügbar, der Anwendungs übergreifend gemeinsam verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>Ithumbnailcacheprimer</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>Ithumbnailhandlerfactory</strong></a><br/></td>
<td>Macht eine Methode zum Abrufen des Miniatur Ansichts Handlers eines Elements verfügbar. Implementieren Sie diese Schnittstelle, wenn Sie angeben möchten, welcher Extraktor für eine untergeordnete idlist verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>IThumbnailProvider</strong></a><br/></td>
<td>Macht eine Methode zum erhalten eines Miniatur Bilds verfügbar und ist für die Implementierung für Miniatur Ansichts Handler vorgesehen. Das Objekt, das diese Schnittstelle implementiert, muss auch <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>implementieren. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>Ithumbnailsettings</strong></a><br/></td>
<td>Stellt eine Methode bereit, die einem Miniatur Ansichts Anbieter ermöglicht, den Benutzer Kontext einer Miniatur Ansichts Anforderung zu bestimmen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>Ithumbnailstreamcache</strong></a><br/></td>
<td>Ruft den Miniatur Ansichts Strom ab oder legt ihn fest. Diese Schnittstelle ist nur für die interne Verwendung vorgesehen und kann nur von der Fotos-Anwendung aufgerufen werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>Itrackshellmenu</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>ishellmenu</strong></a> -Schnittstelle erweitern, indem Sie die Möglichkeit bietet, Symbolleisten-Schaltflächen mit einem Menü zu koordinieren und ein Popup Menü anzuzeigen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>Itranscodeimage</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die die Konvertierung in JPEG-oder Bitmap-Bildformate (BMP) aus jedem von Windows unterstützten Bildtyp zulässt. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>Itransferadvisesink</strong></a><br/></td>
<td>Macht Methoden verfügbar, die die Status Erfassung und Fehlerinformationen unterstützen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>Itransferdestination</strong></a><br/></td>
<td>Macht Methoden verfügbar, die ein zielshellelement für einen Kopier-oder verschiebe Vorgang erstellen. Diese Schnittstelle wird bereitgestellt, um eine bessere Kontrolle über Datei Vorgänge durch Bereitstellen einer <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>itransferdestination:: Empfehlung</strong></a> -Methode zu ermöglichen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>Itransfermediumitem</strong></a><br/></td>
<td>Wird von einer Kopier-Engine verwendet, um das Element abzurufen, für das <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> aufgerufen werden soll, um einen Zeiger auf die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>itransferdestination</strong></a> -Schnittstelle oder die Interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>itransfersource</strong></a>zurückzugeben Diese Schnittstellen können abgefragt und für Kopier-, verschiebe-oder Löschvorgänge aufgelistet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>Itransfersource</strong></a><br/></td>
<td>Macht Methoden zum Bearbeiten von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>verfügbar, einschließlich kopieren, verschieben, wieder verwenden und anderen. Diese Schnittstelle wird angeboten, um mehr Kontrolle über Datei Vorgänge zu bieten, indem eine <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>itransfersource:: Empfehlung</strong></a> -Methode bereitgestellt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>Itraydeskband</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Desktop Bänder angezeigt, ausgeblendet und abgefragt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>Iupdateidlist</strong></a><br/></td>
<td>Stellt eine Methode zum Aktualisieren der <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittlerer List</strong></a> des untergeordneten Elements eines Ordner Objekts bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>Iurlsearchhook</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die vom Browser zum Übersetzen der Adresse eines unbekannten URL-Protokolls verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die vom Browser verwendet wird, um die Adresse eines unbekannten URL-Protokolls mithilfe eines Such Kontext Objekts zu übersetzen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>Iuseraccountchangecallback</strong></a><br/></td>
<td>Macht eine Methode verfügbar, die aufgerufen wird, wenn das Bild, das ein Benutzerkonto darstellt, geändert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>Iusernotification</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Benachrichtigungs Informationen festgelegt werden, und zeigt diese Benachrichtigung für den Benutzer in einer Sprechblase an, die in Verbindung mit dem Benachrichtigungsbereich der Taskleiste angezeigt wird. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> unterscheidet sich von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>iusernotification</strong></a> nur in der <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> -Methode, die einen zusätzlichen Parameter für eine Rückruf Schnittstelle hinzufügt, um mit der Benachrichtigung zu kommunizieren. Andernfalls sind die beiden Schnittstellen in Form und Funktion identisch. CLSID_UserNotification implementiert beide Versionen von <strong>Show</strong> als Überladung.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen Benachrichtigungs Informationen festgelegt werden, und zeigt diese Benachrichtigung für den Benutzer in einer Sprechblase an, die in Verbindung mit dem Benachrichtigungsbereich der Taskleiste angezeigt wird. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> erbt nicht von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>iusernotification</strong></a>. <strong>IUserNotification2</strong> unterscheidet sich von <strong>iusernotification</strong> nur in der <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> -Methode, die einen zusätzlichen Parameter für eine Rückruf Schnittstelle hinzufügt, um mit der Benachrichtigung zu kommunizieren. Andernfalls sind die beiden Schnittstellen in Form und Funktion identisch. CLSID_UserNotification implementiert beide Versionen von <strong>Show</strong> als Überladung.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>Iusernotificationcallback</strong></a><br/></td>
<td>Macht eine Methode für die Behandlung von Mausklicks oder Kontextmenü Zugriff in einer Benachrichtigungs Sprechblase verfügbar. Wird mit <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2:: Show</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>Iuseum browseitem</strong></a><br/></td>
<td>Sucht das Element, das beim Navigieren zu diesem Element verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>Iviewstatueidentityitem</strong></a><br/></td>
<td>Stellt ein kanonisches persistenzelement bereit, ein Element, für das Ansichts Anpassungen gespeichert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>Ivirtualdesktopmanager</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen eine Anwendung mit Windows-Gruppen interagieren kann, die virtuelle Arbeitsbereiche bilden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>Ivisualproperties</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen visuelle Eigenschaften festgelegt und angezeigt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>Iwebwizardextension</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>iwizardextension</strong></a> -Schnittstelle durch das verfügbar machen von Methoden zum Festlegen der anfänglichen URL der Assistenten Erweiterung und eine bestimmte URL im Falle eines Fehlers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>Iwizardextension</strong></a><br/></td>
<td>Wird von Assistenten wie dem Webpublishing-Assistenten und dem Assistenten für die Online-druckbestellung verwendet, der serverseitige Inhaltsseiten hostet. Diese Schnittstelle macht Methoden zum angeben unterstützter Erweiterungs Seiten und zum Navigieren zu und aus diesen Seiten verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>Iwizardsite</strong></a><br/></td>
<td>Macht Methoden verfügbar, die von einer Assistenten Erweiterung zum Navigieren in den Rahmen zwischen sich und dem restlichen Assistenten verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="taskcompletionclient.md"><strong>Taskcompletionclient</strong></a><br/></td>
<td>Aktiviert die Aufgaben Vervollständigung. <br/></td>
</tr>
</tbody>
</table>



 

 

 