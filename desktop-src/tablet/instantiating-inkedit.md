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
# <a name="instantiating-inkedit"></a><span data-ttu-id="64982-103">Instanziieren von InkEdit</span><span class="sxs-lookup"><span data-stu-id="64982-103">Instantiating InkEdit</span></span>

<span data-ttu-id="64982-104">In diesem Thema werden die verschiedenen Methoden beschrieben, mit denen Sie ein [InkEdit](inkedit-control.md) -Steuerelement instanziieren können.</span><span class="sxs-lookup"><span data-stu-id="64982-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="64982-105">Visual Basic .net und C\#</span><span class="sxs-lookup"><span data-stu-id="64982-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="64982-106">Wenn Sie mit Microsoft Visual Basic .net oder C arbeiten \# , ziehen Sie das [InkEdit](./inkedit-control.md) -Steuerelement aus der Toolbox in Visual Studio in das Formular oder die Seite, auf dem das Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64982-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="64982-107">Win32/C++</span><span class="sxs-lookup"><span data-stu-id="64982-107">Win32/C++</span></span>

<span data-ttu-id="64982-108">Das [InkEdit](inkedit-control-reference.md) -Steuerelement ist eine übergeordnete Klasse des Rich Edit 4,5 Win32 OLE einbettbaren Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="64982-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="64982-109">Win32-Anwendungen instanziieren das [InkEdit](inkedit-control-reference.md) -Steuerelement durch Aufrufen von [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) und übergeben von InkEdit als Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="64982-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="64982-110">InkEdit ist in ". h" definiert.</span><span class="sxs-lookup"><span data-stu-id="64982-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="64982-111">Nachdem das Steuerelement erstellt wurde, können Sie mit Nachrichten mit dem Steuerelement kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="64982-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="64982-112">Rich Edit Messages (EM \_ \* ) werden von InkEdit an eine umfangreiche Bearbeitung ohne Änderung übermittelt. alle vorhandenen Funktionen der funktionsreichen Bearbeitung sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64982-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="64982-113">Zum Erstellen eines [InkEdit](inkedit-control-reference.md) -Steuer Elements rufen Sie die Funktion "up [Window ()](/windows/win32/api/winuser/nf-winuser-createwindowa) " auf, und geben Sie dabei die Fenster Klasse "InkEdit" an</span><span class="sxs-lookup"><span data-stu-id="64982-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="64982-114">Verwenden Sie [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , um InkEd.dll zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="64982-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="64982-115">Geben Sie die \_ für den Window Class-Parameter definierte Konstante "InkEdit Class" an, und verwenden Sie die in den folgenden Beispielen angegebenen Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="64982-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="64982-116">Instanziieren eines mehrzeiligen InkEdit-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="64982-116">Instantiating a Multiline InkEdit Control</span></span>


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



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="64982-117">Instanziieren eines Single-Line InkEdit-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="64982-117">Instantiating a Single-Line InkEdit Control</span></span>


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
> <span data-ttu-id="64982-118">Anders als bei RichEdit müssen Sie sicherstellen, dass [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) aufgerufen wird, bevor das [InkEdit](inkedit-control-reference.md) -Steuerelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="64982-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="64982-119">Wenden [Sie](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) sich an, wenn die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="64982-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="64982-120">Nach dem Aufruf von "zählinitialize ()" müssen Sie " [FreeLibrary (s \_ Hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) " aufrufen, um den Verweis Zähler für die InkEdit.dll Datei zu verringern.</span><span class="sxs-lookup"><span data-stu-id="64982-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="64982-121">Wenn Sie den Stil des [es- \_ noime](../controls/rich-edit-control-styles.md) -Fensters verwenden, ist die integrierte Korrektur Unterstützung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64982-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="64982-122">Wenn Sie kein übergeordnetes Fenster angeben, wird das Steuerelement als Fenster der obersten Ebene erstellt, und der WS \_ sysmenu-Stil wird hinzugefügt. Dadurch wird auch die integrierte Korrektur Unterstützung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="64982-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64982-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64982-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64982-124">Hinzufügen von Ink-Steuerelementen zu einem Projekt</span><span class="sxs-lookup"><span data-stu-id="64982-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
