---
description: Mit dem PenInputPanel-Objekt können Sie Ihren Anwendungen ganz einfach eingaben.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: PenInputPanel-Klasse (Msinkaut.h)
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
ms.openlocfilehash: 58d27b97bb6683f32c145b92c1fda65fe0a786d5cb502e644580b57366119840
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708340"
---
# <a name="peninputpanel-class"></a>PenInputPanel-Klasse

\[Veraltet. **PenInputPanel** wurde durch den [Texteingabebereich (TIP) ersetzt.](text-input-panel-reference.md)\]

Mit **dem PenInputPanel-Objekt** können Sie Ihren Anwendungen ganz einfach eingaben.

Das **PenInputPanel-Objekt** ist als anfingbares Objekt verfügbar, mit dem Sie vorhandenen Steuerelementen Tablet PC-Eingabebereichsfunktionen hinzufügen können. Die Benutzeroberfläche wird größtenteils von der aktuellen Eingabesprache beauftragt. Sie können die Standardeingabemethode für das **PenInputPanel-Objekt** auswählen, entweder Handschrift oder Tastatur. Der Endbenutzer kann mithilfe von Schaltflächen auf der Benutzeroberfläche zwischen Eingabemethoden wechseln.

**PenInputPanel** verfügt über die folgenden Membertypen:

-   [Enumerationen](#enumerations)
-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="enumerations"></a>Enumerationen

Die **PenInputPanel-Klasse** verfügt über diese Enumerationen.



| Enumeration                    | Beschreibung                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Definiert den Typ der Eingabe, die derzeit im **PenInputPanel-Objekt verfügbar** ist.<br/> |



 

### <a name="events"></a>Ereignisse

Die **PenInputPanel-Klasse** verfügt über diese Ereignisse.



| Ereignis                                                  | Beschreibung                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Tritt ein, wenn sich der Eingabefokus ändert, bevor das **PenInputPanel-Objekt** Benutzereingaben in das angefügte Steuerelement einfügen konnte.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Tritt ein, wenn **sich das PenInputPanel-Objekt** zwischen Layouts ändert.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Tritt ein, wenn **das PenInputPanel-Objekt** bewegt wird.<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Tritt ein, wenn **das PenInputPanel-Objekt** sich selbst angezeigt oder ausgeblendet hat.<br/>                                                         |



 

### <a name="interfaces"></a>Schnittstellen

Die **PenInputPanel-Klasse** definiert diese Schnittstellen.



| Schnittstelle          | BESCHREIBUNG                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Dieses Objekt implementiert die **IPenInputPanel-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **PenInputPanel-Klasse** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Sendet gesammelte Ink-Daten an die Erkennung und sendet das Erkennungsergebnis.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Wenn **TRUE** übergeben wird, versucht **PenInputPanel,** Text über die Textdienstframework (TSF) an das angefügte Steuerelement zu senden, und ermöglicht die Verwendung der Korrektur-Benutzeroberfläche.<br/>    |
| [**Moveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Legt die Position des **PenInputPanel-Objekts** auf eine statische Bildschirmposition fest.<br/>                                                                                                               |
| [**Aktualisieren**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Aktualisiert und stellt die **PenInputPanel-Eigenschaften** basierend auf den Einstellungen des Tablet PC-Eingabebereichs wieder auf, positioniert den Stifteingabebereich automatisch und legt die Benutzeroberfläche auf den Standardbereich fest.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **PenInputPanel-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp           | Beschreibung                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lesen/Schreiben<br/> | Ruft das Fensterhand handle des Steuerelements ab, an das das **PenInputPanel-Objekt** angefügt ist, oder legt dieses fest.<br/>                                                                     |
| [**Autoshow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob das **PenInputPanel-Objekt** angezeigt wird, wenn der Fokus mithilfe des Stifts festgelegt wird, oder legt diesen fest.<br/>                                           |
| [**Beschäftigt**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Schreibgeschützt<br/>  | Ruft einen booleschen Wert ab, der angibt, ob das **PenInputPanel-Objekt** derzeit Ink verarbeitet.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lesen/Schreiben<br/> | Ruft ab oder legt fest, welcher Paneltyp derzeit für die Eingabe im **PenInputPanel-Objekt verwendet** wird.<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lesen/Schreiben<br/> | Ruft ab oder legt fest, welcher Paneltyp der Standardbereichstyp ist, der für die Eingabe im **PenInputPanel-Objekt verwendet** wird.<br/>                                                         |
| [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lesen/Schreiben<br/> | Ruft den Zeichenfolgennamen des in der Erkennung verwendeten Factoids ab oder legt diese fest.<br/>                                                                                                    |
| [**Höhe**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Schreibgeschützt<br/>  | Ruft die Höhe des **PenInputPanel-Objekts** in Clientkoordinaten ab.<br/>                                                                                              |
| [**Horizontaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lesen/Schreiben<br/> | Ruft den Offset zwischen dem linken Rand des **PenInputPanel-Objekts** und dem linken Rand des Steuerelements ab, an das es angefügt ist, oder legt diesen fest.<br/>                             |
| [**Links**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Schreibgeschützt<br/>  | Ruft die horizontale Position (oder x-Achse) des linken Rands des **PenInputPanel-Objekts** in Bildschirmkoordinaten ab.<br/>                                                   |
| [**Nach oben**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Schreibgeschützt<br/>  | Ruft die vertikale Position oder y-Achse des oberen Rands des **PenInputPanel-Objekts** in Bildschirmkoordinaten ab.<br/>                                                      |
| [**Verticaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lesen/Schreiben<br/> | Ruft den Offset zwischen dem nächstgelegenen horizontalen Rand des **PenInputPanel-Objekts** und dem nächstgelegenen horizontalen Rand des Steuerelements ab, an das es angefügt ist, oder legt diesen fest.<br/> |
| [**Sichtbar**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob das **PenInputPanel-Objekt** sichtbar ist, oder legt diesen fest.<br/>                                                                                |
| [**Breite**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Schreibgeschützt<br/>  | Ruft die Breite des **PenInputPanel-Objekts** in Clientkoordinaten ab.<br/>                                                                                               |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Programmieren des Eingabebereichs mit der PenInputPanel-Klasse](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
