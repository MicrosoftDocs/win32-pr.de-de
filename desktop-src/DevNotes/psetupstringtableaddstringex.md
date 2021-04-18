---
description: Fügt einer Tabelle eine Zeichenfolge und zusätzliche Daten hinzu.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: psetupstringtableaddstringex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358326"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="93e8a-103">psetupstringtableaddstringex-Funktion</span><span class="sxs-lookup"><span data-stu-id="93e8a-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="93e8a-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="93e8a-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="93e8a-105">Fügt einer Tabelle eine Zeichenfolge und zusätzliche Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="93e8a-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e8a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="93e8a-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="93e8a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="93e8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e8a-108">*STRINGTABLE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e8a-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8a-109">Ein Zeiger auf die Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="93e8a-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="93e8a-110">*Zeichenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e8a-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8a-111">Ein Zeiger auf die Zeichenfolge, die der Tabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93e8a-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="93e8a-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="93e8a-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8a-113">Der Wert dieses Parameters kann sein `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .</span><span class="sxs-lookup"><span data-stu-id="93e8a-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="93e8a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="93e8a-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="93e8a-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93e8a-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="93e8a-116">"Strauch" <dt>**\_ Mit \_**</dt> Beachtung der Groß-/Kleinschreibung <dt></dt></span><span class="sxs-lookup"><span data-stu-id="93e8a-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="93e8a-117">Bei der Zeichenfolge wird die groß-</span><span class="sxs-lookup"><span data-stu-id="93e8a-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="93e8a-118">"Strauch" <dt>**\_ Neue \_ ExtraData**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="93e8a-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="93e8a-119">Es sind zusätzliche Daten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93e8a-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="93e8a-120">*ExtraData* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="93e8a-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8a-121">Ein optionaler Zeiger auf ein zusätzliches Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="93e8a-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="93e8a-122">*Extradatasize* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="93e8a-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8a-123">Die Größe der zusätzlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="93e8a-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93e8a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93e8a-124">Remarks</span></span>

<span data-ttu-id="93e8a-125">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="93e8a-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e8a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93e8a-126">Requirements</span></span>



| <span data-ttu-id="93e8a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93e8a-127">Requirement</span></span> | <span data-ttu-id="93e8a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="93e8a-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93e8a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="93e8a-129">DLL</span></span><br/> | <dl> <span data-ttu-id="93e8a-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e8a-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
