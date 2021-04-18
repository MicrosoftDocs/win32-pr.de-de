---
description: Die FieldCount-Eigenschaft des Datensatz-Objekts ist eine schreibgeschützte Eigenschaft, die die Anzahl der Felder im Datensatz zurückgibt. Lesezugriff auf Felder über diese Anzahl hinaus gibt NULL-Werte zurück. Schreibzugriff schlägt fehl.
ms.assetid: 50be848a-2d38-4768-aeb4-25cbaedade01
title: Record. FieldCount (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FieldCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 548c1da4c2a0106cbcd667b5ce3c915ec17bf1ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372089"
---
# <a name="recordfieldcount-property"></a><span data-ttu-id="e37b8-105">Record. FieldCount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e37b8-105">Record.FieldCount property</span></span>

<span data-ttu-id="e37b8-106">Die **FieldCount** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die die Anzahl der Felder im Datensatz zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e37b8-106">The **FieldCount** property of the [**Record**](record-object.md) object is a read-only property that returns the number of fields in the record.</span></span> <span data-ttu-id="e37b8-107">Lesezugriff auf Felder über diese Anzahl hinaus gibt NULL-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e37b8-107">Read access to fields beyond this count returns Null values.</span></span> <span data-ttu-id="e37b8-108">Schreibzugriff schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="e37b8-108">Write access fails.</span></span>

<span data-ttu-id="e37b8-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e37b8-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e37b8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e37b8-110">Syntax</span></span>


```JScript
propVal = Record.FieldCount
```



## <a name="property-value"></a><span data-ttu-id="e37b8-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e37b8-111">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e37b8-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e37b8-112">Requirements</span></span>



| <span data-ttu-id="e37b8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e37b8-113">Requirement</span></span> | <span data-ttu-id="e37b8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e37b8-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37b8-115">Version</span><span class="sxs-lookup"><span data-stu-id="e37b8-115">Version</span></span><br/> | <span data-ttu-id="e37b8-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e37b8-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e37b8-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e37b8-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e37b8-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e37b8-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e37b8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e37b8-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="e37b8-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e37b8-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e37b8-121">IID</span><span class="sxs-lookup"><span data-stu-id="e37b8-121">IID</span></span><br/>     | <span data-ttu-id="e37b8-122">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e37b8-122">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




