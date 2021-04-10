---
title: Text Objektmodell
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit dem Text Objektmodell (Tom) verwendet werden.
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103858524"
---
# <a name="text-object-model"></a>Text Objektmodell

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit dem Text Objektmodell (Tom) verwendet werden.

Der Tom definiert einen beträchtlichen Satz an Text Bearbeitungs Schnittstellen. Text Lösungen wie Microsoft Word und Rich Edit-Steuerelemente unterstützen die Tom-Funktionsgruppe. Tom hat sich stark von WordBasic (der Programmiersprache, die für Word verwendet wird) beeinflusst und ist von Microsoft Visual Basic for Applications (VBA) leicht zu verwenden. Diese Kompatibilität hat mehrere Vorteile:

-   Code kann relativ einfach von einer Lösung zu einer anderen migriert werden.
-   Eine Sprache kann verwendet werden, um Textinformationen zwischen verschiedenen Text Modulen gemeinsam zu nutzen.
-   Es verringert den Bedarf an Dokumentation und Code im Vergleich zu separaten Component Object Model (com) und VBA-Schnittstellen auf niedriger Ebene.

Allerdings kann es für C/C++-Zwecke weniger effizient sein als die Verwendung allgemeiner com-Schnittstellen auf niedrigerer Ebene.

Tom ist ein einfacher Satz von Schnittstellen, die für seine primären Textlösungen, Word und Rich Edit-Steuerelemente implementiert werden können. Bei Anwendungen, die einen geringfügigen Schwerpunkt auf Text legen, ist es jedoch besser, Tom-Schnittstellen bereitzustellen, indem der Text in ein Bearbeitungs Steuerelement übertragen wird, das Tom Da Rich Edit-Steuerelemente mit Microsoft-Betriebssystemen ausgeliefert werden, sind Sie die Standardmethode, Tom-Funktionen zu erhalten.

### <a name="overviews"></a>Übersichten



| Thema                                                          | Inhalte                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum Text Objektmodell](about-text-object-model.md)         | Das Tom-Objekt (Text Object Model) der obersten Ebene wird von der [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle definiert, die über Methoden zum Erstellen und Abrufen von Objekten in der Objekthierarchie verfügt.<br/> |
| [Verwenden des Text Objektmodells](using-the-text-object-model.md) | Die Codebeispiele in diesem Dokument zeigen verschiedene Aspekte der Verwendung des Text Objektmodells (Tom).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Schnittstellen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></td>
<td>Die <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> -Schnittstelle ist die Oberfläche der obersten Ebene von Tom, mit der die aktiven Auswahl-und Bereichs Objekte für jede Story im Dokument abgerufen werden, unabhängig davon, ob Sie aktiv ist oder nicht. Dadurch kann die Anwendung folgende Aktionen ausführen:
<ul>
<li>Dokumente öffnen und speichern.</li>
<li>Steuerelement rückgängigverhalten und Bildschirm Aktualisierung</li>
<li>Einen Bereich von einer Bildschirmposition aus suchen.</li>
<li>Einen <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>itextstoryranges</strong></a> Story-Enumerator erhalten.</li>
</ul>
<br/> <strong>Zeitpunkt der Implementierung</strong><br/> Anwendungen implementieren die <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> -Schnittstelle in der Regel nicht. Microsoft-Textlösungen, wie z. b. Rich Edit-Steuerelemente, implementieren <strong>ITextDocument</strong> als Teil ihrer Tom-Implementierung. <br/> <strong>Verwendungs Zeitpunkt</strong><br/> Anwendungen können einen <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> -Zeiger von einem Rich Edit-Steuerelement abrufen. Senden Sie hierzu eine <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> Nachricht, um ein <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>iricheditole</strong></a> -Objekt von einem Rich Edit-Steuerelement abzurufen. Rufen Sie dann die <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> -Methode des Objekts auf, um einen <strong>ITextDocument</strong> -Zeiger abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>Itextfont</strong></a></td>
<td>Der Zugriff auf Tom Rich-Text Bereichs Attribute erfolgt über ein paar von Dual Schnittstellen, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>itextfont</strong></a> und <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>itextpara</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>Itextpara</strong></a></td>
<td>Der Zugriff auf Tom Rich-Text Bereichs Attribute erfolgt über ein paar von Dual Schnittstellen, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>itextfont</strong></a> und <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>itextpara</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>Itextrange</strong></a></td>
<td>Die <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>itextrange</strong></a> -Objekte sind leistungsstarke Tools für die Bearbeitung und Datenbindung, die es einem Programm ermöglichen, Text in einer Story auszuwählen und dann diesen Text zu überprüfen oder zu ändern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>Itextselection</strong></a></td>
<td>Bei einer Textauswahl handelt es sich um einen Textbereich mit Auswahl Hervorhebung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>Itextstorybereiche</strong></a></td>
<td>Der Zweck der <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>itextstoryranges</strong></a> -Schnittstelle besteht darin, die Stories in einem <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>aufzulisten.<br/></td>
</tr>
</tbody>
</table>



 

 

