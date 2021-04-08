---
title: Übersetzen der COM-Objekt Syntax für Programmiersprachen
description: Übersetzen der COM-Objekt Syntax für Programmiersprachen
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855999"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="24ba9-103">Übersetzen der COM-Objekt Syntax für Programmiersprachen</span><span class="sxs-lookup"><span data-stu-id="24ba9-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="24ba9-104">Zum Abrufen eines COM-Objekts aus einer Anwendung, die in einer anderen Programmiersprache als der verwendet wird, um das COM-Objekt zu schreiben, müssen Sie zuerst die Syntax des Objekts in Ihre Programmiersprache übersetzen.</span><span class="sxs-lookup"><span data-stu-id="24ba9-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="24ba9-105">Führen Sie hierzu die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="24ba9-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="24ba9-106">Zeigen Sie die Typbibliothek des COM-Objekts in der Syntax der Programmiersprache an.</span><span class="sxs-lookup"><span data-stu-id="24ba9-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="24ba9-107">Dadurch erhalten Sie Beschreibungen der Klassen, Schnittstellen, Methoden, Eigenschaften und Ereignisse des Objekts in der verwendeten Sprachsyntax.</span><span class="sxs-lookup"><span data-stu-id="24ba9-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="24ba9-108">Microsoft-Entwickler Produkte bieten verschiedene Tools, die Sie beim Anzeigen und Umrechnen von Typbibliotheken unterstützen.</span><span class="sxs-lookup"><span data-stu-id="24ba9-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="24ba9-109">Weitere Informationen finden Sie unter [Typbibliotheks-Viewer und-Konvertierungs Tools](type-library-viewers-and-conversion-tools.md) und [Entwicklertools Verwenden von Typbibliotheken](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="24ba9-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="24ba9-110">Wenn Sie die Typbibliothek des Objekts in Ihrer bevorzugten Programmiersprache anzeigen können, können Sie die zugehörige Syntax mit der in der Dokumentation für das Objekt vergleichen.</span><span class="sxs-lookup"><span data-stu-id="24ba9-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="24ba9-111">Wenn das Objekt in einer anderen Programmiersprache als der von Ihnen verwendeten Programmiersprache dokumentiert ist, können die Datentypen und die Syntax abweichen, aber die Beschreibungen der Parameter, Rückgabewerte und die Funktionalität des Objekts sollten identisch sein.</span><span class="sxs-lookup"><span data-stu-id="24ba9-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="24ba9-112">Berücksichtigen Sie besondere Überlegungen für die Übersetzung in Ihre Programmiersprache.</span><span class="sxs-lookup"><span data-stu-id="24ba9-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="24ba9-113">Da jede Programmiersprache Konzepte definiert, die möglicherweise in anderen Sprachen nicht gleichwertig sind, können einige Funktionen eines Objekts in einer anderen Sprache unterschiedlich funktionieren oder überhaupt nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="24ba9-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="24ba9-114">Beispielsweise erkennt die Programmiersprache Visual Basic nicht signierte C++-Datentypen, wie z. b. **"unsignedLong"**.</span><span class="sxs-lookup"><span data-stu-id="24ba9-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="24ba9-115">Eine in Visual Basic geschriebene Anwendung kann keine com-Methoden verwenden, die nicht signierte Datentyp Variablen akzeptieren oder zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="24ba9-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="24ba9-116">Fügen Sie dem Projekt den kompilierten Code des COM-Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="24ba9-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="24ba9-117">Der kompilierte Code ist in der Regel in einer DLL-oder OCX-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="24ba9-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="24ba9-118">Dieser Schritt ist erforderlich, damit der Compiler die Klassen des COM-Objekts erkennen kann.</span><span class="sxs-lookup"><span data-stu-id="24ba9-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="24ba9-119">Nachdem Sie das COM-Objekt hinzugefügt haben, kann die Anwendung seine Klassen und Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="24ba9-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="24ba9-120">In den folgenden Themen wird beschrieben, wie COM-Objekte in einer Vielzahl von Programmiersprachen übersetzt und verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="24ba9-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="24ba9-121">Übersetzen in C++</span><span class="sxs-lookup"><span data-stu-id="24ba9-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="24ba9-122">Übersetzen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="24ba9-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="24ba9-123">Übersetzen in Java</span><span class="sxs-lookup"><span data-stu-id="24ba9-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="24ba9-124">In diesen Themen werden die Konvertierungs Tools und-Prozesse beschrieben, die von Microsoft-Entwickler Produkten</span><span class="sxs-lookup"><span data-stu-id="24ba9-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="24ba9-125">Anweisungen zum Programmieren von COM-Objekten mit von anderen Unternehmen erstellten Entwicklungs Tools finden Sie in der Dokumentation der Entwicklungs Tools.</span><span class="sxs-lookup"><span data-stu-id="24ba9-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 




