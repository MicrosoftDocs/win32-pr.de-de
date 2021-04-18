---
description: Ruft einen Verweis auf ein TCP-V6-Treiber Objekt ab.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365776"
---
# <a name="referencetcpdriverv6-function"></a><span data-ttu-id="cdd14-103">ReferenceTcpDriverV6-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdd14-103">ReferenceTcpDriverV6 function</span></span>

<span data-ttu-id="cdd14-104">Ruft einen Verweis auf ein TCP-V6-Treiber Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="cdd14-104">Obtains a reference to a TCP v6 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd14-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="cdd14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd14-107">*ppdriverobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdd14-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd14-108">Ein Zeiger auf eine **Treiber \_ Objekt** Struktur.</span><span class="sxs-lookup"><span data-stu-id="cdd14-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="cdd14-109">Weitere Informationen finden Sie in der Dokumentation für das WDK.</span><span class="sxs-lookup"><span data-stu-id="cdd14-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd14-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdd14-110">Return value</span></span>

<span data-ttu-id="cdd14-111">Wenn die Funktion erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdd14-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="cdd14-112">Wenn ein Fehler auftritt, wird der entsprechende Statuscode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdd14-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd14-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdd14-113">Remarks</span></span>

<span data-ttu-id="cdd14-114">Diese Funktion kann nur aus dem Kernel Modus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cdd14-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="cdd14-115">Der Aufrufer muss den Verweis Zähler verringern, indem er die **obdereferenceobject** -Funktion aufruft, wenn er mit dem-Objekt abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cdd14-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="cdd14-116">Diese Funktion ist in drvref. lib implementiert, das zum Download verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cdd14-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="cdd14-117">Siehe [Referenz-API-Bibliothek für Windows-Netzwerktreiber](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="cdd14-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd14-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdd14-118">Requirements</span></span>



| <span data-ttu-id="cdd14-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdd14-119">Requirement</span></span> | <span data-ttu-id="cdd14-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cdd14-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd14-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdd14-121">Library</span></span><br/> | <dl> <span data-ttu-id="cdd14-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdd14-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd14-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdd14-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd14-124">**Referencetcpdriver**</span><span class="sxs-lookup"><span data-stu-id="cdd14-124">**ReferenceTcpDriver**</span></span>](referencetcpdriver.md)
</dt> </dl>

 

 




