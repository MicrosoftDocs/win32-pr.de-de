---
description: Ruft einen Fehlercode Bezeichner (IDA) ab und erstellt die endgültige Anzeige Zeichenfolge, wenn ein Jet-Fehler und erweiterte Fehlerinformationen bereitgestellt werden.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Jeterrformattedmessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369381"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="1a472-103">Jeterrformattedmessage-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a472-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="1a472-104">Ruft einen Fehlercode Bezeichner (IDA) ab und erstellt die endgültige Anzeige Zeichenfolge, wenn ein Jet-Fehler und erweiterte Fehlerinformationen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1a472-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a472-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a472-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="1a472-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a472-107">*irre*</span><span class="sxs-lookup"><span data-stu-id="1a472-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-108">Die Jet-Fehlernummer, die verwendet wird, um die anzeigbare Fehlermeldung zu suchen und zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="1a472-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-109">*pextendederrorinfo*</span><span class="sxs-lookup"><span data-stu-id="1a472-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-110">Alle Jet-Fehlerinformationen, einschließlich Datenbankname, Tabellenname und geringfügige Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="1a472-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-111">*pida*</span><span class="sxs-lookup"><span data-stu-id="1a472-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-112">Ein Zeiger auf die IDA, die dem spezifischen Fehlercode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a472-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-113">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="1a472-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-114">Ein Zeiger auf die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1a472-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-115">*cbmessage*</span><span class="sxs-lookup"><span data-stu-id="1a472-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-116">Gibt die Anzahl der Bytes in der Fehlermeldung an.</span><span class="sxs-lookup"><span data-stu-id="1a472-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-117">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="1a472-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-118">Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="1a472-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-119">*pcontextid*</span><span class="sxs-lookup"><span data-stu-id="1a472-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-120">Ein Zeiger auf den Kontext Bezeichner, der der Hilfedatei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a472-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="1a472-121">*pwszhelp/Datei*</span><span class="sxs-lookup"><span data-stu-id="1a472-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="1a472-122">Ein Zeiger auf einen Zeiger auf die Datei, in der der Fehler erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="1a472-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a472-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a472-123">Return value</span></span>

<span data-ttu-id="1a472-124">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **Jet \_ errsuccess** zurück; andernfalls wird eine formatierte Fehlermeldung zurückgegeben, die die Ursache für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="1a472-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a472-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a472-125">Remarks</span></span>

<span data-ttu-id="1a472-126">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1a472-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a472-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a472-127">Requirements</span></span>



| <span data-ttu-id="1a472-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a472-128">Requirement</span></span> | <span data-ttu-id="1a472-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1a472-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a472-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1a472-130">DLL</span></span><br/> | <dl> <span data-ttu-id="1a472-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a472-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
