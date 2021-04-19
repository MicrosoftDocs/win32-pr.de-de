---
description: Die DataSize-Eigenschaft des Datensatz-Objekts ist eine schreibgeschützte Eigenschaft, die die Größe der Daten für das angegebene Feld zurückgibt.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record. DataSize-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361948"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="9e518-103">Record. DataSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e518-103">Record.DataSize property</span></span>

<span data-ttu-id="9e518-104">Die **DataSize** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die die Größe der Daten für das angegebene Feld zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9e518-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="9e518-105">Wenn es sich bei den Daten um einen Datenstrom handelt, wird die Datenstrom Länge in Bytes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e518-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="9e518-106">Wenn es sich bei den Daten um eine Zeichenfolge handelt, wird die Zeichen folgen Länge ohne NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e518-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="9e518-107">Wenn es sich bei den Daten um eine ganze Zahl handelt, wird der Wert 4 zurückgegeben (was die Größe der ganzen Zahl angibt).</span><span class="sxs-lookup"><span data-stu-id="9e518-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="9e518-108">Wenn die Daten NULL sind, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e518-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="9e518-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9e518-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e518-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e518-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="9e518-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9e518-111">Property value</span></span>

<span data-ttu-id="9e518-112">Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="9e518-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e518-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e518-113">Requirements</span></span>



| <span data-ttu-id="9e518-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e518-114">Requirement</span></span> | <span data-ttu-id="9e518-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9e518-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e518-116">Version</span><span class="sxs-lookup"><span data-stu-id="9e518-116">Version</span></span><br/> | <span data-ttu-id="9e518-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e518-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9e518-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e518-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9e518-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="9e518-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9e518-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9e518-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e518-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e518-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9e518-122">IID</span><span class="sxs-lookup"><span data-stu-id="9e518-122">IID</span></span><br/>     | <span data-ttu-id="9e518-123">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9e518-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




