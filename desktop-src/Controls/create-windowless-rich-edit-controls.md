---
title: Bereitstellen von fensterlosen Bearbeitungs Steuerelementen mit Fenster Funktionen
description: Die Fenster Funktionalität umfasst die Möglichkeit, Nachrichten zu empfangen, und den Besitz eines Geräte Kontexts, in den gezeichnet werden soll. Fensterlose Rich Edit-Steuerelemente erhalten diese Funktionalität über ein paar von Schnittstellen itextservices und itexthost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103948527"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="ba912-104">Bereitstellen von fensterlosen Bearbeitungs Steuerelementen mit Fenster Funktionen</span><span class="sxs-lookup"><span data-stu-id="ba912-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="ba912-105">Die Fenster Funktionalität umfasst die Möglichkeit, Nachrichten zu empfangen, und den Besitz eines Geräte Kontexts, in den gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba912-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="ba912-106">Fensterlose Rich Edit-Steuerelemente erhalten diese Funktionalität über ein paar von Schnittstellen: [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="ba912-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ba912-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="ba912-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ba912-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="ba912-108">Technologies</span></span>

-   [<span data-ttu-id="ba912-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="ba912-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ba912-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ba912-110">Prerequisites</span></span>

-   <span data-ttu-id="ba912-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ba912-111">C/C++</span></span>
-   <span data-ttu-id="ba912-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="ba912-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ba912-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="ba912-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="ba912-114">Einrichten der Fenster Funktionalität</span><span class="sxs-lookup"><span data-stu-id="ba912-114">Establish the Window Functionality</span></span>

<span data-ttu-id="ba912-115">Im folgenden Beispielcode wird veranschaulicht, wie der texthost und die Text Dienste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba912-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="ba912-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba912-116">Remarks</span></span>

<span data-ttu-id="ba912-117">Der *hthchechedit* -Parameter im Codebeispiel ist ein Handle für das Msftedit.dll Modul, und es wird davon ausgegangen, dass dieses Handle bereits durch einen Aufrufen der **GetModuleHandle** -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ba912-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="ba912-118">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="ba912-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba912-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba912-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba912-120">Verwenden von fensterlosen Rich-Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="ba912-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="ba912-121">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="ba912-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ba912-122">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ba912-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




