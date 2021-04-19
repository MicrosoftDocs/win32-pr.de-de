---
description: Formatiert die eigenschafteninstanzdaten mit dem von Netzwerkmonitor bereitgestellten generischen Formatierer.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Formatpropertyinstance-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346276"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="d549e-103">Formatpropertyinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="d549e-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="d549e-104">Die Funktion **formatpropertyinstance** formatiert die eigenschafteninstanzdaten mit dem generischen Formatierer, den Netzwerkmonitor bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d549e-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="d549e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d549e-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="d549e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d549e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d549e-107">*lppropertyinst* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d549e-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d549e-108">Ein Zeiger auf eine [propertyinst](propertyinst.md) -Struktur, die die Instanzdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="d549e-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="d549e-109">Bei der Eingabe nimmt das generische Formatierungs Programm die Instanzdaten von einem der **propertyinst** -Union-Member an und konvertiert diese Daten in eine vordefinierte formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d549e-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="d549e-110">Bei der Ausgabe legt das generische Formatierer den **szpropertytext** -Member der **propertyinst** -Struktur auf einen Zeiger auf die formatierte Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="d549e-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d549e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d549e-111">Return value</span></span>

<span data-ttu-id="d549e-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d549e-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d549e-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode von "nmerr. h".</span><span class="sxs-lookup"><span data-stu-id="d549e-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="d549e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d549e-114">Remarks</span></span>

<span data-ttu-id="d549e-115">Die parserdll ruft indirekt die **formatpropertyinstance** -Funktion auf, wenn der generische Formatierer zum Formatieren von Daten für die Anzeige im Detailbereich der Netzwerkmonitor-Benutzeroberfläche erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d549e-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="d549e-116">Um **formatpropertyinstance** aufzurufen, geben Sie diese im **InstanceData** -Member der [PropertyInfo](propertyinfo.md) -Struktur an, wenn Sie die Eigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="d549e-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="d549e-117">Der Parser erkennt nicht, welche Funktion aufgerufen wird, wenn eine Instanz einer Eigenschaft formatiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d549e-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="d549e-118">Bei der Funktion kann es sich um eine **formatpropertyinstance** oder eine vom Parser definierte benutzerdefinierte Format Funktion handeln.</span><span class="sxs-lookup"><span data-stu-id="d549e-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="d549e-119">Der Parser Ruft eine beliebige Format Funktion auf, die vom **InstanceData** -Member der **PropertyInfo** -Struktur für die Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d549e-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="d549e-120">Weitere Informationen und ein Beispiel für die Implementierung von [formatproperties](formatproperties.md)finden Sie unter [Implementieren von formatproperties](implementing-formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="d549e-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="d549e-121">Weitere Informationen dazu, wie das generische Formatierungssystem verschiedene Datentypen formatiert, finden Sie unter [generische formatiererausgabe](generic-formatter-output.md).</span><span class="sxs-lookup"><span data-stu-id="d549e-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d549e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d549e-122">Requirements</span></span>



| <span data-ttu-id="d549e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d549e-123">Requirement</span></span> | <span data-ttu-id="d549e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d549e-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d549e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d549e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d549e-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d549e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d549e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d549e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d549e-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d549e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d549e-129">Header</span><span class="sxs-lookup"><span data-stu-id="d549e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d549e-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d549e-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d549e-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d549e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d549e-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d549e-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d549e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d549e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d549e-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d549e-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d549e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d549e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d549e-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="d549e-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="d549e-137">Propertyinst</span><span class="sxs-lookup"><span data-stu-id="d549e-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




