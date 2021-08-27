---
description: In diesem Abschnitt werden die von der Shell implementierten Windows-Objekte beschrieben.
title: Shellobjekte für Skripterstellung und Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e4d367b836516259a4c0f73cea9da20e7e13326
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465027"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Shellobjekte für Skripterstellung und Microsoft Visual Basic

In diesem Abschnitt werden die von der Shell implementierten Windows-Objekte beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br /> | Ermöglicht es einem Client, die globalen Datenträgerkontingenteinstellungen eines NTFS-Volumes zu verwalten. Dieses Objekt macht die wesentlichen Funktionen der <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser-Schnittstelle</strong></a> für Skripts und Microsoft Visual Basic-basierte Anwendungen verfügbar.<br /> | 
| <a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br /> | Ermöglicht es einem Administrator, die Datenträgerkontingenteigenschaften eines Volumes zu verwalten. Das NTFS-Dateisystem ermöglicht es einem Administrator, die Datenträgernutzung auf einem freigegebenen Volume zu verwalten, indem jedem Benutzer eine bestimmte Menge an Speicherplatz oder ein <em>Kontingentlimit</em>zugewiesen wird. Sie können dieses Objekt verwenden, um das Standardkontingentlimit festzulegen, das automatisch allen neuen Benutzern zugewiesen wird.<br /> | 
| <a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br /> | Empfängt <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows-Fensterregistrierungsereignisse.</strong></a> <br /> | 
| <a href="folder.md"><strong>Ordner</strong></a><br /> | Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.<br /> | 
| <a href="folder2-object.md"><strong>Ordner2</strong></a><br /> | Erweitert das <a href="folder.md"><strong>Folder-Objekt</strong></a> zur Unterstützung von Offlineordnern.<br /> | 
| <a href="folderitem.md"><strong>FolderItem</strong></a><br /> | Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.<br /> | 
| <a href="folderitems.md"><strong>FolderItems</strong></a><br /> | Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.<br /> | 
| <a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br /> | Erweitert das <a href="folderitems.md"><strong>FolderItems-Objekt.</strong></a> Es unterstützt eine zusätzliche Methode.<br /> | 
| <a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br /> | Erweitert das <a href="folderitems2-object.md"><strong>FolderItems2-Objekt.</strong></a> Dieses Objekt unterstützt eine zusätzliche Methode und Eigenschaft.<br /> | 
| <a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br /> | Stellt ein einzelnes Verb dar, das für ein Element verfügbar ist. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Verb abrufen können.<br /> | 
| <a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br /> | Stellt die Auflistung von Verben für ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.<br /> | 
| <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br /> | Stellt ein Objekt in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle innerhalb der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte abzurufen. <br /><blockquote>[!Note]<br /><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.</blockquote><br /> | 
| <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br /> | Erweitert das <a href="ishelldispatch.md"><strong>IShellDispatch-Objekt</strong></a> um eine Vielzahl neuer Funktionen. <br /><blockquote>[!Note]<br /><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.</blockquote><br /> | 
| <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br /> | Erweitert das <a href="ishelldispatch2-object.md"><strong>IShellDispatch2-Objekt.</strong></a> <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> unterstützt zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch2</strong>unterstützt werden, eine neue Methode. <br /><blockquote>[!Note]<br /><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.</blockquote><br /> | 
| <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br /> | Erweitert das <a href="ishelldispatch3.md"><strong>IShellDispatch3-Objekt.</strong></a> Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch3</strong>unterstützt werden, unterstützt <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> vier zusätzliche Methoden. <br /><blockquote>[!Note]<br /><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.</blockquote><br /> | 
| <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br /> | Erweitert das <a href="ishelldispatch4.md"><strong>IShellDispatch4-Objekt.</strong></a> Zusätzlich zu den von <strong>IShellDispatch4</strong>unterstützten Eigenschaften und Methoden fügt <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt. <br /><blockquote>[!Note]<br /><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.</blockquote><br /> | 
| <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br /> | Erweitert das <a href="ishelldispatch5.md"><strong>IShellDispatch5-Objekt.</strong></a> Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch5</strong>unterstützt werden, fügt <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> eine Methode hinzu, die den Bereich Apps-Suche anzeigt. <br /><blockquote>[!Note]<br /><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shell-Objekt</strong></a> aufgerufen.</blockquote><br /> | 
| <a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br /> | Erweitert das <a href="shelllinkobject-object.md"><strong>ShellLinkObject-Objekt</strong></a> und unterstützt eine zusätzliche Eigenschaft.<br /> | 
| <a href="newwdevents.md"><strong>NewWDEvents</strong></a><br /> | Erweitert das <a href="webwizardhost.md"><strong>WebWizardHost-Objekt,</strong></a> indem serverseitige Seiten, die in einem Assistenten gehostet werden, aktiviert werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.<br /> | 
| <a href="shell.md"><strong>Shell</strong></a><br /> | Stellt die Objekte in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle innerhalb der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte abzurufen.<br /> | 
| <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br /> | Erweitert das <a href="folderitem.md"><strong>FolderItem-Objekt.</strong></a> Zusätzlich zu den Eigenschaften und Methoden, die von <strong>FolderItem</strong>unterstützt werden, verfügt <a href="shellfolderitem-object.md"><strong>ShellFolderItem über</strong></a> zwei zusätzliche Methoden.<br /> | 
| <a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br /> | Stellt die Objekte in einer Sicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Sicht verwendet werden.<br /> | 
| <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br /> | Leitet die von einem angegebenen <a href="shellfolderview.md"><strong>ShellFolderView-Objekt</strong></a> ausgelösten Ereignisse an die entsprechenden <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC-Ereignishandler</strong></a> weiter.<br /> | 
| <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br /> | Verwaltet Shelllinks. Dieses Objekt macht einen Großteil der Funktionalität der <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink-Schnittstelle</strong></a> für Skriptanwendungen verfügbar. <br /> | 
| <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br /> | Wird von der Shell implementiert, damit Skript- und Visual Basic Entwickler einige der in der Shell verfügbaren Features verwenden können. Das <a href="shelluihelper.md"><strong>ShellUIHelper-Objekt</strong></a> verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.<br /> | 
| <a href="shellwindows.md"><strong>ShellWindows</strong></a><br /> | Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Methoden, die diesen Objekten zugeordnet sind, können Befehle in der Shell steuern und ausführen und andere Shell-bezogene Objekte abrufen.<br /> | 
| <a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br /> | Macht Methoden verfügbar, mit denen HTML-Seiten, die in einer Assistentenerweiterung gehostet werden, mit dem Assistenten kommunizieren können.<br /> | 




 

 

 




