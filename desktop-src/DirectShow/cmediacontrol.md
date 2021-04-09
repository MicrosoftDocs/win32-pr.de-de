---
description: Die cmediacontrol-Klasse stellt die Basisklassen Behandlung der IDispatch-Methoden der Dual-Interface IMediaControl bereit. Die Eigenschaften und Methoden der IMediaControl-Schnittstelle werden als rein virtuell angezeigt.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Cmediacontrol-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869595"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="4f275-104">Cmediacontrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="4f275-104">CMediaControl class</span></span>

![cmediacontrol-Klassenhierarchie](images/cutil02.png)

<span data-ttu-id="4f275-106">Die- `CMediaControl` Klasse stellt die Basisklassen Behandlung der [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Methoden der Dual-Interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)bereit.</span><span class="sxs-lookup"><span data-stu-id="4f275-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="4f275-107">Die Eigenschaften und Methoden der **IMediaControl** -Schnittstelle werden als rein virtuell angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f275-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="4f275-108">In der Regel ist der Filter Graph-Manager das einzige Objekt, das die [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f275-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="4f275-109">(Filter implementieren die [**imediafilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) -Schnittstelle, die von [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)geerbt wurde, um Steuerungsbefehle vom Filter Graph-Manager zu empfangen.) Daher ist diese Klassenbibliothek nur für das Filtern von Entwicklern eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="4f275-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="4f275-110">[**Cmediacontrol:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**cmediacontrol:: die Funktionen "GetTypeInfo**](cmediacontrol-gettypeinfo.md)", " [**cmediacontrol:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)" und " [**cmediacontrol:: Aufrufen**](cmediacontrol-invoke.md) " sind Standard Implementierungen der [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Methoden mithilfe der [**cbasedispatch**](cbasedispatch.md) -Klasse (und einer Typbibliothek) zum Analysieren der Befehle und zum übergeben an die reinen virtuellen Methoden der Schnittstelle " [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) "</span><span class="sxs-lookup"><span data-stu-id="4f275-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="4f275-111">Die in Control. ODL definierten [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Methoden werden als rein virtuell belassen.</span><span class="sxs-lookup"><span data-stu-id="4f275-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="4f275-112">Elementfunktionen</span><span class="sxs-lookup"><span data-stu-id="4f275-112">Member Functions</span></span>                                           | <span data-ttu-id="4f275-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f275-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f275-114">**Cmediacontrol**</span><span class="sxs-lookup"><span data-stu-id="4f275-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="4f275-115">Erstellt ein **cmediacontrol** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4f275-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="4f275-116">IDispatch-Methoden</span><span class="sxs-lookup"><span data-stu-id="4f275-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="4f275-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f275-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="4f275-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="4f275-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="4f275-119">Ordnet einen einzelnen Member und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern (DispIds) zu, der bei nachfolgenden Aufrufen der [**cmediacontrol:: Aufrufen**](cmediacontrol-invoke.md) -Methode verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4f275-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="4f275-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="4f275-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="4f275-121">Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="4f275-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="4f275-122">**Gettypeingefocount**</span><span class="sxs-lookup"><span data-stu-id="4f275-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="4f275-123">Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="4f275-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="4f275-124">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="4f275-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="4f275-125">Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="4f275-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
