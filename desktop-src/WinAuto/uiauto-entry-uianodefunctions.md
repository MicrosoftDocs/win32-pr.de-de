---
title: Veraltete Knotenfunktionen
description: Veraltete Knotenfunktionen
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d700c506ee0bb0baf41cdd2facb85b0e7153d57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476166"
---
# <a name="deprecated-node-functions"></a>Veraltete Knotenfunktionen

> [!Note]  
> Die in diesem Abschnitt beschriebenen Steuerelementmusterfunktionen sind veraltet. Clientanwendungen sollten die in den folgenden Abschnitten Component Object Model (COM)-Schnittstellen verwenden:
>
> -   [Benutzeroberflächenautomatisierung Elementschnittstellen für Clients](uiauto-entry-uiautoclientinterfaces.md)
> -   [Eigenschaftsbedingungsschnittstelle für Clients](uiauto-client-propconditioninterfaces.md)
> -   [Steuerelementmusterschnittstellen für Clients](uiauto-client-controlpatterninterfaces.md)
> -   [Ereignisbehandlungsschnittstellen für Clients](uiauto-client-eventhandlinginterfaces.md)
> -   [Proxy Factory-Schnittstellen für Clients](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>In diesem Abschnitt




| Funktion | BESCHREIBUNG | 
|----------|-------------|
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Microsoft Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Fügt einen Listener für Ereignisse auf einem Knoten in der Benutzeroberflächenautomatisierung hinzu.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Fügt dem Ereignislistener ein Fenster hinzu.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Eine vom Client implementierte Funktion, die von Benutzeroberflächenautomatisierung, wenn ein Ereignis ausgelöst wird, das der Client abonniert hat.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Entfernt ein Fenster aus dem Ereignislistener.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft einen oder mehrere Benutzeroberflächenautomatisierung ab, die den Suchkriterien entsprechen.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft eine Fehlerzeichenfolge ab, damit sie an den Client übergeben werden kann. Diese Methode wird nicht direkt von Clients verwendet.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft ein <em>Steuerelementmuster ab.</em><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Wert einer Benutzeroberflächenautomatisierung ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Stammknoten Benutzeroberflächenautomatisierung ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Laufzeitbezeichner eines Benutzeroberflächenautomatisierung ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Aktualisiert den Cache von Eigenschaftswerten und Steuerelementmustern.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft ein Steuerelementmusterobjekt aus einem <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT-Typ</strong></a> ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft einen Textbereich aus einem <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT-Typ</strong></a> ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft eine HU VARIATIONDE aus einem <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT-Typ</strong></a> ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den ganzzahligen Bezeichner ab, der in Methoden verwendet werden kann, die eine PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID oder EVENTID erfordern.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Navigiert in der Benutzeroberflächenautomatisierung Struktur und ruft optional zwischengespeicherte Informationen ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Benutzeroberflächenautomatisierung knoten für das Benutzeroberflächenelement ab, das derzeit den Eingabefokus besitzt.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Benutzeroberflächenautomatisierung knoten ab, der einem Fenster zugeordnet ist.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Benutzeroberflächenautomatisierung knoten für das Element am angegebenen Punkt ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft den Benutzeroberflächenautomatisierung knoten für einen Rohelementanbieter ab.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Löscht einen Knoten aus dem Arbeitsspeicher.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Löscht ein zugeordnetes Musterobjekt aus dem Arbeitsspeicher.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Eine anwendungsdefinierte Funktion, die von Benutzeroberflächenautomatisierung aufgerufen wird, um einen clientseitigen Anbieter für ein Element abzurufen.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Ruft einen booleschen Wert ab, der angibt, ob für ein Rechteck alle Koordinaten auf 0 festgelegt sind.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Legt die Elemente einer <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect-Struktur</strong></a> auf 0 fest.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Registriert die anwendungsdefinierte Methode, die von Benutzeroberflächenautomatisierung aufgerufen wird, um einen Anbieter für ein Element abzurufen.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Entfernt einen Listener für Ereignisse auf einem Knoten in der Benutzeroberflächenautomatisierung Struktur.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Legt den Eingabefokus auf das angegebene Element in der Benutzeroberfläche fest.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br /> | <blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Clientanwendungen sollten stattdessen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden.</blockquote><br /> Löscht ein zugeordnetes Textbereichsobjekt aus dem Arbeitsspeicher.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächenautomatisierung Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

