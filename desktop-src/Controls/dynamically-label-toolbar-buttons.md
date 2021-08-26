---
title: Dynamisches Bezeichnen von Symbolleistenschaltflächen
description: Sie können einer vorhandenen Schaltfläche Text zuweisen, indem Sie die TB \_ SETBUTTONINFO-Meldung verwenden.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877440"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Dynamisches Bezeichnen von Symbolleistenschaltflächen

Sie können einer vorhandenen Schaltfläche Text zuweisen, indem Sie die [**TB \_ SETBUTTONINFO-Meldung**](tb-setbuttoninfo.md) verwenden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="dynamically-label-a-toolbar-button"></a>Dynamisches Bezeichnen einer Symbolleistenschaltfläche

Im folgenden Beispiel wird veranschaulicht, wie der Text der dritten Schaltfläche in den vorherigen Beispielen von **Speichern** in Speichern unter geändert **wird.**


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



## <a name="remarks"></a>Hinweise

Das Ändern des Texts einer Schaltfläche mitHILFE von [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) wirkt sich nicht auf die Zeichenfolge aus, die dieser Schaltfläche in der internen Zeichenfolgenliste zugewiesen ist.

Wenn Sie der internen Textliste eine Symbolleisten-Schaltflächenzeichenfolge hinzufügen, können Sie den Index dieser Zeichenfolge nicht abrufen, indem Sie [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)aufrufen. Sie müssen stattdessen die [**TB \_ GETBUTTON-Nachricht**](tb-getbutton.md) verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleistensteuerelementen](using-toolbar-controls.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




