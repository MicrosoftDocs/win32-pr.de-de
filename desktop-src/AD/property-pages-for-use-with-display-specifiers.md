---
title: Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken
description: Active Directory Domain Services bieten einen Mechanismus zum Hinzufügen von Seiten zu dem Eigenschaften Blatt, das für ein Verzeichnis Objekt aus den Active Directory Verwaltungs-Snap-Ins oder der Windows-Shell angezeigt wird.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- Anzeige spezifiker anzeigen, Eigenschaften Seiten für die Verwendung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858131"
---
# <a name="property-pages-for-use-with-display-specifiers"></a><span data-ttu-id="bb4dc-104">Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken</span><span class="sxs-lookup"><span data-stu-id="bb4dc-104">Property Pages for Use with Display Specifiers</span></span>

<span data-ttu-id="bb4dc-105">Active Directory Domain Services bieten einen Mechanismus zum Hinzufügen von Seiten zu dem Eigenschaften Blatt, das für ein Verzeichnis Objekt aus den Active Directory Verwaltungs-Snap-Ins oder der Windows-Shell angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-105">Active Directory Domain Services provide a mechanism for adding pages to the property sheet displayed for a directory object from the Active Directory administrative snap-ins or the Windows shell.</span></span> <span data-ttu-id="bb4dc-106">Um dem Eigenschaften Blatt eine Seite hinzuzufügen, implementieren Sie eine Eigenschaften Blatt Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-106">To add a page to the property sheet, implement a property sheet extension.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bb4dc-107">Entwicklerzielgruppe</span><span class="sxs-lookup"><span data-stu-id="bb4dc-107">Developer Audience</span></span>

<span data-ttu-id="bb4dc-108">In dieser Dokumentation wird davon ausgegangen, dass der Reader mit der com-Operation und-Komponentenentwicklung mit C++ vertraut ist.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-108">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="bb4dc-109">Es ist derzeit nicht möglich, eine Active Directory Eigenschaften Blatt Erweiterung mit Visual Basic zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-109">It is not currently possible to create an Active Directory property sheet extension using Visual Basic.</span></span>

## <a name="creating-an-active-directory-property-sheet-extension"></a><span data-ttu-id="bb4dc-110">Erstellen einer Active Directory-Eigenschaften Blatt Erweiterung</span><span class="sxs-lookup"><span data-stu-id="bb4dc-110">Creating an Active Directory Property Sheet Extension</span></span>

<span data-ttu-id="bb4dc-111">Eine *Eigenschaften Blatt Erweiterung* ist ein com-in-proc-Server, der bestimmte Schnittstellen implementiert und bei Active Directory Domain Services registriert ist.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-111">A *property sheet extension* is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span> <span data-ttu-id="bb4dc-112">Führen Sie die folgenden Schritte aus, um eine Eigenschaften Blatt Erweiterung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-112">To create a property sheet extension, perform the following steps.</span></span>

<span data-ttu-id="bb4dc-113">**So erstellen Sie eine Active Directory-Eigenschaften Blatt Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="bb4dc-113">**To create an Active Directory property sheet extension**</span></span>

1.  <span data-ttu-id="bb4dc-114">Erstellen Sie die Eigenschaften Blatt-Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-114">Create the property sheet extension DLL.</span></span> <span data-ttu-id="bb4dc-115">Eine Eigenschaften Blatt Erweiterung ist ein com-in-proc-Server, der mindestens die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -und [**ishellpropsheetext**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-115">A property sheet extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interfaces.</span></span> <span data-ttu-id="bb4dc-116">Weitere Informationen finden Sie unter [Implementieren des COM-Objekts der Eigenschaften Seite](implementing-the-property-page-com-object.md).</span><span class="sxs-lookup"><span data-stu-id="bb4dc-116">For more information, see [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).</span></span>
2.  <span data-ttu-id="bb4dc-117">Installieren Sie die Eigenschaften Blatt Erweiterung auf den Computern, auf denen die Eigenschaften Blatt Erweiterung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-117">Install the property sheet extension on the computers where the property sheet extension is to be used.</span></span> <span data-ttu-id="bb4dc-118">Zu diesem Zweck erstellen Sie ein Microsoft Windows Installer Paket für die DLL-Datei der Eigenschafts Blatt Erweiterung und stellen das Paket entsprechend mithilfe der Gruppenrichtlinie bereit.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-118">To do this, create a Microsoft Windows Installer package for the property sheet extension DLL and deploy the package appropriately using the group policy.</span></span> <span data-ttu-id="bb4dc-119">Weitere Informationen finden Sie unter [Verteilen von Benutzeroberflächen Komponenten](distributing-user-interface-components.md).</span><span class="sxs-lookup"><span data-stu-id="bb4dc-119">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="bb4dc-120">Registrieren Sie die Erweiterung des Eigenschaften Blatts in der Windows-Registrierung und mit Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="bb4dc-120">Register the property sheet extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="bb4dc-121">Weitere Informationen finden Sie unter [Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="bb4dc-121">For more information, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>

 

 