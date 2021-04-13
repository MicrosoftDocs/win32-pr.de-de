---
description: Ruft Informationen darüber ab, welche Spalten (Objektdaten Typen) von der Objekttabelle unterstützt werden.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablecallback:: getsupportedcolumns-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ed077e0921043245e4ff3dda4b1c33dd4e3f20d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481275"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span data-ttu-id="50501-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>Iobjecttablecallback:: getsupportedcolumns-Methode</span><span class="sxs-lookup"><span data-stu-id="50501-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns method</span></span>

<span data-ttu-id="50501-104">Ruft Informationen darüber ab, welche Spalten (Objektdaten Typen) von der Objekttabelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50501-104">Gets information about which columns (types of object data) are supported by the object table.</span></span>

## <a name="syntax"></a><span data-ttu-id="50501-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50501-105">Syntax</span></span>


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="50501-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50501-106">Parameters</span></span>

<span data-ttu-id="50501-107">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="50501-107">*numColumns* </span></span>  
<span data-ttu-id="50501-108">Die Anzahl der Spalten, die von der Objekttabelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50501-108">The number of columns supported by the object table.</span></span>

<span data-ttu-id="50501-109">*count0_pIDs* </span><span class="sxs-lookup"><span data-stu-id="50501-109">*count0_pIDs* </span></span>  
<span data-ttu-id="50501-110">Die IDs der einzelnen Spalten, die von der Objekttabelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50501-110">The IDs of each column supported by the object table.</span></span>

<span data-ttu-id="50501-111">*count0_pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="50501-111">*count0_pBstrNames* </span></span>  
<span data-ttu-id="50501-112">Die Namen der einzelnen Spalten (als com-Zeichenfolge), die von der Objekttabelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50501-112">The names of each column, as a COM string, supported by the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="50501-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50501-113">Return value</span></span>

<span data-ttu-id="50501-114">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50501-114">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="50501-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50501-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="50501-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50501-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="50501-117">Header</span><span class="sxs-lookup"><span data-stu-id="50501-117">Header</span></span></p></td><td><span data-ttu-id="50501-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="50501-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="50501-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50501-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="50501-120">**Iobjecttablecallback**</span><span class="sxs-lookup"><span data-stu-id="50501-120">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
