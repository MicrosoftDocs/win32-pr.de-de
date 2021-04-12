---
description: Die cmediaevent-Klasse stellt die Basisklassen Implementierung der IDispatch-Methoden der Dual-Interface imediaevent bereit. Die Eigenschaften und Methoden der imediaevent-Schnittstelle werden als rein virtuell angezeigt.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Cmediaevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104219024"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="4a5c6-104">Cmediaevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="4a5c6-104">CMediaEvent class</span></span>

![cmediaevent-Klassenhierarchie](images/cutil03.png)

<span data-ttu-id="4a5c6-106">Die- `CMediaEvent` Klasse stellt die Basisklassen Implementierung der **IDispatch** -Methoden der Dual-Interface [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent)bereit.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="4a5c6-107">Die Eigenschaften und Methoden der **imediaevent** -Schnittstelle werden als rein virtuell angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="4a5c6-108">Die- `CMediaEvent` Klasse stellt auch die Basisklassen Implementierung der [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle bereit, die von [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="4a5c6-109">[**Cmediaevent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**cmediaevent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**cmediaevent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)und [**cmediaevent:: Aufrufen**](cmediaevent-invoke.md) Member-Funktionen sind Standard Implementierungen der **IDispatch** -Schnittstelle mithilfe der [**cbasedispatch**](cbasedispatch.md) -Klasse (und einer Typbibliothek), um die Befehle zu analysieren und an die reinen virtuellen Methoden der [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Schnittstelle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="4a5c6-110">Elementfunktionen</span><span class="sxs-lookup"><span data-stu-id="4a5c6-110">Member Functions</span></span>                                         | <span data-ttu-id="4a5c6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a5c6-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a5c6-112">**Cmediaevent**</span><span class="sxs-lookup"><span data-stu-id="4a5c6-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="4a5c6-113">Erstellt ein **cmediaevent** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="4a5c6-114">IDispatch-Methoden</span><span class="sxs-lookup"><span data-stu-id="4a5c6-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="4a5c6-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a5c6-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="4a5c6-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="4a5c6-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="4a5c6-117">Ordnet einen einzelnen Member und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern zu, der bei nachfolgenden Aufrufen der **IDispatch:: Aufrufen** -Methode verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="4a5c6-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="4a5c6-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="4a5c6-119">Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abruft.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="4a5c6-120">**Gettypeingefocount**</span><span class="sxs-lookup"><span data-stu-id="4a5c6-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="4a5c6-121">Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="4a5c6-122">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="4a5c6-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="4a5c6-123">Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="4a5c6-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



