---
description: Die Persistenzmethode des SummaryInfo-Objekts formatiert und schreibt die zuvor gespeicherten Eigenschaften in den standardmäßigen SummaryInformation-Stream.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. persistent-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361305"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="a4332-103">SummaryInfo. persistent-Methode</span><span class="sxs-lookup"><span data-stu-id="a4332-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="a4332-104">Die **Persistenzmethode** des [**SummaryInfo**](summaryinfo-object.md) -Objekts formatiert und schreibt die zuvor gespeicherten Eigenschaften in den standardmäßigen SummaryInformation-Stream.</span><span class="sxs-lookup"><span data-stu-id="a4332-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="a4332-105">Es wird ein Fehler generiert, wenn der Stream nicht erfolgreich geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4332-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="a4332-106">Diese Methode kann nur einmal aufgerufen werden, nachdem alle Eigenschaftswerte festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="a4332-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="a4332-107">Eigenschaften können nach dem Schreiben des Streams noch gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a4332-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4332-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4332-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="a4332-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4332-109">Parameters</span></span>

<span data-ttu-id="a4332-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4332-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4332-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4332-111">Return value</span></span>

<span data-ttu-id="a4332-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a4332-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4332-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4332-113">Requirements</span></span>



| <span data-ttu-id="a4332-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4332-114">Requirement</span></span> | <span data-ttu-id="a4332-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a4332-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4332-116">Version</span><span class="sxs-lookup"><span data-stu-id="a4332-116">Version</span></span><br/> | <span data-ttu-id="a4332-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a4332-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a4332-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4332-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a4332-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4332-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a4332-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a4332-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4332-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4332-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a4332-122">IID</span><span class="sxs-lookup"><span data-stu-id="a4332-122">IID</span></span><br/>     | <span data-ttu-id="a4332-123">IID \_ isummaryinfo ist definiert als 000c109b-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a4332-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




