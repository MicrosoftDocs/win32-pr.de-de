---
description: Veranschaulicht, wie das Gruppierungsverhalten der Taskleistenfenster einer Anwendung über die -Eigenschaft System.AppUserModel.ID wird.
title: Fenstereigenschaft „Anwendungsbenutzermodell-ID“ (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a6a4b0daca8b6bd4147c1e36d921b58b3802d975e678e49a9b9153761e61820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219880"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Application User Model ID (AppID) Window Property Sample

Veranschaulicht, wie das Gruppierungsverhalten der Taskleistenfenster einer Anwendung über die -Eigenschaft System.AppUserModel.ID [wird.](../properties/props-system-appusermodel-id.md)

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel wird gezeigt, wie die [System.AppUserModel.ID-Eigenschaft](../properties/props-system-appusermodel-id.md) mithilfe der [**IPropertyStore-Implementierung**](/windows/win32/api/propsys/nn-propsys-ipropertystore) des Fensters festgelegt wird, die über [**SHGetPropertyStoreForWindow ermittelt wird.**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [AppUserModelIDWindowProperty-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis AppUserModelIDWindowProperty.**
2.  Geben Sie `msbuild AppUserModelIDWindowProperty.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis AppUserModelIDWindowProperty.**
2.  Doppelklicken Sie auf das Symbol für die Datei AppUserModelIDWindowProperty.sln, um das Projekt in Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue ausführbare Windows enthält.
2.  Geben Sie in der Befehlszeile `AppUserModelIDWindowProperty.exe` ein. Doppelklicken Sie alternativ Windows Explorer auf das Symbol für AppUserModelIDWindowProperty.exe.
3.  Um die Auswirkungen von Anwendungsbenutzermodell-IDs (AppUserModelIDs) auf die Taskleistengruppe zu veranschaulichen, starten Sie mindestens drei Instanzen der Anwendung gleichzeitig.
4.  Verwenden Sie das Menü, um in jedem der drei Fenster eine andere AppUserModelID festlegen. Beachten Sie, dass jede separate AppUserModelID zu einer separaten Taskleistenschaltfläche führt und dass Fenster ihre Identität zur Laufzeit ändern können.
5.  Legen Sie mindestens zwei Fenster auf die zweite AppUserModelID fest. Beachten Sie, dass beide in dieselbe Taskleistengruppe wechseln.
6.  Öffnen Sie **das Eigenschaftenfenster Taskleiste** und Startmenü, indem Sie mit der rechten Maustaste auf die Taskleiste klicken und eigenschaften **im** Kontextmenü auswählen. Ändern Sie **die Schaltflächen taskbar:** in der Dropdownliste zwischen der Dropdownliste Kombinieren, **wenn die Taskleiste** voll ist, und Der Wert wird nie **kombiniert.** Beachten Sie, dass jedes Fenster eine separate Schaltfläche erhalten kann, die Schaltflächen jedoch nach AppUserModelID gruppiert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsbenutzermodell-IDs (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
