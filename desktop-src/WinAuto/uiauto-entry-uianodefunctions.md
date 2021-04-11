---
title: Veraltete Knoten Funktionen
description: Veraltete Knoten Funktionen
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103949186"
---
# <a name="deprecated-node-functions"></a>Veraltete Knoten Funktionen

> [!Note]  
> Die in diesem Abschnitt beschriebenen Steuerelement Muster Funktionen sind veraltet. Client Anwendungen sollten die Component Object Model (com)-Schnittstellen verwenden, die in den folgenden Abschnitten beschrieben werden:
>
> -   [Benutzeroberflächenautomatisierungs-Element Schnittstellen für Clients](uiauto-entry-uiautoclientinterfaces.md)
> -   [Eigenschaften Bedingungs Schnittstelle für Clients](uiauto-client-propconditioninterfaces.md)
> -   [Steuerelement Muster-Schnittstellen für Clients](uiauto-client-controlpatterninterfaces.md)
> -   [Ereignis Behandlungs Schnittstellen für Clients](uiauto-client-eventhandlinginterfaces.md)
> -   [Proxyfactory-Schnittstellen für Clients](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>Uiaaddebug</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen der Microsoft UI Automation verwenden.
</blockquote>
<br/> Fügt einen Listener für Ereignisse in einem Knoten in der Benutzeroberflächenautomatisierungs-Struktur hinzu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>Uiaeventaddwindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Fügt dem Ereignislistener ein Fenster hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>Uiaeventcallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Eine vom Client implementierte Funktion, die von der Benutzeroberflächen Automatisierung aufgerufen wird, wenn ein Ereignis ausgelöst wird, das der Client abonniert hat.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>Uiaeventremovewindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Entfernt ein Fenster aus dem Ereignislistener.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>Uiafind</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft mindestens einen Benutzeroberflächenautomatisierungs-Knoten ab, der den Suchkriterien entspricht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>Uiageterrordescription</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft eine Fehler Zeichenfolge ab, damit Sie an den Client übermittelt werden kann. Diese Methode wird nicht direkt von-Clients verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>Uiagetpatternprovider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft ein <em>Steuerelement Muster</em>ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>Uiagetpropertyvalue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den Wert einer Benutzeroberflächenautomatisierungs-Eigenschaft ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>Uiagetrootnode</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den Stamm Knoten für die Benutzeroberflächen Automatisierung ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>Uiagetruntimeid</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den Lauf Zeit Bezeichner eines Benutzeroberflächenautomatisierungs-Knotens ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>Uiagetupdatedcache</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Aktualisiert den Cache von Eigenschafts Werten und Steuerelement Mustern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>Uiahpatternobjectfromvariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft ein Steuerelement Musterobjekt aus einem <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> -Typ ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>Uiahtextrangefromvariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft einen Textbereich von einem <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> -Typ ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>Uiahuianodefromvariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft ein huianode aus einem <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> -Typ ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>Uialookupid</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den ganzzahligen Bezeichner ab, der in Methoden verwendet werden kann, die eine PropertyId, patternId, controltypeid, textattributeid oder EventID erfordern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>Uianavigate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Navigiert in der Benutzeroberflächenautomatisierungs-Struktur und ruft optional zwischengespeicherte Informationen ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>Uianodefromfocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den Benutzeroberflächenautomatisierungs-Knoten für das Benutzeroberflächen Element ab, das derzeit den Eingabefokus besitzt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>Uianodefromhandle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den einem Fenster zugeordneten Benutzeroberflächenautomatisierungs-Knoten ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>Uianodefrompoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den Benutzeroberflächenautomatisierungs-Knoten für das Element am angegebenen Punkt ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>Uianodefromprovider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft den Benutzeroberflächenautomatisierungs-Knoten für einen RAW-Element Anbieter ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>Uianoderelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Löscht einen Knoten aus dem Arbeitsspeicher.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>Uiapatternrelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Löscht ein zugeordneter Musterobjekt aus dem Arbeitsspeicher.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>Uiaprovidercallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Eine Anwendungs definierte Funktion, die von der Benutzeroberflächen Automatisierung aufgerufen wird, um einen Client seitigen Anbieter für ein Element zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>Uiarectiabmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Ruft einen booleschen Wert ab, der angibt, ob für ein Rechteck alle Koordinaten auf 0 festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>Uiarect* tempty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Legt die Elemente einer <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>uiarect</strong></a> -Struktur auf 0 fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>Uiaregisterprovidercallback</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Registriert die Anwendungs definierte Methode, die von der Benutzeroberflächen Automatisierung aufgerufen wird, um einen Anbieter für ein Element zu erhalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>Uiaremuveevent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Entfernt einen Listener für Ereignisse auf einem Knoten in der Benutzeroberflächenautomatisierungs-Struktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>Uiasetfocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Legt den Eingabefokus auf das angegebene Element in der Benutzeroberfläche fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>Uiatextrangerelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Client Anwendungen sollten stattdessen die COM-Schnittstellen für die Benutzeroberflächen Automatisierung verwenden.
</blockquote>
<br/> Löscht ein zugeordneter Text Bereichs Objekt aus dem Arbeitsspeicher.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI-Automatisierungs Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

