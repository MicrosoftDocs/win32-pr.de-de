---
description: Ruft bei Bereitstellung eines Jet-Fehlers einen Fehlercode Bezeichner (IDA) und eine unformatierte Meldungs Zeichenfolge ab.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Jeterrrawmessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357935"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="779a6-103">Jeterrrawmessage-Funktion</span><span class="sxs-lookup"><span data-stu-id="779a6-103">JetErrRawMessage function</span></span>

<span data-ttu-id="779a6-104">Ruft bei Bereitstellung eines Jet-Fehlers einen Fehlercode Bezeichner (IDA) und eine unformatierte Meldungs Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="779a6-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="779a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="779a6-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="779a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="779a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="779a6-107">*irre*</span><span class="sxs-lookup"><span data-stu-id="779a6-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-108">Der Jet-Fehler, der den erhaltenen Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="779a6-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="779a6-109">*pida*</span><span class="sxs-lookup"><span data-stu-id="779a6-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-110">Ein Zeiger auf die IDA.</span><span class="sxs-lookup"><span data-stu-id="779a6-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="779a6-111">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="779a6-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-112">Ein Zeiger auf die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="779a6-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="779a6-113">*cbmessage*</span><span class="sxs-lookup"><span data-stu-id="779a6-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-114">Gibt die Anzahl der Bytes in der Fehlermeldung an.</span><span class="sxs-lookup"><span data-stu-id="779a6-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="779a6-115">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="779a6-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-116">Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="779a6-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="779a6-117">*pcontextid*</span><span class="sxs-lookup"><span data-stu-id="779a6-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-118">Ein Zeiger auf den Kontext Bezeichner, der der Hilfedatei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="779a6-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="779a6-119">*pwszhelp/Datei*</span><span class="sxs-lookup"><span data-stu-id="779a6-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="779a6-120">Verweist auf einen Zeiger auf die Datei, in der der Fehler erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="779a6-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="779a6-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="779a6-121">Return value</span></span>

<span data-ttu-id="779a6-122">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **Jet \_ errsuccess** zurück; andernfalls wird eine unformatierte Fehlermeldung zurückgegeben, die die Ursache für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="779a6-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="779a6-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="779a6-123">Remarks</span></span>

<span data-ttu-id="779a6-124">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="779a6-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="779a6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="779a6-125">Requirements</span></span>



| <span data-ttu-id="779a6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="779a6-126">Requirement</span></span> | <span data-ttu-id="779a6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="779a6-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="779a6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="779a6-128">DLL</span></span><br/> | <dl> <span data-ttu-id="779a6-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="779a6-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
