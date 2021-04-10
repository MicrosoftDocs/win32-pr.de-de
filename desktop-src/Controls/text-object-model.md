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
# <a name="text-object-model"></a><span data-ttu-id="64064-103">Text Objektmodell</span><span class="sxs-lookup"><span data-stu-id="64064-103">Text Object Model</span></span>

<span data-ttu-id="64064-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit dem Text Objektmodell (Tom) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64064-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="64064-105">Der Tom definiert einen beträchtlichen Satz an Text Bearbeitungs Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="64064-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="64064-106">Text Lösungen wie Microsoft Word und Rich Edit-Steuerelemente unterstützen die Tom-Funktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="64064-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="64064-107">Tom hat sich stark von WordBasic (der Programmiersprache, die für Word verwendet wird) beeinflusst und ist von Microsoft Visual Basic for Applications (VBA) leicht zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="64064-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="64064-108">Diese Kompatibilität hat mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="64064-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="64064-109">Code kann relativ einfach von einer Lösung zu einer anderen migriert werden.</span><span class="sxs-lookup"><span data-stu-id="64064-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="64064-110">Eine Sprache kann verwendet werden, um Textinformationen zwischen verschiedenen Text Modulen gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="64064-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="64064-111">Es verringert den Bedarf an Dokumentation und Code im Vergleich zu separaten Component Object Model (com) und VBA-Schnittstellen auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="64064-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="64064-112">Allerdings kann es für C/C++-Zwecke weniger effizient sein als die Verwendung allgemeiner com-Schnittstellen auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="64064-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="64064-113">Tom ist ein einfacher Satz von Schnittstellen, die für seine primären Textlösungen, Word und Rich Edit-Steuerelemente implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="64064-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="64064-114">Bei Anwendungen, die einen geringfügigen Schwerpunkt auf Text legen, ist es jedoch besser, Tom-Schnittstellen bereitzustellen, indem der Text in ein Bearbeitungs Steuerelement übertragen wird, das Tom</span><span class="sxs-lookup"><span data-stu-id="64064-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="64064-115">Da Rich Edit-Steuerelemente mit Microsoft-Betriebssystemen ausgeliefert werden, sind Sie die Standardmethode, Tom-Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="64064-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="64064-116">Übersichten</span><span class="sxs-lookup"><span data-stu-id="64064-116">Overviews</span></span>



| <span data-ttu-id="64064-117">Thema</span><span class="sxs-lookup"><span data-stu-id="64064-117">Topic</span></span>                                                          | <span data-ttu-id="64064-118">Inhalte</span><span class="sxs-lookup"><span data-stu-id="64064-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64064-119">Informationen zum Text Objektmodell</span><span class="sxs-lookup"><span data-stu-id="64064-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="64064-120">Das Tom-Objekt (Text Object Model) der obersten Ebene wird von der [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle definiert, die über Methoden zum Erstellen und Abrufen von Objekten in der Objekthierarchie verfügt.</span><span class="sxs-lookup"><span data-stu-id="64064-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="64064-121">Verwenden des Text Objektmodells</span><span class="sxs-lookup"><span data-stu-id="64064-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="64064-122">Die Codebeispiele in diesem Dokument zeigen verschiedene Aspekte der Verwendung des Text Objektmodells (Tom).</span><span class="sxs-lookup"><span data-stu-id="64064-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="64064-123">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="64064-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64064-124">Thema</span><span class="sxs-lookup"><span data-stu-id="64064-124">Topic</span></span></th>
<th><span data-ttu-id="64064-125">Inhalte</span><span class="sxs-lookup"><span data-stu-id="64064-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64064-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="64064-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="64064-127">Die <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> -Schnittstelle ist die Oberfläche der obersten Ebene von Tom, mit der die aktiven Auswahl-und Bereichs Objekte für jede Story im Dokument abgerufen werden, unabhängig davon, ob Sie aktiv ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="64064-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="64064-128">Dadurch kann die Anwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64064-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="64064-129">Dokumente öffnen und speichern.</span><span class="sxs-lookup"><span data-stu-id="64064-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="64064-130">Steuerelement rückgängigverhalten und Bildschirm Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="64064-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="64064-131">Einen Bereich von einer Bildschirmposition aus suchen.</span><span class="sxs-lookup"><span data-stu-id="64064-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="64064-132">Einen <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>itextstoryranges</strong></a> Story-Enumerator erhalten.</span><span class="sxs-lookup"><span data-stu-id="64064-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="64064-133"><strong>Zeitpunkt der Implementierung</strong></span><span class="sxs-lookup"><span data-stu-id="64064-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="64064-134">Anwendungen implementieren die <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> -Schnittstelle in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="64064-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="64064-135">Microsoft-Textlösungen, wie z. b. Rich Edit-Steuerelemente, implementieren <strong>ITextDocument</strong> als Teil ihrer Tom-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="64064-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="64064-136"><strong>Verwendungs Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="64064-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="64064-137">Anwendungen können einen <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> -Zeiger von einem Rich Edit-Steuerelement abrufen.</span><span class="sxs-lookup"><span data-stu-id="64064-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="64064-138">Senden Sie hierzu eine <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> Nachricht, um ein <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>iricheditole</strong></a> -Objekt von einem Rich Edit-Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="64064-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="64064-139">Rufen Sie dann die <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> -Methode des Objekts auf, um einen <strong>ITextDocument</strong> -Zeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="64064-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64064-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>Itextfont</strong></a></span><span class="sxs-lookup"><span data-stu-id="64064-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="64064-141">Der Zugriff auf Tom Rich-Text Bereichs Attribute erfolgt über ein paar von Dual Schnittstellen, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>itextfont</strong></a> und <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>itextpara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="64064-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64064-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>Itextpara</strong></a></span><span class="sxs-lookup"><span data-stu-id="64064-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="64064-143">Der Zugriff auf Tom Rich-Text Bereichs Attribute erfolgt über ein paar von Dual Schnittstellen, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>itextfont</strong></a> und <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>itextpara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="64064-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64064-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>Itextrange</strong></a></span><span class="sxs-lookup"><span data-stu-id="64064-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="64064-145">Die <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>itextrange</strong></a> -Objekte sind leistungsstarke Tools für die Bearbeitung und Datenbindung, die es einem Programm ermöglichen, Text in einer Story auszuwählen und dann diesen Text zu überprüfen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="64064-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64064-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>Itextselection</strong></a></span><span class="sxs-lookup"><span data-stu-id="64064-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="64064-147">Bei einer Textauswahl handelt es sich um einen Textbereich mit Auswahl Hervorhebung.</span><span class="sxs-lookup"><span data-stu-id="64064-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64064-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>Itextstorybereiche</strong></a></span><span class="sxs-lookup"><span data-stu-id="64064-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="64064-149">Der Zweck der <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>itextstoryranges</strong></a> -Schnittstelle besteht darin, die Stories in einem <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="64064-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

