---
description: Die provideintegerdata-Methode des Objekts "konfiguriertmodule" wird von Mergemod.dll aufgerufen, um ganzzahlige Daten aus dem Client Tool abzurufen.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Konfigurations Methode. provideintegerdata-Methode (Mergemod. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364453"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="6a471-103">Konfigurations Methode. provideintegerdata-Methode</span><span class="sxs-lookup"><span data-stu-id="6a471-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="6a471-104">Die **provideintegerdata** -Methode des [**Objekts "konfiguriertmodule**](configuremodule-object.md) " wird von Mergemod.dll aufgerufen, um ganzzahlige Daten aus dem Client Tool abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a471-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="6a471-105">Mergemod.dll stellt den *Namen* aus dem entsprechenden Eintrag in der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="6a471-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="6a471-106">Das Tool sollte S OK zurückgeben \_ und die passende Anpassungs Ganzzahl in *ConfigData* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6a471-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="6a471-107">Wenn das Tool keine Konfigurationsdaten für diesen *namens* Wert bereitstellt, sollte die Funktion "S false" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="6a471-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="6a471-108">In diesem Fall Mergemod.dll den Wert des Arguments *ConfigData* ignoriert und den Standardwert aus der Tabelle ModuleConfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a471-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a471-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a471-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="6a471-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a471-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a471-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="6a471-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="6a471-112">Der Name des Elements, für das Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6a471-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="6a471-113">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="6a471-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="6a471-114">Zeiger auf den Anpassungs Text.</span><span class="sxs-lookup"><span data-stu-id="6a471-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a471-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a471-115">Return value</span></span>

<span data-ttu-id="6a471-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6a471-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a471-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a471-117">Remarks</span></span>

<span data-ttu-id="6a471-118">Der Client kann für jeden Datensatz in der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" nicht mehr als einmal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6a471-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="6a471-119">Beachten Sie, dass Mergemod.dll für den gleichen "Name"-Wert nie mehrere Aufrufe an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="6a471-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="6a471-120">Wenn kein Datensatz in der ModuleSubstitution-Tabelle die-Eigenschaft verwendet, bewirkt ein Eintrag in der ModuleConfiguration-Tabelle keine Aufrufe an den Client.</span><span class="sxs-lookup"><span data-stu-id="6a471-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="6a471-121">C++</span><span class="sxs-lookup"><span data-stu-id="6a471-121">C++</span></span>

<span data-ttu-id="6a471-122">Siehe [**provideintegerdata-Funktion**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span><span class="sxs-lookup"><span data-stu-id="6a471-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a471-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a471-123">Requirements</span></span>



| <span data-ttu-id="6a471-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a471-124">Requirement</span></span> | <span data-ttu-id="6a471-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6a471-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a471-126">Version</span><span class="sxs-lookup"><span data-stu-id="6a471-126">Version</span></span><br/> | <span data-ttu-id="6a471-127">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6a471-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6a471-128">Header</span><span class="sxs-lookup"><span data-stu-id="6a471-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6a471-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a471-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a471-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6a471-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="6a471-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a471-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




