---
description: Ruft Daten aus den angegebenen Einträgen ab, die zu einem exe-Eintrag gehören.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Sdbquerydataextagid-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392938"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="0c794-103">Sdbquerydataextagid-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c794-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="0c794-104">Ruft Daten aus den angegebenen Einträgen ab, die zu einem exe-Eintrag gehören.</span><span class="sxs-lookup"><span data-stu-id="0c794-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c794-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c794-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="0c794-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c794-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c794-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c794-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0c794-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0c794-109">*tiexe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c794-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-110">Die [**TagID**](tagid.md) des exe-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="0c794-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="0c794-111">*lpszdataname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0c794-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-112">Der Name des Daten Eintrags, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c794-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="0c794-113">Wenn Sie mehrere Einträge angeben möchten, trennen Sie die Namen durch den umgekehrten Schrägstrich (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="0c794-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="0c794-114">Wenn dieser Parameter **null** ist, versucht die Funktion, alle Dateneinträge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0c794-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="0c794-115">*lpdwdatatype* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="0c794-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-116">Der Datentyp der zurückgegebenen Einträge.</span><span class="sxs-lookup"><span data-stu-id="0c794-116">The data type of the returned entries.</span></span> <span data-ttu-id="0c794-117">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0c794-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="0c794-118">**REG- \_ Binärdatei**</span><span class="sxs-lookup"><span data-stu-id="0c794-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="0c794-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0c794-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="0c794-120">**REG \_ \_ MultiSZ**</span><span class="sxs-lookup"><span data-stu-id="0c794-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="0c794-121">**REG \_ None**</span><span class="sxs-lookup"><span data-stu-id="0c794-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="0c794-122">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="0c794-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="0c794-123">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="0c794-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0c794-124">*lpBuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c794-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-125">Der Puffer, der die Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="0c794-125">The buffer that receives the data.</span></span> <span data-ttu-id="0c794-126">Wenn der Puffer nicht groß genug ist, um die Daten zu enthalten, schlägt die Funktion fehl und gibt einen **fehlerhaften \_ \_ Puffer** zurück.</span><span class="sxs-lookup"><span data-stu-id="0c794-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="0c794-127">*lpcbbuffersize* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="0c794-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-128">Die Größe des *lpBuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0c794-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0c794-129">*ptidata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c794-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c794-130">Die [**TagID**](tagid.md) des Daten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="0c794-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c794-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c794-131">Return value</span></span>

<span data-ttu-id="0c794-132">Diese Funktion gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0c794-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="0c794-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0c794-133">Return code</span></span>                                                                                                    | <span data-ttu-id="0c794-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c794-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c794-135"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="0c794-136">Mindestens ein Eingabeparameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="0c794-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="0c794-137"><dt>**Fehler bei \_ interner \_ DB- \_ Datenbank.**</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="0c794-138">Es wurden keine Dateneinträge für den exe-Eintrag gefunden.</span><span class="sxs-lookup"><span data-stu-id="0c794-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="0c794-139"><dt>**Fehler \_ beim \_ Puffer.**</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="0c794-140">Der Puffer ist nicht groß genug, um die Dateneinträge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c794-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="0c794-141"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="0c794-142">Die Speicher Belegung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="0c794-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="0c794-143"><dt>**Fehler \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="0c794-144">Ein Dateneintrag mit dem Namen *lpszdataname* wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="0c794-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="0c794-145"><dt>**Fehler \_ erfolgreich**</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="0c794-146">Die Funktion wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0c794-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="0c794-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c794-147">Requirements</span></span>



| <span data-ttu-id="0c794-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c794-148">Requirement</span></span> | <span data-ttu-id="0c794-149">Wert</span><span class="sxs-lookup"><span data-stu-id="0c794-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c794-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c794-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0c794-151">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c794-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c794-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c794-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0c794-153">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c794-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c794-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0c794-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c794-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c794-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




