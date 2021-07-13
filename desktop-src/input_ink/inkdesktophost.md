---
description: Implementiert die IInkDesktopHost-Schnittstelle.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost-Klasse
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
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689223"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="d8b14-103">InkDesktopHost-Klasse</span><span class="sxs-lookup"><span data-stu-id="d8b14-103">InkDesktopHost class</span></span>

<span data-ttu-id="d8b14-104">Implementiert die [**IInkDesktopHost-Schnittstelle.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)</span><span class="sxs-lookup"><span data-stu-id="d8b14-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="d8b14-105">Ein [**IInkDesktopHost-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) ermöglicht das Eingeben, Verarbeiten und Rendern von Freihandeingaben durch die Erstellung eines App-Threads, um ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) zu hosten und in die visuelle [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App einzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8b14-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="d8b14-106">Member</span><span class="sxs-lookup"><span data-stu-id="d8b14-106">Members</span></span>

<span data-ttu-id="d8b14-107">Die **InkDesktopHost-Klasse** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="d8b14-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d8b14-108">**InkDesktopHost** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8b14-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="d8b14-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8b14-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8b14-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8b14-110">Methods</span></span>

<span data-ttu-id="d8b14-111">Die **InkDesktopHost-Klasse** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d8b14-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="d8b14-112">Methode</span><span class="sxs-lookup"><span data-stu-id="d8b14-112">Method</span></span> | <span data-ttu-id="d8b14-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8b14-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="d8b14-114">**CreateAndInitializeInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="d8b14-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="d8b14-115">Erstellt ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in einem Anwendungsthread, verbindet es mit der visuellen [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App und legt die Größe des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="d8b14-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="d8b14-116">**CreateInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="d8b14-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="d8b14-117">Erstellt ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in einem Anwendungsthread.</span><span class="sxs-lookup"><span data-stu-id="d8b14-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="d8b14-118">**QueueWorkItem**</span><span class="sxs-lookup"><span data-stu-id="d8b14-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="d8b14-119">Fügen Sie einer Arbeitswarteschlange einen Inkk-Vorgang für die Ausführung im **InkDesktopHost-Thread** hinzu.</span><span class="sxs-lookup"><span data-stu-id="d8b14-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="d8b14-120">\\Erstellungszugriffsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d8b14-120">Creation\\Access Functions</span></span>

<span data-ttu-id="d8b14-121">Rufen Sie [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassenbezeichner <strong>InkDesktopHost</strong> auf, um einen Verweis auf das Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8b14-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="d8b14-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8b14-122">Requirements</span></span>

| <span data-ttu-id="d8b14-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8b14-123">Requirement</span></span> | <span data-ttu-id="d8b14-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d8b14-124">Value</span></span> |
|---|---|
| <span data-ttu-id="d8b14-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8b14-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b14-126">\[Windows 10 Nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8b14-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8b14-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8b14-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b14-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8b14-128">None supported</span></span><br/> |
| <span data-ttu-id="d8b14-129">Header</span><span class="sxs-lookup"><span data-stu-id="d8b14-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b14-130"><dt>InkPresenterDesktop.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b14-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8b14-131">Idl</span><span class="sxs-lookup"><span data-stu-id="d8b14-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8b14-132"><dt>InkPresenterDesktop.idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8b14-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8b14-133">IID</span><span class="sxs-lookup"><span data-stu-id="d8b14-133">IID</span></span><br/>                      | <span data-ttu-id="d8b14-134">IID \_ IInkDesktopHost ist als 4ce7d875-a981-4140-a1ff-ad93258e8d59 definiert.</span><span class="sxs-lookup"><span data-stu-id="d8b14-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="d8b14-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8b14-135">Related topics</span></span>

<span data-ttu-id="d8b14-136">[Klassen für die Ink-Präsentation,](ink-presenter-classes.md) [Stift- und Stiftinteraktionen,](/windows/uwp/design/input/pen-and-stylus-interactions) [Beispiel für die Ink-Analyse,](/samples/microsoft/windows-universal-samples/inkanalysis/) [Einfaches Beispiel für Denkaktionen,](/samples/microsoft/windows-universal-samples/simpleink/)Beispiel für [komplexes Inknen](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="d8b14-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
