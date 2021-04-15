---
description: In diesem Thema werden die verschiedenen Methoden beschrieben, mit denen Sie ein InkEdit-Steuerelement instanziieren können.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Instanziieren von InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485195"
---
# <a name="instantiating-inkedit"></a>Instanziieren von InkEdit

In diesem Thema werden die verschiedenen Methoden beschrieben, mit denen Sie ein [InkEdit](inkedit-control.md) -Steuerelement instanziieren können.

## <a name="visual-basic-net-and-c"></a>Visual Basic .net und C\#

Wenn Sie mit Microsoft Visual Basic .net oder C arbeiten \# , ziehen Sie das [InkEdit](./inkedit-control.md) -Steuerelement aus der Toolbox in Visual Studio in das Formular oder die Seite, auf dem das Steuerelement angezeigt werden soll.

## <a name="win32c"></a>Win32/C++

Das [InkEdit](inkedit-control-reference.md) -Steuerelement ist eine übergeordnete Klasse des Rich Edit 4,5 Win32 OLE einbettbaren Steuer Elements.

Win32-Anwendungen instanziieren das [InkEdit](inkedit-control-reference.md) -Steuerelement durch Aufrufen von [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) und übergeben von InkEdit als Fenster Klasse. InkEdit ist in ". h" definiert. Nachdem das Steuerelement erstellt wurde, können Sie mit Nachrichten mit dem Steuerelement kommunizieren. Rich Edit Messages (EM \_ \* ) werden von InkEdit an eine umfangreiche Bearbeitung ohne Änderung übermittelt. alle vorhandenen Funktionen der funktionsreichen Bearbeitung sind verfügbar.

Zum Erstellen eines [InkEdit](inkedit-control-reference.md) -Steuer Elements rufen Sie die Funktion "up [Window ()](/windows/win32/api/winuser/nf-winuser-createwindowa) " auf, und geben Sie dabei die Fenster Klasse "InkEdit" an Verwenden Sie [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , um InkEd.dll zu registrieren. Geben Sie die \_ für den Window Class-Parameter definierte Konstante "InkEdit Class" an, und verwenden Sie die in den folgenden Beispielen angegebenen Fenster Stile.

### <a name="instantiating-a-multiline-inkedit-control"></a>Instanziieren eines mehrzeiligen InkEdit-Steuer Elements


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



### <a name="instantiating-a-single-line-inkedit-control"></a>Instanziieren eines Single-Line InkEdit-Steuer Elements


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
> Anders als bei RichEdit müssen Sie sicherstellen, dass [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) aufgerufen wird, bevor das [InkEdit](inkedit-control-reference.md) -Steuerelement erstellt wird. Wenden [Sie](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) sich an, wenn die Anwendung heruntergefahren wird. Nach dem Aufruf von "zählinitialize ()" müssen Sie " [FreeLibrary (s \_ Hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) " aufrufen, um den Verweis Zähler für die InkEdit.dll Datei zu verringern.

 

Wenn Sie den Stil des [es- \_ noime](../controls/rich-edit-control-styles.md) -Fensters verwenden, ist die integrierte Korrektur Unterstützung nicht verfügbar. Wenn Sie kein übergeordnetes Fenster angeben, wird das Steuerelement als Fenster der obersten Ebene erstellt, und der WS \_ sysmenu-Stil wird hinzugefügt. Dadurch wird auch die integrierte Korrektur Unterstützung deaktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von Ink-Steuerelementen zu einem Projekt](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
