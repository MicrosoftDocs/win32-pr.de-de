---
description: In diesem Abschnitt werden die von der Shell implementierten Windows-Objekte beschrieben.
title: Shellobjekte für Skripterstellung und Microsoft-Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529423"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Shellobjekte für Skripterstellung und Microsoft-Visual Basic

In diesem Abschnitt werden die von der Shell implementierten Windows-Objekte beschrieben.

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
<td><a href="didiskquotauser-object.md"><strong>Didiskquotauser</strong></a><br/></td>
<td>Ermöglicht einem Client, die globalen Datenträger Kontingent Einstellungen eines NTFS-Volumes zu verwalten. Dieses Objekt stellt die wesentlichen Funktionen der <a href="didiskquotauser-object.md"><strong>didiskquotauser</strong></a> -Schnittstelle für Skript-und Microsoft Visual Basic-basierte Anwendungen zur Verfügung.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>Diskquotacontrol</strong></a><br/></td>
<td>Ermöglicht es einem Administrator, die Datenträger Kontingent Eigenschaften eines Volumes zu verwalten. Das NTFS-Dateisystem ermöglicht einem Administrator, die Datenträger Verwendung auf einem freigegebenen Volume zu verwalten, indem jedem Benutzer eine angegebene Menge an Speicherplatz oder <em>Kontingent Limit</em>zugewiesen wird. Mit diesem Objekt können Sie die Standard Kontingent Grenze festlegen, die automatisch allen neuen Benutzern zugewiesen wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>Dshellwindowgvents</strong></a><br/></td>
<td>Empfängt <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> -Fenster Registrierungs Ereignisse. <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Ordner</strong></a><br/></td>
<td>Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Folder2</strong></a><br/></td>
<td>Erweitert das <a href="folder.md"><strong>Ordner</strong></a> Objekt, um Offline Ordner zu unterstützen.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>Von folderItem</strong></a><br/></td>
<td>Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>Folderitems</strong></a><br/></td>
<td>Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Erweitert das <a href="folderitems.md"><strong>folderitems</strong></a> -Objekt. Es wird eine zusätzliche Methode unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Erweitert das <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> -Objekt. Dieses Objekt unterstützt eine zusätzliche Methode und Eigenschaft.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>Folderitemverb</strong></a><br/></td>
<td>Stellt ein einzelnes Verb dar, das einem Element zur Verfügung steht. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Verb abrufen können.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>Folderitemverbs</strong></a><br/></td>
<td>Stellt die Auflistung von Verben für ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>Ishelldispatch</strong></a><br/></td>
<td>Stellt ein Objekt in der Shell dar. Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen. Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>Ishelldispatch</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shellobjekt</strong></a> aufgerufen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch.md"><strong>ishelldispatch</strong></a> -Objekt mit einer Reihe von neuen Funktionen. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> -Objekt. <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> unterstützt eine neue Methode zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch2</strong>unterstützt werden. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> -Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch3</strong>unterstützt werden, unterstützt <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> vier zusätzliche Methoden. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> -Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch4</strong>unterstützt werden, fügt <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Erweitert das <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> -Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch5</strong>unterstützt werden, fügt <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> eine Methode hinzu, die den Suchbereich apps anzeigt. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Erweitert das <a href="shelllinkobject-object.md"><strong>shelllinkobject</strong></a> -Objekt und unterstützt eine zusätzliche Eigenschaft.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>Newwentvents</strong></a><br/></td>
<td>Erweitert das <a href="webwizardhost.md"><strong>webwizardhost</strong></a> -Objekt durch Aktivieren von serverseitigen Seiten, die in einem Assistenten gehostet werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Stellt die-Objekte in der Shell dar. Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen. Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>Shellfolderitem</strong></a><br/></td>
<td>Erweitert das <a href="folderitem.md"><strong>folderItem</strong></a> -Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von <strong>folderItem</strong>unterstützt werden, verfügt <a href="shellfolderitem-object.md"><strong>shellfolderitem</strong></a> über zwei zusätzliche Methoden.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>Shellfolderview</strong></a><br/></td>
<td>Stellt die Objekte in einer Ansicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Ansicht verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>Shellfolderviewoc</strong></a><br/></td>
<td>Leitet die von einem angegebenen <a href="shellfolderview.md"><strong>shellfolderview</strong></a> -Objekt ausgelösten Ereignisse an entsprechende <a href="shellfolderviewoc-object.md"><strong>shellfolderviewoc</strong></a> -Ereignishandler weiter.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>Shelllinkobject</strong></a><br/></td>
<td>Verwaltet shelllinks. Dieses Objekt stellt einen Großteil der Funktionen der <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> -Schnittstelle für Skript Anwendungen zur Verfügung. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>Shelluihelper</strong></a><br/></td>
<td>Wird von der Shell implementiert, um Skripts und Visual Basic Entwicklern zu helfen, einige der in der Shell verfügbaren Features zu verwenden. Das <a href="shelluihelper.md"><strong>shelluihelper</strong></a> -Objekt hat keine Eigenschaften oder Ereignisse. Es werden Methoden bereitgestellt, um der Shell Elemente hinzuzufügen.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>Shellwindows</strong></a><br/></td>
<td>Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Mit diesen Objekten verknüpfte Methoden können Befehle in der Shell Steuern und ausführen sowie andere shellbezogene Objekte abrufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>Webwizardhost</strong></a><br/></td>
<td>Macht Methoden verfügbar, mit denen HTML-Seiten aktiviert werden, die in einer Assistenten Erweiterung gehostet werden, um mit dem Assistenten zu kommunizieren.<br/></td>
</tr>
</tbody>
</table>



 

 

 




