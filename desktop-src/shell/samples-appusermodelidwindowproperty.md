---
description: Veranschaulicht, wie das Verhalten der Task leisten Gruppierung der Fenster einer Anwendung über die System.AppUserModel.ID-Eigenschaft gesteuert wird.
title: Fenstereigenschaft „Anwendungsbenutzermodell-ID“ (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980344"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Beispiel für eine Anwendungs Benutzer Modell-ID (AppID) Window-Eigenschaft

Veranschaulicht, wie das Verhalten der Task leisten Gruppierung der Fenster einer Anwendung über die [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft gesteuert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

Dieses Beispiel zeigt, wie die [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft mithilfe der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Implementierung des Fensters festgelegt wird, die über [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)abgerufen wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Appusermudelidwindowproperty-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **appusermudelidwindowproperty** .
2.  Geben Sie `msbuild AppUserModelIDWindowProperty.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **appusermudelidwindowproperty** ".
2.  Doppelklicken Sie auf das Symbol für die Datei appusermudelidwindowproperty. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `AppUserModelIDWindowProperty.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für AppUserModelIDWindowProperty.exe doppelklicken.
3.  Um zu veranschaulichen, wie sich die App-Benutzer Modell-IDs (appusermudelids) auf die Task leisten Gruppierung auswirken, starten Sie mindestens drei Instanzen der Anwendung gleichzeitig.
4.  Verwenden Sie das Menü, um für jedes der drei Fenster eine andere appusermodelid festzulegen. Beachten Sie, dass jede separate appusermodelid zu einer separaten Task leisten Schaltfläche führt und dass Windows Ihre Identität zur Laufzeit ändern kann.
5.  Legen Sie mindestens zwei Fenster auf die zweite appusermodelid fest. Beachten Sie, dass beide in dieselbe Task leisten Gruppe verschoben werden.
6.  Öffnen Sie das Fenster **Taskleiste und Start Menü Eigenschaften** , indem Sie mit der rechten Maustaste auf die Taskleiste klicken und im Kontextmenü **Eigenschaften** auswählen. Ändern der **Task** leisten Schaltflächen: Dropdown zwischen der **Kombination, wenn die Taskleiste voll ist** und **nie Werte kombinieren** . Beachten Sie, dass jedes Fenster eine separate Schaltfläche erhalten kann, dass die Schaltflächen jedoch nach appusermodelid gruppiert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](appids.md)
</dt> </dl>

 

 
