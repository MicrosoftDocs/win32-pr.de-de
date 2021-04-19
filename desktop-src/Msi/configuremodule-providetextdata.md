---
description: Die providetextdata-Methode wird von Mergemod.dll aufgerufen, um Textdaten aus dem Client Tool abzurufen. Mergemod.dll stellt den Namen aus dem entsprechenden Eintrag in der Tabelle ModuleConfiguration bereit.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: "\"Konfigurationsmodul. providetextdata\"-Methode (Mergemod. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370320"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="7315e-104">"Konfigurationsmodul. providetextdata"-Methode</span><span class="sxs-lookup"><span data-stu-id="7315e-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="7315e-105">Die **providetextdata** -Methode wird von Mergemod.dll aufgerufen, um Textdaten aus dem Client Tool abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7315e-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="7315e-106">Mergemod.dll stellt den *Namen* aus dem entsprechenden Eintrag in der Tabelle ModuleConfiguration bereit.</span><span class="sxs-lookup"><span data-stu-id="7315e-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="7315e-107">Das Tool sollte S OK zurückgeben \_ und den entsprechenden Anpassungs Text in ConfigData bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7315e-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="7315e-108">Das Client Tool ist für die Zuordnung der Daten zuständig, Mergemod.dllist jedoch für die Freigabe des Arbeitsspeichers zuständig.</span><span class="sxs-lookup"><span data-stu-id="7315e-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="7315e-109">Dieses Argument muss ein **BSTR** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="7315e-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="7315e-110">**LPCWSTR** wird nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="7315e-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="7315e-111">Wenn das Tool keine Konfigurationsdaten für diesen *namens* Wert bereitstellt, sollte die Funktion "S false" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="7315e-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="7315e-112">In diesem Fall Mergemod.dll den Wert des Arguments ConfigData ignoriert und den Standardwert aus der Tabelle ModuleConfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="7315e-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="7315e-113">Jeder andere Rückgabecode als s \_ OK oder s \_ false bewirkt, dass ein Fehler protokolliert wird (wenn ein Protokoll geöffnet ist), und führt zu einem Fehler beim Zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="7315e-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="7315e-114">Da diese Funktion der standardmäßigen **BSTR** -Konvention folgt, entspricht NULL der leeren Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7315e-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7315e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="7315e-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="7315e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7315e-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7315e-117">*Name*</span><span class="sxs-lookup"><span data-stu-id="7315e-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="7315e-118">Der Name des Elements, für das Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7315e-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="7315e-119">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="7315e-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="7315e-120">Zeiger auf den Anpassungs Text.</span><span class="sxs-lookup"><span data-stu-id="7315e-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7315e-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7315e-121">Return value</span></span>

<span data-ttu-id="7315e-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7315e-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7315e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7315e-123">Remarks</span></span>

<span data-ttu-id="7315e-124">Der Client kann für jeden Datensatz in der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" nicht mehr als einmal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7315e-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="7315e-125">Beachten Sie, dass Mergemod.dll für den gleichen "Name"-Wert nie mehrere Aufrufe an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="7315e-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="7315e-126">Wenn kein Datensatz in der ModuleSubstitution-Tabelle die-Eigenschaft verwendet, bewirkt ein Eintrag in der ModuleConfiguration-Tabelle keine Aufrufe an den Client.</span><span class="sxs-lookup"><span data-stu-id="7315e-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="7315e-127">C++</span><span class="sxs-lookup"><span data-stu-id="7315e-127">C++</span></span>

<span data-ttu-id="7315e-128">Weitere Informationen finden Sie unter [**providebug TextData-Funktion**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span><span class="sxs-lookup"><span data-stu-id="7315e-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="7315e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7315e-129">Requirements</span></span>



| <span data-ttu-id="7315e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7315e-130">Requirement</span></span> | <span data-ttu-id="7315e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7315e-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7315e-132">Version</span><span class="sxs-lookup"><span data-stu-id="7315e-132">Version</span></span><br/> | <span data-ttu-id="7315e-133">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7315e-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="7315e-134">Header</span><span class="sxs-lookup"><span data-stu-id="7315e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7315e-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="7315e-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="7315e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7315e-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="7315e-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7315e-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




