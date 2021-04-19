---
description: Die Funktion "| atehandofftable" erstellt eine Übergabe Tabelle, die die in der INI-Datei des Parsers gespeicherten Übergabe-Informationen enthält.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Funktion "anatehandofftable" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355689"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="99b79-103">"Anatehandofftable"-Funktion</span><span class="sxs-lookup"><span data-stu-id="99b79-103">CreateHandoffTable function</span></span>

<span data-ttu-id="99b79-104">Die Funktion "| **atehandofftable** " erstellt eine [*Übergabe Tabelle*](h.md) , die die in der INI-Datei des Parsers gespeicherten Übergabe-Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="99b79-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99b79-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="99b79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99b79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b79-107">*secname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b79-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b79-108">Eine Zeichenfolge, die den Abschnitt der INI-Datei angibt, in der sich die handaus Satz Informationen befinden.</span><span class="sxs-lookup"><span data-stu-id="99b79-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="99b79-109">*IniFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b79-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b79-110">Zeichenfolge, die den Namen der INI-Datei des Parsers enthält.</span><span class="sxs-lookup"><span data-stu-id="99b79-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="99b79-111">*htable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="99b79-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b79-112">Handle für eine **handofftable** -Struktur, die von Netzwerkmonitor erstellt und verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="99b79-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="99b79-113">*nmaxprotocolentries* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b79-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b79-114">Zahl, die die maximale Anzahl von Einträgen angibt, die von der Übergabe-Tabelle verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="99b79-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="99b79-115">*Basis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b79-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b79-116">Numerische Basis der Übergabe Satz Nummern, die in der INI-Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="99b79-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b79-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99b79-117">Return value</span></span>

<span data-ttu-id="99b79-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Anzahl der Einträge in der Übergabe-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="99b79-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="99b79-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="99b79-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b79-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99b79-120">Remarks</span></span>

<span data-ttu-id="99b79-121">Die von Netzwerkmonitor erstellte Übergabe Tabelle basiert auf Informationen, die in der-Parser-ini bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="99b79-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="99b79-122">Der zurückgegebene Handle der Übergabe-Tabelle kann dann verwendet werden, um ein Handle für eines der in der Tabelle enthaltenen Protokolle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="99b79-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="99b79-123">Rufen Sie [getprotocolfromtable](getprotocolfromtable.md)auf, um ein Handle für eines dieser Protokolle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99b79-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="99b79-124">Beachten Sie, dass die parseranwendung niemals direkt auf die **handofftable** -Struktur zugreift.</span><span class="sxs-lookup"><span data-stu-id="99b79-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="99b79-125">Diese Struktur wird von Netzwerkmonitor erstellt und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="99b79-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b79-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99b79-126">Requirements</span></span>



| <span data-ttu-id="99b79-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99b79-127">Requirement</span></span> | <span data-ttu-id="99b79-128">Wert</span><span class="sxs-lookup"><span data-stu-id="99b79-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99b79-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99b79-129">Minimum supported client</span></span><br/> | <span data-ttu-id="99b79-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99b79-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="99b79-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99b79-131">Minimum supported server</span></span><br/> | <span data-ttu-id="99b79-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99b79-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="99b79-133">Header</span><span class="sxs-lookup"><span data-stu-id="99b79-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b79-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b79-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="99b79-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99b79-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="99b79-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b79-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="99b79-137">DLL</span><span class="sxs-lookup"><span data-stu-id="99b79-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b79-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b79-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b79-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99b79-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b79-140">Getprotocolfromtable</span><span class="sxs-lookup"><span data-stu-id="99b79-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="99b79-141">Handofftable</span><span class="sxs-lookup"><span data-stu-id="99b79-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




