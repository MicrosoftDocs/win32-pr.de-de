---
description: Erstellt eine Offline Registrierungs Struktur, die einen einzelnen leeren Stamm Schlüssel enthält.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Orkreatehive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370775"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="2beea-103">Orkreatehive-Funktion</span><span class="sxs-lookup"><span data-stu-id="2beea-103">ORCreateHive function</span></span>

<span data-ttu-id="2beea-104">Erstellt eine Offline Registrierungs Struktur, die einen einzelnen leeren Stamm Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="2beea-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2beea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2beea-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="2beea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2beea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2beea-107">*phkResult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2beea-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2beea-108">Verweist auf eine Variable zum Empfangen eines Handles für den Stamm Schlüssel der neu erstellten Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="2beea-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="2beea-109">Wenn die Struktur nicht erstellt werden kann, legt die Funktion diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="2beea-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2beea-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2beea-110">Return value</span></span>

<span data-ttu-id="2beea-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2beea-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="2beea-112">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2beea-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="2beea-113">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2beea-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="2beea-114">Wenn nicht genügend Arbeitsspeicher zum Erstellen der Registrierungs Struktur vorhanden ist, gibt die Funktion einen nicht ausreichenden Arbeitsspeicher für den Fehler zurück \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2beea-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2beea-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2beea-115">Remarks</span></span>

<span data-ttu-id="2beea-116">Die **orkreatehive** -Funktion erstellt eine leere Offline Registrierungs Struktur im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2beea-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="2beea-117">Verwenden Sie die Funktionen [**orkreatekey**](orcreatekey.md) und [**orsetvalue**](orsetvalue.md) , um Schlüssel hinzuzufügen und ihre Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2beea-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2beea-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2beea-118">Requirements</span></span>



| <span data-ttu-id="2beea-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2beea-119">Requirement</span></span> | <span data-ttu-id="2beea-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2beea-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2beea-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2beea-121">Redistributable</span></span><br/> | <span data-ttu-id="2beea-122">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2beea-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="2beea-123">Header</span><span class="sxs-lookup"><span data-stu-id="2beea-123">Header</span></span><br/>          | <dl> <span data-ttu-id="2beea-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2beea-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="2beea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2beea-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="2beea-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2beea-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2beea-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2beea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beea-128">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="2beea-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="2beea-129">**Oropenhive**</span><span class="sxs-lookup"><span data-stu-id="2beea-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="2beea-130">**Orsavehive**</span><span class="sxs-lookup"><span data-stu-id="2beea-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="2beea-131">**Orsetvalue**</span><span class="sxs-lookup"><span data-stu-id="2beea-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
