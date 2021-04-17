---
description: Erläutert, wie ein mathematisches Eingabe Steuerelement erstellt wird.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Erstellen eines mathematischen Eingabe Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549931"
---
# <a name="creating-a-math-input-control"></a><span data-ttu-id="b4e5b-103">Erstellen eines mathematischen Eingabe Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="b4e5b-103">Creating a Math Input Control</span></span>

<span data-ttu-id="b4e5b-104">Um das mathematische Eingabe Steuerelement zu erstellen, müssen Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="b4e5b-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="b4e5b-105">Einschließen von Headern und Bibliotheken für das mathematische Eingabe Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b4e5b-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="b4e5b-106">Deklarieren Sie den Steuerelement Zeiger, und rufen Sie CoInitialize im Steuerelement Zeiger auf</span><span class="sxs-lookup"><span data-stu-id="b4e5b-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="b4e5b-107">Steuerelement anzeigen</span><span class="sxs-lookup"><span data-stu-id="b4e5b-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="b4e5b-108">Einschließen von Headern und Bibliotheken für das mathematische Eingabe Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b4e5b-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="b4e5b-109">Der folgende Code sollte am Anfang des Codes platziert werden, in dem Sie das mathematische Eingabe Steuerelement verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="b4e5b-110">Mit diesem Code wird der Anwendung Unterstützung für das mathematische Eingabe Steuerelement hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="b4e5b-111">Deklarieren Sie den Steuerelement Zeiger, und rufen Sie CoInitialize im Steuerelement Zeiger auf</span><span class="sxs-lookup"><span data-stu-id="b4e5b-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="b4e5b-112">Nachdem Sie die Header für das-Steuerelement eingefügt haben, können Sie den Steuerelement Zeiger deklarieren und CoInitialize darauf abrufen, um ein Handle für die mathematische Eingabe Steuerungs Schnittstelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="b4e5b-113">Der folgende Code kann in einer Klasse oder als globale Variable in der Implementierung der Anwendung platziert werden:</span><span class="sxs-lookup"><span data-stu-id="b4e5b-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="b4e5b-114">Der folgende Code zeigt, wie Sie CoInitialize auf dem Steuerelement Zeiger abrufen können.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="b4e5b-115">Nach dem Aufrufen von CoInitialize für den Steuerelement Zeiger verfügen Sie über einen Verweis auf das Steuerelement und können auf die Methoden des Steuer Elements zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="b4e5b-116">Beispielsweise können Sie den erweiterten Satz von Steuerelementen aktivieren, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="b4e5b-117">Steuerelement anzeigen</span><span class="sxs-lookup"><span data-stu-id="b4e5b-117">Show the Control</span></span>

<span data-ttu-id="b4e5b-118">Das Steuerelement wird nach der Erstellung nicht automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="b4e5b-119">Um das Steuerelement anzuzeigen, nennen Sie die [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) -Methode für den Steuerelement Verweis, den Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="b4e5b-120">Der folgende Code veranschaulicht, wie die [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) -Methode aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="b4e5b-121">Nachdem das Steuerelement angezeigt wird, sieht es in etwa wie in der folgenden Abbildung aus.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-121">After the control shows, it will look something like the following illustration.</span></span>

![Screenshot mit mathematischer Eingabesteuerung](images/mic.png)

<span data-ttu-id="b4e5b-123">Beachten Sie, dass der erweiterte Satz von Schaltflächen aktiviert ist, sodass wieder **holen** und **Rückgängig** gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
