---
description: Veranschaulicht das Schreiben eines Handlers, der zum Anzeigen einer Datei Vorschau innerhalb des Vorschau Bereichs von Windows-Explorer oder anderen Vorschau handlerhosts verwendet wird.
title: Rezept-Vorschauhandler (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980248"
---
# <a name="recipe-preview-handler-sample"></a>Rezept-Vorschauhandler (Beispiel)

Veranschaulicht das Schreiben eines Handlers, der zum Anzeigen einer Datei Vorschau innerhalb des Vorschau Bereichs von Windows-Explorer oder anderen Vorschau handlerhosts verwendet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Aufheben der Registrierung der Beispiel-Vorschau Handler-dll](#unregistering-the-sample-preview-handler-dll)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Beispiel für "recipeer PreviewHandler"](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis " **recipeer PreviewHandler** ". Beispiel: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.
2.  Geben Sie `msbuild PreviewHandlerSDKSample.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **recipeer PreviewHandler** ".
2.  Doppelklicken Sie auf das Symbol für die Datei previewhandlersdksample. sln, um das Projekt in Visual Studio zu öffnen.
    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

> [!Note]  
> Wenn das Zielsystem 64-Bit (x64) ist, muss dieser Beispiel-Vorschau Handler als 64-Bit-Anwendung erstellt werden.

 

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum erstellten Projektverzeichnis " **recipeer PreviewHandler** ". Beispiel: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`. Geben Sie ein `regsvr32.exe PreviewHandlerSDKSample.dll` , um den Handler zu registrieren.
2.  Öffnen Sie Windows-Explorer, und zeigen Sie den Vorschaubereich an, wenn er nicht bereits angezeigt wird.
    -   **Windows 7**: Klicken Sie auf die Schaltfläche Vorschaubereich.
    -   **Windows Vista**: Klicken Sie auf das Menü **organisieren** , wechseln Sie zum Untermenü **Layout** , und wählen Sie **Vorschau** Bereich aus.
3.  Navigieren Sie in Windows-Explorer zum Projektverzeichnis " **recipeer PreviewHandler** ".
4.  Wählen Sie die Datei "example. Rezept" aus.

Legen Sie den **AppID** -Wert `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` wie im folgenden Code gezeigt auf den WOW64-Ersatz Zeichen Host fest, damit sowohl die 32-Bit (x86)-als auch die 64-Bit (x64)-Ausgabe in einer 64-Bit-Version von Windows funktioniert.


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>Aufheben der Registrierung der Beispiel-Vorschau Handler-dll

-   Öffnen Sie die Eingabeaufforderung, und geben Sie ein `regsvr32.exe /u PreviewHandlerSDKSample.dll` , um die Registrierung des Handlers aufzuheben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](appids.md)
</dt> </dl>

 

 
