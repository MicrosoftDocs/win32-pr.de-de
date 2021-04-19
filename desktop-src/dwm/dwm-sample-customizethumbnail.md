---
title: Anpassen eines Miniaturansichtsymbols und einer Bitmap für die Livevorschau
description: Zeigt, wie Sie eine Miniaturansicht und eine Live Vorschau-Bitmap (auch als Peek Preview bezeichnet) anpassen können.
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106364022"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>Anpassen eines Miniaturansichtsymbols und einer Bitmap für die Livevorschau

## <a name="description"></a>BESCHREIBUNG

Sie können eine Miniaturansicht und eine *Live Vorschau* (oder *Peek Preview*)-Bitmap mithilfe von Funktionen und Nachrichten anpassen, die in den Windows 7-Desktopfenster-Manager-APIs (DWM) eingeführt werden.

Insbesondere verwenden Sie die Funktion " [**dwmstisubicminiatur**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) " und die " [**WM \_ sendianicthumbnailbitmap**](wm-dwmsendiconicthumbnail.md) "-Meldung, um eine Miniaturansicht anzupassen. Sie können auch die [**dwmseticoniclivepreviewbitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) -Funktion und die [**WM- \_ sendiconiclivepreviewbitmap**](wm-dwmsendiconiclivepreviewbitmap.md) -Nachricht verwenden, um eine legendäre Live Vorschau-Bitmap festzulegen.

Eine Beispielanwendung, die die Funktion " **dwmseticonfiguration** " verwendet, finden Sie unter [Beispiel für tabminiatur Ansichten](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).

Die folgende Abbildung zeigt eine in eine angepasste Miniaturansicht transformierte Standard Miniaturansicht.

![Abbildung eines ursprünglichen Miniatur Bilds und eines geänderten Miniatur Bilds mit einer benutzerdefinierten Bitmap](images/customthumbnail.jpg)

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Platt Form Update für Windows Vista                          |
| Unterstützte Mindestversion (Server) | Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Platt Form Update für Windows Server 2008 |
| Minimale Windows SDK      | [Windows Software Development Kit (SDK) für Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>Aufbauen des tabthumbnails-Beispiels

**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugte Methode)**

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zu dem Ordner, in dem sich die Datei "tabthumbnails. sln" befindet.
2.  Doppelklicken Sie auf die Projektmappendatei (. sln), um die Datei in Microsoft Visual Studio zu öffnen.
3.  Klicken Sie im Menü **Erstellen** auf **Projektmappe erstellen**. Die Anwendung wird im standardmäßigen \\ Debug-oder \\ releaseverzeichnis erstellt.

**So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung**

1.  Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zum Beispiel Verzeichnis.
2.  Geben Sie `msbuild TabThumbnails.sln` ein.

## <a name="related-topics"></a>Zugehörige Themen

[Desktopfenster-Manager](dwm-overview.md)

[Windows-Entwicklung](/windows/desktop/win32-and-com-development)
