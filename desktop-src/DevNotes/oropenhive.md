---
description: Lädt die angegebene Registrierungs Struktur Datei in den Arbeitsspeicher und überprüft die Hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Oropenhive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367725"
---
# <a name="oropenhive-function"></a><span data-ttu-id="eb05e-103">Oropenhive-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb05e-103">OROpenHive function</span></span>

<span data-ttu-id="eb05e-104">Lädt die angegebene Registrierungs Struktur Datei in den Arbeitsspeicher und überprüft die Hive.</span><span class="sxs-lookup"><span data-stu-id="eb05e-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb05e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb05e-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="eb05e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb05e-107">*lphivepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb05e-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb05e-108">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen der Hive-Registrierungsdatei angibt, die in den Arbeitsspeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb05e-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="eb05e-109">Dabei kann es sich um eine Hive-Datei handeln, die mit der [**orsavehive**](orsavehive.md) -Funktion gespeichert oder mit der [regsavekey](/windows/win32/api/winreg/nf-winreg-regsavekeya) -Funktion oder der [regsavekeyex](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="eb05e-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="eb05e-110">Die Datei muss weniger als 4 GB groß sein, und der Aufrufer muss über Datei \_ Lese \_ Zugriff auf die Datei verfügen.</span><span class="sxs-lookup"><span data-stu-id="eb05e-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="eb05e-111">Weitere Informationen finden Sie unter [Datei Sicherheit und Zugriffsrechte](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="eb05e-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb05e-112">*phkResult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eb05e-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb05e-113">Ein Zeiger auf eine Variable, die ein Handle für den Stamm Schlüssel der geladenen Offline Registrierungs Struktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="eb05e-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="eb05e-114">Wenn die Hive-Registrierungsdatei nicht geöffnet werden kann oder die Validierung fehlschlägt, legt die Funktion diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="eb05e-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb05e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb05e-115">Return value</span></span>

<span data-ttu-id="eb05e-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="eb05e-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="eb05e-117">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb05e-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="eb05e-118">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb05e-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="eb05e-119">Folgende Fehlercodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="eb05e-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="eb05e-120">Wenn die Datei leer oder größer als 4 GB ist, gibt die Funktion den Fehler \_ baddb zurück.</span><span class="sxs-lookup"><span data-stu-id="eb05e-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="eb05e-121">Wenn der Aufrufer nicht über die erforderlichen Zugriffsrechte verfügt, um die Datei zu öffnen, gibt die Funktion den Fehler \_ Zugriff \_ verweigert zurück.</span><span class="sxs-lookup"><span data-stu-id="eb05e-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="eb05e-122">Wenn die Überprüfung der Registrierungs Struktur fehlschlägt, gibt die Funktion die Fehlermeldung \_ nicht die \_ Registrierungs \_ Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="eb05e-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb05e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb05e-123">Remarks</span></span>

<span data-ttu-id="eb05e-124">Die **oropenhive** -Funktion ist die einzige Offline-Registrierungsfunktion, die eine Registrierungs Struktur überprüft.</span><span class="sxs-lookup"><span data-stu-id="eb05e-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="eb05e-125">Wenn die Überprüfung fehlschlägt, wird nicht versucht, die Struktur zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="eb05e-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb05e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb05e-126">Requirements</span></span>



| <span data-ttu-id="eb05e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb05e-127">Requirement</span></span> | <span data-ttu-id="eb05e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="eb05e-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb05e-129">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="eb05e-129">Redistributable</span></span><br/> | <span data-ttu-id="eb05e-130">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="eb05e-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="eb05e-131">Header</span><span class="sxs-lookup"><span data-stu-id="eb05e-131">Header</span></span><br/>          | <dl> <span data-ttu-id="eb05e-132"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb05e-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb05e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eb05e-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="eb05e-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb05e-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb05e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb05e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb05e-136">**Orclosehive**</span><span class="sxs-lookup"><span data-stu-id="eb05e-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="eb05e-137">**Orkreatehive**</span><span class="sxs-lookup"><span data-stu-id="eb05e-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="eb05e-138">**Orsavehive**</span><span class="sxs-lookup"><span data-stu-id="eb05e-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="eb05e-139">Regsavekey</span><span class="sxs-lookup"><span data-stu-id="eb05e-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="eb05e-140">Regsavekeyex</span><span class="sxs-lookup"><span data-stu-id="eb05e-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
