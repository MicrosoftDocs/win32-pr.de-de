---
description: Die Funktion "-Funktion" erstellt eine Eigenschaften Datenbank, in der die Eigenschaften eines Protokolls gespeichert werden.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Funktion "up propertydatabase" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348591"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="b1b74-103">Funktion "up propertydatabase"</span><span class="sxs-lookup"><span data-stu-id="b1b74-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="b1b74-104">Die **Funktion "** -Funktion" erstellt eine Eigenschaften Datenbank, in der die Eigenschaften eines Protokolls gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b1b74-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b74-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="b1b74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b74-107">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1b74-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b74-108">Handle des Protokolls, das der Datenbank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b1b74-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="b1b74-109">Wenn Netzwerkmonitor die [Register](register-parser.md) -Funktion aufruft, übergibt Netzwerkmonitor das Protokoll Handle an die Parser-DLL.</span><span class="sxs-lookup"><span data-stu-id="b1b74-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="b1b74-110">*nproperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1b74-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b74-111">Anzahl der in der Datenbank gespeicherten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1b74-111">Number of properties stored in the database.</span></span> <span data-ttu-id="b1b74-112">Legen Sie diesen Parameter auf die Anzahl der Eigenschaften fest, die das Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1b74-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b74-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1b74-113">Return value</span></span>

<span data-ttu-id="b1b74-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b1b74-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b1b74-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b1b74-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="b1b74-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b1b74-116">Return code</span></span>                                                                                             | <span data-ttu-id="b1b74-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1b74-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1b74-118"><dt>**Interner nmerr- \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b74-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="b1b74-119">Ein interner Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b1b74-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b1b74-120"><dt>**nmerr \_ ungültige \_ hpotocol.**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b74-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="b1b74-121">Das Handle für das in *hprotocol* angegebene Protokoll ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b1b74-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="b1b74-122"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b74-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="b1b74-123">Netzwerkmonitor verfügt nicht über genügend Arbeitsspeicher, um die Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1b74-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1b74-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1b74-124">Remarks</span></span>

<span data-ttu-id="b1b74-125">Die Funktion " **deatepropertydatabase** " sollte nur aufgerufen werden, wenn die [Register](register-parser.md) Funktion implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b1b74-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="b1b74-126">Der Parser erstellt mithilfe von " **kreatepropertydatabase** " eine Eigenschaften Datenbank, in der die Eigenschaften eines Protokolls beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b1b74-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="b1b74-127">Netzwerkmonitor verwendet die Datenbank, um die Informationen innerhalb des Protokolls zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="b1b74-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="b1b74-128">Die Funktion " **kreatepropertydatabase** " ordnet die Strukturen zu, die Netzwerkmonitor für die Wartung einer Eigenschaften Datenbank benötigt.</span><span class="sxs-lookup"><span data-stu-id="b1b74-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b74-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1b74-129">Requirements</span></span>



| <span data-ttu-id="b1b74-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1b74-130">Requirement</span></span> | <span data-ttu-id="b1b74-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b1b74-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b74-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1b74-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b74-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1b74-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b1b74-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1b74-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b74-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1b74-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1b74-136">Header</span><span class="sxs-lookup"><span data-stu-id="b1b74-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1b74-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b74-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1b74-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1b74-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1b74-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1b74-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1b74-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b1b74-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1b74-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1b74-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b74-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1b74-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b74-143">Registrieren</span><span class="sxs-lookup"><span data-stu-id="b1b74-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




