---
description: In diesem Abschnitt werden die Windows -Objekte beschrieben, die von der Shell implementiert werden.
title: Shellobjekte für Skripterstellung und Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bd2c924d9b66194c8f016fc8b1c16bed8a7e3c62f82e3673837e0e31c8563fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858799"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Shellobjekte für Skripterstellung und Microsoft Visual Basic

In diesem Abschnitt werden die Windows -Objekte beschrieben, die von der Shell implementiert werden.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br/></td>
<td>Ermöglicht es einem Client, die globalen Datenträgerkontingenteinstellungen eines NTFS-Volumes zu verwalten. Dieses Objekt macht die wesentlichen Funktionen der <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser-Schnittstelle</strong></a> für Skripts und Microsoft Visual Basic-basierte Anwendungen verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Ermöglicht es einem Administrator, die Datenträgerkontingenteigenschaften eines Volumes zu verwalten. Das NTFS-Dateisystem ermöglicht es einem Administrator, die Datenträgernutzung auf einem freigegebenen Volume zu verwalten, indem jedem Benutzer eine bestimmte Menge an Speicherplatz oder ein <em>Kontingentlimit</em>zugewiesen wird. Sie können dieses Objekt verwenden, um das Standardkontingentlimit festzulegen, das automatisch allen neuen Benutzern zugewiesen wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Empfängt <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows-Fensterregistrierungsereignisse.</strong></a> <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Ordner</strong></a><br/></td>
<td>Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Folder2</strong></a><br/></td>
<td>Erweitert das <a href="folder.md"><strong>Folder-Objekt</strong></a> zur Unterstützung von Offlineordnern.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Erweitert das <a href="folderitems.md"><strong>FolderItems-Objekt.</strong></a> Es unterstützt eine zusätzliche Methode.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Erweitert das <a href="folderitems2-object.md"><strong>FolderItems2-Objekt.</strong></a> Dieses Objekt unterstützt eine zusätzliche Methode und Eigenschaft.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Stellt ein einzelnes Verb dar, das für ein Element verfügbar ist. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Verb abrufen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Stellt die Auflistung von Verben für ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Stellt ein Objekt in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle innerhalb der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte abzurufen. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch.md"><strong>IShellDispatch-Objekt</strong></a> um eine Vielzahl neuer Funktionen. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch2-object.md"><strong>IShellDispatch2-Objekt.</strong></a> <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> unterstützt zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch2</strong>unterstützt werden, eine neue Methode. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shell-Objekt.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch3.md"><strong>IShellDispatch3-Objekt.</strong></a> Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch3</strong>unterstützt werden, unterstützt <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> vier zusätzliche Methoden. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch4.md"><strong>IShellDispatch4-Objekt.</strong></a> Zusätzlich zu den von <strong>IShellDispatch4</strong>unterstützten Eigenschaften und Methoden fügt <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch5.md"><strong>IShellDispatch5-Objekt.</strong></a> Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch5</strong>unterstützt werden, fügt <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> eine Methode hinzu, die den Bereich Apps-Suche anzeigt. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Erweitert das <a href="shelllinkobject-object.md"><strong>ShellLinkObject-Objekt</strong></a> und unterstützt eine zusätzliche Eigenschaft.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Erweitert das <a href="webwizardhost.md"><strong>WebWizardHost-Objekt,</strong></a> indem serverseitige Seiten, die in einem Assistenten gehostet werden, aktiviert werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Stellt die Objekte in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle innerhalb der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte abzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Erweitert das <a href="folderitem.md"><strong>FolderItem-Objekt.</strong></a> Zusätzlich zu den Eigenschaften und Methoden, die von <strong>FolderItem</strong>unterstützt werden, verfügt <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> über zwei zusätzliche Methoden.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Stellt die -Objekte in einer Sicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Sicht verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Leitet die von einem angegebenen <a href="shellfolderview.md"><strong>ShellFolderView-Objekt</strong></a> ausgelösten Ereignisse an die entsprechenden <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC-Ereignishandler</strong></a> weiter.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Verwaltet Shelllinks. Dieses Objekt macht einen Großteil der Funktionalität der <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink-Schnittstelle</strong></a> für Skriptanwendungen verfügbar. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>Wird von der Shell implementiert, um Skripts und Visual Basic Entwickler bei der Verwendung einiger der in der Shell verfügbaren Features zu unterstützen. Das <a href="shelluihelper.md"><strong>ShellUIHelper-Objekt</strong></a> verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Methoden, die diesen Objekten zugeordnet sind, können Befehle in der Shell steuern und ausführen und andere Shell-bezogene Objekte abrufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen HTML-Seiten, die in einer Assistentenerweiterung gehostet werden, mit dem Assistenten kommunizieren können.<br/></td>
</tr>
</tbody>
</table>



 

 

 




