---
title: Optionale Methoden
description: Optionale Methoden
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102382"
---
# <a name="optional-methods"></a>Optionale Methoden

Eine OLE-Komponente kann eine Schnittstelle implementieren, ohne dass die gesamte Semantik jeder Methode in der Schnittstelle implementiert wird. stattdessen wird "E \_ notimpl" oder "S OK" zurückgegeben \_ . In der folgenden Tabelle werden die Methoden beschrieben, die von einem ActiveX-Steuerelement Container nicht implementiert werden müssen (d. h., der Steuerelement Container kann e \_ notimpl zurückgeben).

In der folgenden Tabelle werden optionale Methoden beschrieben: Beachten Sie, dass die Methode weiterhin vorhanden sein muss, aber einfach E notimpl zurückgeben kann, \_ anstatt eine wirkliche Semantik zu implementieren. Beachten Sie, dass jede Methode aus einer obligatorischen Schnittstelle, die nicht unten aufgeführt ist, als obligatorisch angesehen werden muss und E \_ notimpl nicht zurückgibt.

## <a name="ioleclientsite"></a>IOleClientSite



| Methode                                                     | Kommentare                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Saveobject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Erforderlich, damit die Persistenz erfolgreich unterstützt wird.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Nur erforderlich, wenn der Container das Verknüpfen mit Steuerelementen in einem eigenen Formular oder Dokument unterstützt.<br/> |



 

## <a name="ioleinplacesite"></a>Ioleingeplacesite



| Methode                                                                     | Kommentare                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Optional<br/>                                      |
| [**Scroll**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Gibt möglicherweise \_ den Wert S false ohne Aktion zurück.<br/>           |
| [**Verwerfen von dostate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Kann S \_ OK ohne Aktion zurückgeben.<br/>              |
| [**"Deaktiviert"**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | Die Aktivierung ist obligatorisch. Rückgängigmachen ist optional. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Methode                                                                          | Kommentare                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getextendebug-Steuerelement**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Erforderlich für Container, die erweiterte Steuerelemente unterstützen.<br/>                                                                                                 |
| [**Showpropertyframe**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Erforderlich für Container, die eigene Eigenschaften Seiten einschließen möchten, um erweiterte Steuerelement Eigenschaften zusätzlich zu den von einem Steuerelement bereitgestellten Eigenschaften zu verarbeiten.<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Gibt möglicherweise \_ den Wert S false ohne Aktion zurück.<br/>                                                                                                                      |
| [**Lockinplaceactive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Optional<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (Ambient-Eigenschaften)



| Methode                      | Kommentare                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| Gettypeingefocount<br/> | Erforderlich für Container, die nicht standardmäßige Ambient-Eigenschaften unterstützen.<br/> |
| GetTypeInfo<br/>      | Erforderlich für Container, die nicht standardmäßige Ambient-Eigenschaften unterstützen.<br/> |
| GetIDsOfNames<br/>    | Erforderlich für Container, die nicht standardmäßige Ambient-Eigenschaften unterstützen.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (Ereignis Senke)



| Methode                      | Kommentare                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| Gettypeingefocount<br/> | Das Steuerelement kennt seine eigenen Typinformationen, sodass es nicht aufgerufen werden muss.<br/> |
| GetTypeInfo<br/>      | Das Steuerelement kennt seine eigenen Typinformationen, sodass es nicht aufgerufen werden muss.<br/> |
| GetIDsOfNames<br/>    | Das Steuerelement kennt seine eigenen Typinformationen, sodass es nicht aufgerufen werden muss.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Methode                                                                           | Kommentare                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Erforderlich für Container mit der Symbolleisten-Benutzeroberfläche (optional)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Erforderlich für Container mit der Symbolleisten-Benutzeroberfläche (optional)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Erforderlich für Container mit der Symbolleisten-Benutzeroberfläche (optional)<br/> |
| [**Insertmenüs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Erforderlich für Container mit Menü Benutzeroberfläche (optional)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Erforderlich für Container mit Menü Benutzeroberfläche (optional)<br/>    |
| [**Removemenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Erforderlich für Container mit Menü Benutzeroberfläche (optional)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Nur für Container mit einer Statuszeile erforderlich<br/>        |
| [**Enablemodeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Optional<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Optional<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Methode                                                                    | Kommentare                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name des Parametern**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Nur, wenn das Verknüpfen mit Steuerelementen oder anderen Einbettungen im Container unterstützt wird, da dies für die Monikerbindung erforderlich ist.<br/>                                                                                                                  |
| [**Lockcontainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Wie für "Parser Name"<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Gibt alle ActiveX-Steuerelemente durch einen Enumerator mit [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)zurück, jedoch nicht notwendigerweise alle-Objekte (da es keine Garantie gibt, dass alle Objekte ActiveX-Steuerelemente sind; einige können reguläre Windows-Steuerelemente sein).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

