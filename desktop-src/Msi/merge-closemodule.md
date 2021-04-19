---
description: Die closemodule-Methode des Merge-Objekts schließt das aktuell geöffnete Windows Installer Mergemodul.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Merge. closemodule-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363203"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="44fa3-103">Merge. closemodule-Methode</span><span class="sxs-lookup"><span data-stu-id="44fa3-103">Merge.CloseModule method</span></span>

<span data-ttu-id="44fa3-104">Die **closemodule** -Methode des [**Merge**](merge-object.md) -Objekts schließt das aktuell geöffnete Windows Installer Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="44fa3-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fa3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44fa3-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="44fa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44fa3-106">Parameters</span></span>

<span data-ttu-id="44fa3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="44fa3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44fa3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44fa3-108">Return value</span></span>

<span data-ttu-id="44fa3-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="44fa3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44fa3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44fa3-110">Remarks</span></span>

<span data-ttu-id="44fa3-111">Das Schließen eines Mergemoduls wirkt sich nicht auf Fehler aus, die nicht abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="44fa3-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="44fa3-112">C++</span><span class="sxs-lookup"><span data-stu-id="44fa3-112">C++</span></span>

<span data-ttu-id="44fa3-113">Siehe [**closemodule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44fa3-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="44fa3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44fa3-114">Requirements</span></span>



| <span data-ttu-id="44fa3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44fa3-115">Requirement</span></span> | <span data-ttu-id="44fa3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="44fa3-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44fa3-117">Version</span><span class="sxs-lookup"><span data-stu-id="44fa3-117">Version</span></span><br/> | <span data-ttu-id="44fa3-118">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="44fa3-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="44fa3-119">Header</span><span class="sxs-lookup"><span data-stu-id="44fa3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="44fa3-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="44fa3-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="44fa3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="44fa3-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="44fa3-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44fa3-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
