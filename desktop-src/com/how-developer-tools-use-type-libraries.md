---
title: Verwendung von Typbibliotheken in Entwicklertools
description: Verwendung von Typbibliotheken in Entwicklertools
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106349751"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="be8f6-103">Verwendung von Typbibliotheken in Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="be8f6-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="be8f6-104">Im folgenden Diagramm wird veranschaulicht, wie die verschiedenen Entwicklungs Tools mit der Typbibliothek eines COM-Objekts interagieren.</span><span class="sxs-lookup"><span data-stu-id="be8f6-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="be8f6-105">Jede Typbibliothek stellt standardmäßige programmgesteuerte Schnittstellen zur Verfügung, die von Tools aufgerufen werden können, um Informationen zu den in dieser Typbibliothek beschriebenen Elementen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="be8f6-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="be8f6-106">In diesem Diagramm steht GUID für Globally Unique Identifier und RPC für Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="be8f6-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![Diagramm, das zeigt, wie das Entwicklungs Objekt mit der Typbibliothek eines C O M-Objekts interagiert.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="be8f6-108">Im vorangehenden Diagramm generieren die C++-Konvertierungs Tools, wie z. b. der mittlerer l-Compiler und die vom Microsoft Visual C++ Entwicklungssystem bereitgestellten Assistenten, Header-und Stubdateien.</span><span class="sxs-lookup"><span data-stu-id="be8f6-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="be8f6-109">Sie können diese Dateien dem Projekt hinzufügen, um das COM-Objekt zu verwenden, das von der Typbibliothek beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="be8f6-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="be8f6-110">Ebenso generieren die Entwicklertools in Java Java-Klassen-und Quelldateien, die Sie dann in Ihre Anwendung importieren können.</span><span class="sxs-lookup"><span data-stu-id="be8f6-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="be8f6-111">In Visual Basic ist das Szenario etwas einfacher.</span><span class="sxs-lookup"><span data-stu-id="be8f6-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="be8f6-112">Sie müssen keine zusätzlichen Dateien generieren.</span><span class="sxs-lookup"><span data-stu-id="be8f6-112">You do not need to generate additional files.</span></span> <span data-ttu-id="be8f6-113">Die Visual Basic Umgebung enthält Dialogfelder, in denen die aktuell auf dem Computer installierten COM-Objekte aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="be8f6-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="be8f6-114">Sie wählen die Komponente aus, die Sie aus der Anwendung abrufen möchten, und Sie wird dem Projekt hinzugefügt, entweder als Komponente oder als Verweis.</span><span class="sxs-lookup"><span data-stu-id="be8f6-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="be8f6-115">Der OLE-com-Viewer liest eine Typbibliothek, generiert eine temporäre IDL-Datei auf Grundlage der Typbibliothek und zeigt Sie Benutzern an.</span><span class="sxs-lookup"><span data-stu-id="be8f6-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="be8f6-116">Der OLE-com-Viewer zeigt auch die C++-Syntax für die in der Typbibliothek aufgelisteten com-Elemente an.</span><span class="sxs-lookup"><span data-stu-id="be8f6-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="be8f6-117">Weitere Informationen zu Typbibliotheken finden Sie unter [Typbibliotheken und die Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span><span class="sxs-lookup"><span data-stu-id="be8f6-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 