---
description: Die iprovidebug PropertyBuilder-Schnittstelle ermöglicht es Objekten, Eigenschafts Generator Objekte für Eigenschaften anzugeben, wenn Sie implementiert wird.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Iprovidebug PropertyBuilder-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357548"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="b3204-103">Iprovidebug PropertyBuilder-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b3204-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="b3204-104">Die **iprovidebug PropertyBuilder** -Schnittstelle ermöglicht es Objekten, Eigenschafts Generator Objekte für Eigenschaften anzugeben, wenn Sie implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3204-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="b3204-105">Generatoren werden durch eine Schaltfläche mit Auslassungs Zeichen ( \[ ... \] ) im Microsoft Visual Studio Eigenschaften Browser aufgerufen und durch [**executebuilder**](iprovidepropertybuilder-executebuilder.md) aufgerufen, wenn die Schaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="b3204-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="b3204-106">Wenn Sie einen Generator für eine bestimmte Eigenschaft bereitstellen möchten, geben Sie eine GUID für den Eigenschaften-Generator zurück, die für die aktuelle Eigenschaft von [**mappropertytobuilder**](iprovidepropertybuilder-mappropertytobuilder.md)aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3204-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="b3204-107">Generatoren werden in der Regel über modale Dialogfelder implementiert.</span><span class="sxs-lookup"><span data-stu-id="b3204-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="b3204-108">Die Version für diese Schnittstelle ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="b3204-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="b3204-109">Methodenaufrufe werden an einem dynamisch zugewiesenen Endpunkt empfangen (wie in der MSMQ-Binär Dokumentation zur Endpunkt Zuordnung beschrieben) und verwenden die UUID (universell eindeutiger Bezeichner) "33c0c1d8-33cf-11d3-bff2-00c04f990235".</span><span class="sxs-lookup"><span data-stu-id="b3204-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="b3204-110">Member</span><span class="sxs-lookup"><span data-stu-id="b3204-110">Members</span></span>

<span data-ttu-id="b3204-111">Die **iprovidäpropertybuilder: IUnknown** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b3204-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b3204-112">**Iproviabpropertybuilder** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b3204-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="b3204-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b3204-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b3204-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="b3204-114">Methods</span></span>

<span data-ttu-id="b3204-115">Die **iprovidepropertybuilder: IUnknown** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b3204-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="b3204-116">Methode</span><span class="sxs-lookup"><span data-stu-id="b3204-116">Method</span></span>                                                                       | <span data-ttu-id="b3204-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3204-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3204-118">**Executebuilder**</span><span class="sxs-lookup"><span data-stu-id="b3204-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="b3204-119">Benachrichtigt ein-Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="b3204-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="b3204-120">**Mappropertytbuilder**</span><span class="sxs-lookup"><span data-stu-id="b3204-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="b3204-121">Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3204-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="b3204-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3204-122">Requirements</span></span>



| <span data-ttu-id="b3204-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3204-123">Requirement</span></span> | <span data-ttu-id="b3204-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b3204-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3204-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b3204-125">DLL</span></span><br/> | <dl> <span data-ttu-id="b3204-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3204-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
