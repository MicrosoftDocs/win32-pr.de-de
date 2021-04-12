---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Generiert eine Liste von Adapter Objekten, die den aktuellen Adapter Zustand des Systems darstellen, und erfüllt die angegebenen Kriterien.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473748"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="3f3ee-103">Idxcoreadapterfactory:: kreateadapterlist-Methode</span><span class="sxs-lookup"><span data-stu-id="3f3ee-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="3f3ee-104">Generiert eine Liste von Adapter Objekten, die den aktuellen Adapter Zustand des Systems darstellen, und erfüllt die angegebenen Kriterien.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="3f3ee-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="3f3ee-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3ee-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f3ee-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="3f3ee-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f3ee-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="3f3ee-108">numattribute</span><span class="sxs-lookup"><span data-stu-id="3f3ee-108">numAttributes</span></span>

<span data-ttu-id="3f3ee-109">Typ: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-109">Type: **uint32_t**</span></span>

<span data-ttu-id="3f3ee-110">Die Anzahl der Elemente im Array, auf die vom *filterattributerargument* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="3f3ee-111">Filterattribute [in]</span><span class="sxs-lookup"><span data-stu-id="3f3ee-111">filterAttributes [in]</span></span>

<span data-ttu-id="3f3ee-112">Typ: Konstante **GUID \***</span><span class="sxs-lookup"><span data-stu-id="3f3ee-112">Type: **const GUID\***</span></span>

<span data-ttu-id="3f3ee-113">Ein Zeiger auf ein Array von adapterattributguids.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="3f3ee-114">Eine Liste der Attribut-GUIDs finden Sie unter [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3f3ee-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="3f3ee-115">Mindestens eine GUID muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-115">At least one GUID must be provided.</span></span> <span data-ttu-id="3f3ee-116">Wenn mehr als eine GUID im Array bereitgestellt wird, werden nur Adapter, die *alle* angeforderten Attribute erfüllen, in der zurückgegebenen Liste enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="3f3ee-117">riid</span><span class="sxs-lookup"><span data-stu-id="3f3ee-117">riid</span></span>

<span data-ttu-id="3f3ee-118">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-118">Type: **REFIID**</span></span>

<span data-ttu-id="3f3ee-119">Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvadapterlist* zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="3f3ee-120">Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md)erwartet.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="3f3ee-121">ppvadapterlist [out]</span><span class="sxs-lookup"><span data-stu-id="3f3ee-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="3f3ee-122">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="3f3ee-122">Type: **void\*\***</span></span>

<span data-ttu-id="3f3ee-123">Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="3f3ee-124">Bei erfolgreicher Rückgabe enthält *\* ppvadapterlist* (die Dereferenzierte Adresse) einen Zeiger auf die erstellte Adapter Liste.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="3f3ee-125">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="3f3ee-125">Returns</span></span>

<span data-ttu-id="3f3ee-126">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="3f3ee-127">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="3f3ee-128">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="3f3ee-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f3ee-129">Return value</span></span>|<span data-ttu-id="3f3ee-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f3ee-130">Description</span></span>|
|-|-|
|<span data-ttu-id="3f3ee-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3f3ee-131">E_INVALIDARG</span></span>|<span data-ttu-id="3f3ee-132">`nullptr` wurde für *Filter Attribute* bereitgestellt, oder 0 wurde für *numattribute* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="3f3ee-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="3f3ee-133">E_NOINTERFACE</span></span>|<span data-ttu-id="3f3ee-134">Für *riid* wurde ein ungültiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="3f3ee-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="3f3ee-135">E_POINTER</span></span>|<span data-ttu-id="3f3ee-136">`nullptr` wurde für *ppvadapterlist* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3f3ee-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f3ee-137">Remarks</span></span>

<span data-ttu-id="3f3ee-138">Auch wenn keine Adapter gefunden werden, erstellt " **kreateadapterlist** " ein gültiges [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Objekt und gibt **S_OK** zurück, solange die Argumente gültig sind.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="3f3ee-139">Nach der Generierung werden die Adapter in dieser bestimmten Liste nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="3f3ee-140">Die Liste wird jedoch als veraltet eingestuft, wenn einer der Adapter später ungültig wird oder wenn ein neuer Adapter eintrifft, der die angegebenen Filterkriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="3f3ee-141">Die von " **kreateadapterlist** " zurückgegebene Liste ist nicht auf bestimmte Weise geordnet, aber die Reihenfolge einer Liste ist über mehrere Aufrufe hinweg konsistent und auch über Betriebssystem Neustarts hinweg.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="3f3ee-142">Die Reihenfolge kann sich bei Änderungen der Systemkonfiguration ändern, einschließlich des Hinzufügens oder Entfernens eines Adapters oder eines Treiber Updates für einen vorhandenen Adapter.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="3f3ee-143">Sie können sich für diese Änderungen mit [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) mithilfe des Benachrichtigungs Typs **dxcorenotificationtype. adapterliststale** registrieren.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f3ee-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f3ee-144">See also</span></span>

<span data-ttu-id="3f3ee-145">[Idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="3f3ee-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>