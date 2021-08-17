---
title: Optionale Methoden
description: Optionale Methoden
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64f4b22693c77295d3a21cfb59055f9a232d08bb1426d995f710bbf24073d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130042"
---
# <a name="optional-methods"></a>Optionale Methoden

Eine OLE-Komponente kann eine Schnittstelle implementieren, ohne die ganze Semantik jeder Methode in der Schnittstelle zu implementieren, sondern stattdessen E NOTIMPL oder \_ S OK entsprechend \_ zurückgeben. In der folgenden Tabelle werden die Methoden beschrieben, die von ActiveX Steuerelementcontainer nicht implementiert werden müssen (d. h., der Steuerelementcontainer kann E \_ NOTIMPL zurückgeben).

In der folgenden Tabelle werden optionale Methoden beschrieben. Beachten Sie, dass die Methode noch vorhanden sein muss, aber einfach E NOTIMPL zurückgeben \_ kann, anstatt echte Semantik zu implementieren. Beachten Sie, dass jede Methode aus einer obligatorischen Schnittstelle, die unten nicht aufgeführt ist, als obligatorisch angesehen werden muss und E NOTIMPL möglicherweise \_ nicht zurück gibt.

## <a name="ioleclientsite"></a>IOleClientSite



| Methode                                                     | Kommentare                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Erforderlich, damit Persistenz erfolgreich unterstützt wird.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Nur erforderlich, wenn der Container das Verknüpfen mit Steuerelementen in seinem eigenen Formular oder Dokument unterstützt.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Methode                                                                     | Kommentare                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Optional<br/>                                      |
| [**Blättern**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Gibt möglicherweise S \_ FALSE ohne Aktion zurück.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Kann S \_ OK ohne Aktion zurückgeben.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | Die Deaktivierung ist obligatorisch. Rückgängig ist optional. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Methode                                                                          | Kommentare                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Erforderlich für Container, die erweiterte Steuerelemente unterstützen.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Erforderlich für Container, die ihre eigenen Eigenschaftenseiten enthalten möchten, um erweiterte Steuerelementeigenschaften zusätzlich zu den von einem -Steuerelement bereitgestellten Eigenschaften zu verarbeiten.<br/> |
| [**Translateaccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Gibt möglicherweise S \_ FALSE ohne Aktion zurück.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Optional<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (Ambient-Eigenschaften)



| Methode                      | Kommentare                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Erforderlich für Container, die nicht standardmäßige Umgebungseigenschaften unterstützen.<br/> |
| GetTypeInfo<br/>      | Erforderlich für Container, die nicht standardmäßige Umgebungseigenschaften unterstützen.<br/> |
| GetIDsOfNames<br/>    | Erforderlich für Container, die nicht standardmäßige Umgebungseigenschaften unterstützen.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (Ereignissenke)



| Methode                      | Kommentare                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Das Steuerelement kennt seine eigenen Typinformationen, sodass es diese nicht aufrufen muss.<br/> |
| GetTypeInfo<br/>      | Das Steuerelement kennt seine eigenen Typinformationen, sodass es diese nicht aufrufen muss.<br/> |
| GetIDsOfNames<br/>    | Das Steuerelement kennt seine eigenen Typinformationen, sodass es diese nicht aufrufen muss.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Methode                                                                           | Kommentare                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Erforderlich für Container mit Symbolleistenbenutzeroberfläche (optional)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Erforderlich für Container mit Symbolleistenbenutzeroberfläche (optional)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Erforderlich für Container mit Symbolleistenbenutzeroberfläche (optional)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Erforderlich für Container mit Menübenutzeroberfläche (optional)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Erforderlich für Container mit Menübenutzeroberfläche (optional)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Erforderlich für Container mit Menübenutzeroberfläche (optional)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Nur für Container erforderlich, die über eine Statuszeile verfügen<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Optional<br/>                                                     |
| [**Translateaccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Optional<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Methode                                                                    | Kommentare                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Nur wenn das Verknüpfen mit Steuerelementen oder anderen Einbettungen im Container unterstützt wird, da dies für die Monikerbindung erforderlich ist.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Wie für ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Gibt alle ActiveX-Steuerelemente über einen [**Enumerator mit IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)zurück, aber nicht unbedingt alle Objekte (da es keine Garantie gibt, dass alle Objekte ActiveX-Steuerelemente sind; einige sind möglicherweise reguläre Windows-Steuerelemente).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

