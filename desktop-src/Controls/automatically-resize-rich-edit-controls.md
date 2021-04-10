---
title: Automatisches Ändern der Größe von Rich-Edit-Steuerelementen
description: Eine Anwendung kann die Größe eines Rich-Edit-Steuer Elements nach Bedarf ändern, sodass es immer dieselbe Größe wie der Inhalt hat.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039698"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Automatisches Ändern der Größe von Rich-Edit-Steuerelementen

Eine Anwendung kann die Größe eines Rich-Edit-Steuer Elements nach Bedarf ändern, sodass es immer dieselbe Größe wie der Inhalt hat. Ein RichEdit-Steuerelement unterstützt diese so genannte, nicht *aufgerufene Funktion* , indem es das übergeordnete Fenster an den e-How-Wert der Datei " [ \_ RequestResize](en-requestresize.md) " sendet.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="automatically-resize-a-rich-edit-control"></a>Automatisches Ändern der Größe eines Rich-Edit-Steuer Elements

Bei der Verarbeitung des Benachrichtigungs Codes " [en \_ RequestResize](en-requestresize.md) " sollte eine Anwendung die Größe des Steuer Elements auf die Dimensionen in der angegebenen [**reqresize**](/windows/desktop/api/Richedit/ns-richedit-reqresize) -Struktur ändern. Eine Anwendung kann auch alle Informationen verschieben, die sich in der Nähe des Steuer Elements befinden, um die Änderung der Höhe des Steuer Elements zu ermöglichen. Um die Größe des Steuer Elements zu ändern, können Sie die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion verwenden.

Sie können ein nicht gesteuerloses Bearbeitungs Steuerelement erzwingen, um einen [en \_ RequestResize](en-requestresize.md) -Benachrichtigungs Code mithilfe der [**EM \_ RequestResize**](em-requestresize.md) -Nachricht zu senden. Diese Meldung kann nützlich sein, wenn die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verarbeitet wird.

## <a name="remarks"></a>Bemerkungen

Zum Empfangen von [en \_ RequestResize](en-requestresize.md) -Benachrichtigungs Codes müssen Sie die Benachrichtigung mithilfe der Nachricht [EM \_ SetEventMask](em-seteventmask.md) aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 