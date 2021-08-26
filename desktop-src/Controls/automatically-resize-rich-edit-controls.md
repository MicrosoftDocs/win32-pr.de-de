---
title: Automatisches Ändern der Größe von Rich Edit-Steuerelementen
description: Eine Anwendung kann die Größe eines Rich-Edit-Steuerelements nach Bedarf ändern, sodass es immer die gleiche Größe wie der Inhalt hat.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef3fa798da0a7747464d42535c638f437154124dd76b0324add35b5ba01931a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921720"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Automatisches Ändern der Größe von Rich Edit-Steuerelementen

Eine Anwendung kann die Größe eines Rich-Edit-Steuerelements nach Bedarf ändern, sodass es immer die gleiche Größe wie der Inhalt hat. Ein umfassendes Bearbeitungssteuer steuerelement unterstützt diese so genannte *bottomless-Funktionalität,* indem es dem übergeordneten Fenster einen [EN \_ REQUESTRESIZE-Benachrichtigungscode](en-requestresize.md) sendet, wenn sich die Größe des Inhalts des Steuerelements ändert.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="automatically-resize-a-rich-edit-control"></a>Automatisches Ändern der Größe eines Rich Edit-Steuerelements

Beim Verarbeiten des [EN \_ REQUESTRESIZE-Benachrichtigungscodes](en-requestresize.md) sollte eine Anwendung die Größe des Steuerelements auf die Dimensionen in der angegebenen [**REQRESIZE-Struktur**](/windows/desktop/api/Richedit/ns-richedit-reqresize) ändern. Eine Anwendung kann auch alle Informationen verschieben, die sich in der Nähe des Steuerelements befindet, um die Änderung der Höhe des Steuerelements zu erreichen. Um die Größe des Steuerelements zu ändern, können Sie die [**SetWindowPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) verwenden.

Sie können mithilfe der [**EM \_ REQUESTRESIZE-Nachricht**](em-requestresize.md) erzwingen, dass ein bottomless Rich Edit-Steuerelement einen [EN \_ REQUESTRESIZE-Benachrichtigungscode](en-requestresize.md) sendet. Diese Meldung kann nützlich sein, wenn die [**WM \_ SIZE-Nachricht verarbeitet**](/windows/desktop/winmsg/wm-size) wird.

## <a name="remarks"></a>Hinweise

Um [EN \_ REQUESTRESIZE-Benachrichtigungscodes](en-requestresize.md) zu erhalten, müssen Sie die Benachrichtigung mithilfe der [EM \_ SETEVENTMASK-Nachricht](em-seteventmask.md) aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 