---
description: Vorgehensweise beim Implementieren und Registrieren eines Drop-Handlers.
title: Erstellen von Drop-Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215944"
---
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="08ef8-103">Erstellen von Drop-Handlern</span><span class="sxs-lookup"><span data-stu-id="08ef8-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="08ef8-104">Standardmäßig handelt es sich bei Dateien nicht um Drop-Ziele.</span><span class="sxs-lookup"><span data-stu-id="08ef8-104">By default, files are not drop targets.</span></span> <span data-ttu-id="08ef8-105">Sie können die Member eines [Dateityps](fa-file-types.md) in Ablage Ziele ändern, indem Sie einen *Drop-Handler* implementieren und registrieren.</span><span class="sxs-lookup"><span data-stu-id="08ef8-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="08ef8-106">Wenn ein Drop-Handler für einen Dateityp registriert ist, wird er immer dann aufgerufen, wenn ein Objekt auf einen Member des Dateityps gezogen oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="08ef8-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="08ef8-107">Die Shell verwaltet den Vorgang, indem die entsprechenden Methoden in der [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle des Handlers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="08ef8-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="08ef8-108">Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="08ef8-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="08ef8-109">Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Drop-Handler spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="08ef8-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="08ef8-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="08ef8-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="08ef8-111">Schritt 1: Implementieren von Drop-Handlern</span><span class="sxs-lookup"><span data-stu-id="08ef8-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="08ef8-112">Wie bei allen Shellerweiterungs Handlern sind Drop-Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="08ef8-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="08ef8-113">Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)werden zwei Schnittstellen exportiert: [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span><span class="sxs-lookup"><span data-stu-id="08ef8-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="08ef8-114">Die Shell initialisiert den Handler über seine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="08ef8-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="08ef8-115">Diese Schnittstelle wird verwendet, um den Klassen Bezeichner (CLSID) des Handlers anzufordern und den Dateinamen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="08ef8-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="08ef8-116">Eine allgemeine Erörterung der Implementierung von Shellerweiterungs Handlern, einschließlich der **IPersistFile** -Schnittstelle, finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="08ef8-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="08ef8-117">Nachdem der Drop-Handler initialisiert wurde, ruft die Shell die entsprechende Methode für die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle des Handlers auf.</span><span class="sxs-lookup"><span data-stu-id="08ef8-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="08ef8-118">Schritt 2: Registrieren von Drop-Handlern</span><span class="sxs-lookup"><span data-stu-id="08ef8-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="08ef8-119">Drop Handler werden unter dem Unterschlüssel dieses Dateityps registriert.</span><span class="sxs-lookup"><span data-stu-id="08ef8-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="08ef8-120">Erstellen Sie einen Unterschlüssel von **drophandler** mit dem Namen für den Handler, und legen Sie den Standardwert des unter Schlüssels auf die Zeichen folgen Form der CLSID-GUID des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="08ef8-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="08ef8-121">Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="08ef8-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="08ef8-122">Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Drop-Handler für einen example. MYP-Dateityp aktivieren.</span><span class="sxs-lookup"><span data-stu-id="08ef8-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="08ef8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08ef8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08ef8-124">Erstellen von Shellerweiterungshandlern</span><span class="sxs-lookup"><span data-stu-id="08ef8-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="08ef8-125">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="08ef8-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="08ef8-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="08ef8-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
