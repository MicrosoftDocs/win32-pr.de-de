---
description: Ein Installer-Objekt muss anfänglich erstellt werden, um die für den Zugriff auf die Installationsprogramm Komponenten über com erforderliche Automatisierungsunterstützung zu laden.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Informationen zur Automatisierungsschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215732"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="f9d28-103">Informationen zur Automatisierungsschnittstelle</span><span class="sxs-lookup"><span data-stu-id="f9d28-103">About the Automation Interface</span></span>

<span data-ttu-id="f9d28-104">Ein [**Installer-Objekt**](installer-object.md) muss anfänglich erstellt werden, um die für den Zugriff auf die Installationsprogramm Komponenten über com erforderliche Automatisierungsunterstützung zu laden.</span><span class="sxs-lookup"><span data-stu-id="f9d28-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="f9d28-105">Dieses Objekt stellt Wrapper zum Erstellen der Objekte der obersten Ebene und zum Zugreifen auf ihre Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="f9d28-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="f9d28-106">Diese Wrapper stellen einfach Parameter Übersetzungen bereit, um die Installer-Funktionen in Übereinstimmung mit Microsoft Visual Basic verfügbar zu machen, ohne das Verhalten der Methoden zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f9d28-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="f9d28-107">Wenn möglich, werden ein paar von Get-und Set C++-Methoden für Visual Basic als einzelne Eigenschaft verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f9d28-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="f9d28-108">In einigen Fällen werden C++-Methoden, die ein Index-Argument übernehmen, als indizierte Eigenschaft verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f9d28-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="f9d28-109">Viele C++-Methoden geben das Ergebnis über einen Parameter zurück, da der Rückgabewert für die Fehlerrückgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9d28-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="f9d28-110">In Visual Basic werden Fehler jedoch von einem separaten Mechanismus behandelt, und das Ergebnis wird immer im Rückgabewert übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f9d28-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="f9d28-111">Informationen zum Verwenden von Automation und zum Erstellen des Installations Objekts finden Sie unter [Verwenden der Automatisierungsschnittstelle](using-the-automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f9d28-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="f9d28-112">Referenzmaterial für die Windows Installer-Objekte finden Sie unter [Automation Interface Reference](automation-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f9d28-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9d28-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9d28-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9d28-114">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f9d28-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



