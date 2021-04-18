---
description: Mit dem PenInputPanel-Objekt können Sie Ihren Anwendungen problemlos direkte Stift Eingaben hinzufügen.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: "\"Pinputpanel\"-Klasse (\"msink AUT. h\")"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366227"
---
# <a name="peninputpanel-class"></a>Pinputpanel-Klasse

\[Veraltet. " **Tzinputpanel** " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.\]

Mit dem **PenInputPanel** -Objekt können Sie Ihren Anwendungen problemlos direkte Stift Eingaben hinzufügen.

Das Objekt " **pinputpanel** " steht als anfügbares Objekt zur Verfügung, mit dem Sie vorhandenen Steuerelementen Tablet PC-Eingabe Bereichs Funktionen hinzufügen können. Die Benutzeroberfläche wird größtenteils von der aktuellen Eingabe Sprache vorgeschrieben. Sie haben die Möglichkeit, die Standardeingabe Methode für **das Objekt "** " mit dem Objekt "", entweder Handschrift oder Tastatur, auszuwählen. Der Endbenutzer kann mithilfe von Schaltflächen auf der Benutzeroberfläche zwischen Eingabemethoden wechseln.

" **Pinputpanel** " verfügt über folgende Typen von Membern:

-   [Enumerationen](#enumerations)
-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="enumerations"></a>Enumerationen

Diese Enumerationen sind **in der Klasse** "" der Klasse "" von "".



| Enumeration                    | Beschreibung                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Definiert den Typ der Eingabe, die zurzeit im Objekt " **pinputpanel** " verfügbar ist.<br/> |



 

### <a name="events"></a>Ereignisse

Diese Ereignisse werden **von der Klasse** "" in der Klasse "".



| Ereignis                                                  | BESCHREIBUNG                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Tritt auf, wenn sich der Eingabefokus ändert, bevor das Objekt " **pinputpanel** " Benutzereingaben in das angefügte Steuerelement einfügen konnte.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Tritt auf, wenn sich das Objekt " **pinputpanel** " zwischen Layouts ändert.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Tritt auf, wenn das Objekt " **pinputpanel** " verschoben wird.<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Tritt auf, **Wenn das "** "-Objekt des ""-Objekts angezeigt oder ausgeblendet wird.<br/>                                                         |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der Klasse " **pinputpanel** " definiert.



| Schnittstelle          | BESCHREIBUNG                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **Ipinputpanel** | Dieses Objekt implementiert die **ipinputpanel** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die Klasse " **pinputpanel** " verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Commitpdinginput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Sendet gesammelte frei Hand Eingaben an die Erkennung und stellt das Erkennungs Ergebnis dar.<br/>                                                                                                                      |
| [**Enabletsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Wenn **true** angegeben wird, versucht das " **tzinputpanel** ", Text über das Text Services-Framework (TSF) an das angefügte Steuerelement zu senden, und ermöglicht die Verwendung der Benutzeroberfläche zur Korrektur.<br/>    |
| [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Legt die Position des " **pinputpanel** "-Objekts auf eine statische Bildschirmposition fest.<br/>                                                                                                               |
| [**Aktualisieren**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Aktualisiert und stellt die **PenInputPanel** -Eigenschaften auf Grundlage der Einstellungen für den Tablet PC-Eingabebereich wieder her, positioniert automatisch den Stift Eingabebereich und legt die Benutzeroberfläche auf den Standardbereich fest.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die Klasse " **pinputpanel** " verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lesen/Schreiben<br/> | Ruft das Fenster Handle des Steuer Elements ab oder legt dieses fest, an das das " **pinputpanel** "-Objekt angefügt ist.<br/>                                                                     |
| [**Automatisch anzeigen**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob das **PenInputPanel** -Objekt angezeigt wird, wenn der Fokus mithilfe des Stifts festgelegt wird<br/>                                           |
| [**Busy**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Schreibgeschützt<br/>  | Ruft einen booleschen Wert ab, der angibt, ob das " **cuinputpanel** "-Objekt zurzeit frei Hand Eingaben verarbeitet.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lesen/Schreiben<br/> | Ruft ab oder legt fest, welcher Panel-Typ zurzeit für Eingaben innerhalb des " **pinputpanel** "-Objekts verwendet wird.<br/>                                                                |
| [**Defaultpanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lesen/Schreiben<br/> | Ruft ab oder legt fest, welcher Bereichs Datentyp der Standard Bereichs Datentyp ist **, der für** die Eingabe innerhalb des "" "" "" "<br/>                                                         |
| [**Faktoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lesen/Schreiben<br/> | Ruft den Zeichen folgen Namen des in der Erkennung verwendeten Faktoid ab oder legt diesen fest.<br/>                                                                                                    |
| [**Höhe**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Schreibgeschützt<br/>  | Ruft die Höhe des " **pinputpanel** "-Objekts in Client Koordinaten ab.<br/>                                                                                              |
| [**Horizontal Offset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lesen/Schreiben<br/> | Ruft den Offset zwischen dem linken Rand des " **pinputpanel** "-Objekts und dem linken Rand des Steuer Elements ab, an das es angefügt ist, oder legt diesen fest.<br/>                             |
| [**Linken**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Schreibgeschützt<br/>  | Ruft die horizontale bzw. x-Achse, Position des linken Rands des " **tabinputpanel** "-Objekts in Bildschirm Koordinaten ab.<br/>                                                   |
| [**Nach oben**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Schreibgeschützt<br/>  | Ruft die vertikale Achse bzw. y-Achse, Position des oberen Rands des **Objekt-** Objekts in Bildschirm Koordinaten ab.<br/>                                                      |
| [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lesen/Schreiben<br/> | Ruft den Offset zwischen dem nächstgelegenen horizontalen Rand des " **kinputpanel** "-Objekts und dem nächstgelegenen horizontalen Rand des Steuer Elements ab, an das es angefügt ist, oder legt diesen fest.<br/> |
| [**Sichtbar**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das Objekt " **pinput Panel** " sichtbar ist.<br/>                                                                                |
| [**Breite**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Schreibgeschützt<br/>  | Ruft die Breite des " **pinputpanel** "-Objekts in Client Koordinaten ab.<br/>                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel"](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
