---
description: In diesem Thema werden die verschiedenen Möglichkeiten zum Instanziieren eines InkEdit-Steuerelements beschrieben.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Instanziieren von InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53df76fea92077e2d1dbfaea57213ad95cdccf91a4b40267cec02e28b887b984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032018"
---
# <a name="instantiating-inkedit"></a>Instanziieren von InkEdit

In diesem Thema werden die verschiedenen Möglichkeiten zum Instanziieren eines [InkEdit-Steuerelements](inkedit-control.md) beschrieben.

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET und C\#

Wenn Sie mit Microsoft Visual Basic .NET oder C arbeiten, ziehen Sie das \# [InkEdit-Steuerelement](./inkedit-control.md) aus der Toolbox in Visual Studio in das Formular oder die Seite, in dem das Steuerelement angezeigt werden soll.

## <a name="win32c"></a>Win32/C++

Das [InkEdit-Steuerelement](inkedit-control-reference.md) ist eine Oberklasse des einbettbaren Rich Edit 4.5 Win32 OLE-Steuerelements.

Win32-Anwendungen instanziieren das [InkEdit-Steuerelement,](inkedit-control-reference.md) indem sie [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) aufrufen und INKEDIT als Fensterklasse übergeben. INKEDIT ist in InkEd.h definiert. Nachdem das Steuerelement erstellt wurde, können Sie mit Nachrichten mit dem Steuerelement "sprechen". Rich Edit-Nachrichten (EM) werden unverändert von InkEdit an Rich Edit übergeben. Alle vorhandenen \_ \* Rich Edit-Funktionen sind verfügbar.

Um ein [InkEdit-Steuerelement](inkedit-control-reference.md) zu erstellen, rufen Sie die [CreateWindow()-Funktion](/windows/win32/api/winuser/nf-winuser-createwindowa) unter Angabe der InkEdit-Fensterklasse auf. Verwenden [Sie LoadLibrary() zum](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Registrieren InkEd.dll. Geben Sie die definierte Konstante INKEDIT CLASS für den Window Class-Parameter an, und verwenden Sie die Fensterstile, wie \_ in den folgenden Beispielen angegeben.

### <a name="instantiating-a-multiline-inkedit-control"></a>Instanziieren eines mehrstufigen InkEdit-Steuerelements


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a>Instanziieren eines Single-Line InkEdit-Steuerelements


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> Im Gegensatz zu RichEdit müssen Sie vor dem Erstellen des [InkEdit-Steuerelements](inkedit-control-reference.md) [unbedingt CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) aufrufen. Rufen [Sie CoUninitialize() auf,](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) wenn Ihre Anwendung heruntergefahren wird. Nach dem Aufruf von CoUninitialize() müssen Sie [FreeLibrary(s \_ hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) aufrufen, um die Verweisanzahl für die InkEdit.dll zu dekrementieren.

 

Wenn Sie den [ES \_ NOIME-Fensterstil](../controls/rich-edit-control-styles.md) verwenden, ist die integrierte Korrekturunterstützung nicht verfügbar. Wenn Sie kein übergeordnetes Fenster angeben, wird das Steuerelement als Fenster der obersten Ebene erstellt, und der WS-SYSMENU-Stil wird hinzugefügt. Dadurch wird auch die integrierte Korrekturunterstützung \_ deaktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von Ink-Steuerelementen zu Project](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
