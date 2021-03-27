---
description: Erweitern der Zwischenablage mit benutzerdefinierten Datenformat Handlern.
title: Erstellen von Daten Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994686"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="f4505-103">Erstellen von Daten Handlern</span><span class="sxs-lookup"><span data-stu-id="f4505-103">How to Create Data Handlers</span></span>

<span data-ttu-id="f4505-104">Wenn eine Datei in die Zwischenablage kopiert oder gezogen und abgelegt wird, erstellt die Shell ein Datenobjekt, das eine Vielzahl von standardmäßigen [Zwischenablage Formaten](dragdrop.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4505-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="f4505-105">Für Dateien, die einen bestimmten Dateityp haben, können Sie die verfügbaren Zwischenablage Formate durch Implementieren und Registrieren eines *Daten Handlers* erweitern.</span><span class="sxs-lookup"><span data-stu-id="f4505-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="f4505-106">Wenn eine Datei des Dateityps übertragen wird, delegiert die Shell Aufrufe an die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts an den Daten Handler, wenn eines der benutzerdefinierten Formate verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4505-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="f4505-107">Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="f4505-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="f4505-108">Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Daten Handler spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f4505-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="f4505-109">Implementieren von Daten Handlern</span><span class="sxs-lookup"><span data-stu-id="f4505-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="f4505-110">Registrieren von Daten Handlern</span><span class="sxs-lookup"><span data-stu-id="f4505-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="f4505-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4505-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="f4505-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="f4505-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="f4505-113">Schritt 1: Implementieren von Daten Handlern</span><span class="sxs-lookup"><span data-stu-id="f4505-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="f4505-114">Wie bei allen Shellerweiterungs Handlern sind Daten Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4505-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="f4505-115">Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)werden zwei Schnittstellen exportiert: [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="f4505-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="f4505-116">Die Shell initialisiert den Handler über seine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f4505-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="f4505-117">Diese Schnittstelle wird verwendet, um den Klassen Bezeichner (CLSID) des Handlers anzufordern und den Dateinamen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f4505-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="f4505-118">Eine allgemeine Erörterung der Implementierung von Shellerweiterungs Handlern, einschließlich der **IPersistFile** -Schnittstelle, finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f4505-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="f4505-119">Nachdem der Daten Handler initialisiert wurde, delegiert die Shell Aufrufe aus dem Datenobjekt an die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Handlers, wenn eines der benutzerdefinierten Formate verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4505-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="f4505-120">Schritt 2: Registrieren von Daten Handlern</span><span class="sxs-lookup"><span data-stu-id="f4505-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="f4505-121">Daten Handler werden unter dem *ProgID* -Unterschlüssel des Dateityps registriert, wie hier gezeigt: **HKEY \_ Classes \_ root** \\ *ProgID* \\ **shellex** \\ **DataHandler**</span><span class="sxs-lookup"><span data-stu-id="f4505-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="f4505-122">Erstellen Sie einen Unterschlüssel mit dem Namen für den Handler unter **DataHandler** , und legen Sie den Standardwert des unter Schlüssels dieses Handlers auf die Zeichen folgen Form der CLSID-GUID des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="f4505-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="f4505-123">Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f4505-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="f4505-124">Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Daten Handler für einen example. MYP-Dateityp aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f4505-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="f4505-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4505-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4505-126">Erstellen von Shellerweiterungshandlern</span><span class="sxs-lookup"><span data-stu-id="f4505-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="f4505-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="f4505-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="f4505-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="f4505-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
