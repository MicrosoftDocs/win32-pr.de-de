---
description: Implementiert die iinkdesktophost-Schnittstelle.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Inkdesktophost-Klasse
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106365221"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="55a81-103">Inkdesktophost-Klasse</span><span class="sxs-lookup"><span data-stu-id="55a81-103">InkDesktopHost class</span></span>

<span data-ttu-id="55a81-104">Implementiert die [**iinkdesktophost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="55a81-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="55a81-105">Ein [**iinkdesktophost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) -Objekt ermöglicht das Übertragen von Eingaben, die Verarbeitung und das Rendering durch die Erstellung eines App-Threads zum Hosten eines [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekts und das Einfügen in die visuelle [directcomposition](../directcomp/directcomposition-portal.md) -Struktur der app.</span><span class="sxs-lookup"><span data-stu-id="55a81-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="55a81-106">Member</span><span class="sxs-lookup"><span data-stu-id="55a81-106">Members</span></span>

<span data-ttu-id="55a81-107">Die **inkdesktophost** -Klasse erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="55a81-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="55a81-108">**Inkdesktophost** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="55a81-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="55a81-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="55a81-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55a81-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="55a81-110">Methods</span></span>

<span data-ttu-id="55a81-111">Die **inkdesktophost** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="55a81-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="55a81-112">Methode</span><span class="sxs-lookup"><span data-stu-id="55a81-112">Method</span></span> | <span data-ttu-id="55a81-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55a81-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="55a81-114">**"Kreateandinitializabkpresenter"**</span><span class="sxs-lookup"><span data-stu-id="55a81-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="55a81-115">Erstellt ein [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekt in einem Anwendungs Thread, verbindet es mit der visuellen Struktur des [directcomposition](../directcomp/directcomposition-portal.md) -Objekts der APP und legt die Größe des-Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="55a81-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="55a81-116">**"Kreatabkpresenter"**</span><span class="sxs-lookup"><span data-stu-id="55a81-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="55a81-117">Erstellt ein [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekt in einem Anwendungs Thread.</span><span class="sxs-lookup"><span data-stu-id="55a81-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="55a81-118">**Queueworkitem**</span><span class="sxs-lookup"><span data-stu-id="55a81-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="55a81-119">Fügen Sie einer Arbeits Warteschlange einen frei Hand Vorgang zur Ausführung auf dem **inkdesktophost** -Thread hinzu.</span><span class="sxs-lookup"><span data-stu-id="55a81-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="55a81-120">Zugriffs Funktionen für die Erstellung \\</span><span class="sxs-lookup"><span data-stu-id="55a81-120">Creation\\Access Functions</span></span>

<span data-ttu-id="55a81-121">Rufen Sie [<strong>cokreateinstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassen Bezeichner <strong>inkdesktophost</strong> auf, um einen Verweis auf das Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="55a81-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="55a81-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a81-122">Requirements</span></span>

| <span data-ttu-id="55a81-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a81-123">Requirement</span></span> | <span data-ttu-id="55a81-124">Wert</span><span class="sxs-lookup"><span data-stu-id="55a81-124">Value</span></span> |
|---|---|
| <span data-ttu-id="55a81-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55a81-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55a81-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a81-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="55a81-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55a81-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55a81-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="55a81-128">None supported</span></span><br/> |
| <span data-ttu-id="55a81-129">Header</span><span class="sxs-lookup"><span data-stu-id="55a81-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a81-130"><dt>Inkpresenterdesktop. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a81-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="55a81-131">IDL</span><span class="sxs-lookup"><span data-stu-id="55a81-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55a81-132"><dt>Inkpresenterdesktop. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55a81-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="55a81-133">IID</span><span class="sxs-lookup"><span data-stu-id="55a81-133">IID</span></span><br/>                      | <span data-ttu-id="55a81-134">IID \_ iinkdesktophost ist als 4ce7d875-A981-4140-a1ff-ad93258e8d59 definiert.</span><span class="sxs-lookup"><span data-stu-id="55a81-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="55a81-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55a81-135">Related topics</span></span>

<span data-ttu-id="55a81-136">[Ink Presenter-Klassen](ink-presenter-classes.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift Analyse- [Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel zum Einfügen](/samples/microsoft/windows-universal-samples/simpleink/), Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung</span><span class="sxs-lookup"><span data-stu-id="55a81-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
