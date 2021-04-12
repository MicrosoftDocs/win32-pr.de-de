---
title: Dynamisches bezeichnen von Symbolleisten-Schaltflächen
description: Mithilfe der TB-SetButtonInfo-Meldung können Sie einer vorhandenen Schaltfläche Text zuweisen \_ .
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472428"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Dynamisches bezeichnen von Symbolleisten-Schaltflächen

Mithilfe der [**TB- \_ SetButtonInfo**](tb-setbuttoninfo.md) -Meldung können Sie einer vorhandenen Schaltfläche Text zuweisen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="dynamically-label-a-toolbar-button"></a>Dynamisches bezeichnen einer Symbolleisten-Schaltfläche

Im folgenden Beispiel wird veranschaulicht, wie Sie den Text der dritten Schaltfläche in den vorherigen Beispielen von " **Speichern** " in " **Speichern** unter" ändern.


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>Bemerkungen

Wenn Sie den Text einer Schaltfläche mithilfe von [**TB \_ SetButtonInfo**](tb-setbuttoninfo.md) ändern, wirkt sich dies nicht auf die Zeichenfolge aus, die dieser Schaltfläche in der internen Zeichen folgen Liste zugewiesen wird.

Wenn Sie der internen Textliste eine Symbolleisten-Schaltflächen Zeichenfolge hinzufügen, können Sie den Index dieser Zeichenfolge nicht abrufen, indem Sie [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md)aufrufen – Sie müssen stattdessen die [**TB \_ getbutton**](tb-getbutton.md) -Nachricht verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleisten](using-toolbar-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




