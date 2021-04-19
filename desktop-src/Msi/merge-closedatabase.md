---
description: Die CloseDatabase-Methode des Merge-Objekts schließt die aktuell geöffnete Windows Installer Datenbank.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge. CloseDatabase-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350748"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="92092-103">Merge. CloseDatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="92092-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="92092-104">Die **CloseDatabase** -Methode des [**Merge**](merge-object.md) -Objekts schließt die aktuell geöffnete Windows Installer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="92092-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="92092-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92092-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="92092-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92092-107">*bcommit*</span><span class="sxs-lookup"><span data-stu-id="92092-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="92092-108">**True** , wenn Änderungen gespeichert werden sollen, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="92092-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92092-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92092-109">Return value</span></span>

<span data-ttu-id="92092-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="92092-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92092-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92092-111">Remarks</span></span>

<span data-ttu-id="92092-112">Durch das Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber keine Fehler, die noch nicht abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="92092-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="92092-113">C++</span><span class="sxs-lookup"><span data-stu-id="92092-113">C++</span></span>

<span data-ttu-id="92092-114">Siehe [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="92092-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="92092-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92092-115">Requirements</span></span>



| <span data-ttu-id="92092-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92092-116">Requirement</span></span> | <span data-ttu-id="92092-117">Wert</span><span class="sxs-lookup"><span data-stu-id="92092-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92092-118">Version</span><span class="sxs-lookup"><span data-stu-id="92092-118">Version</span></span><br/> | <span data-ttu-id="92092-119">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="92092-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="92092-120">Header</span><span class="sxs-lookup"><span data-stu-id="92092-120">Header</span></span><br/>  | <dl> <span data-ttu-id="92092-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="92092-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="92092-122">DLL</span><span class="sxs-lookup"><span data-stu-id="92092-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="92092-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92092-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
