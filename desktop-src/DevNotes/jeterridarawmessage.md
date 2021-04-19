---
description: Ruft eine unformatierte Meldungs Zeichenfolge ab, wenn ein Fehlercode Bezeichner (IDA) bereitgestellt wird.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Jeterridarawmessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369239"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="31a68-103">Jeterridarawmessage-Funktion</span><span class="sxs-lookup"><span data-stu-id="31a68-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="31a68-104">Ruft eine unformatierte Meldungs Zeichenfolge ab, wenn ein Fehlercode Bezeichner (IDA) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="31a68-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a68-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="31a68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31a68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a68-107">*I*</span><span class="sxs-lookup"><span data-stu-id="31a68-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="31a68-108">Eine Zahl, die einem bestimmten Fehlercode zugeordnet ist und dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="31a68-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="31a68-109">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="31a68-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="31a68-110">Ein Zeiger auf die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="31a68-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="31a68-111">*cbmessage*</span><span class="sxs-lookup"><span data-stu-id="31a68-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="31a68-112">Gibt die Anzahl der Bytes in der Fehlermeldung an.</span><span class="sxs-lookup"><span data-stu-id="31a68-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="31a68-113">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="31a68-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="31a68-114">Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="31a68-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="31a68-115">*pcontextid*</span><span class="sxs-lookup"><span data-stu-id="31a68-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="31a68-116">Ein Zeiger auf den Kontext Bezeichner, der der Hilfedatei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="31a68-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="31a68-117">*pwszhelp/Datei*</span><span class="sxs-lookup"><span data-stu-id="31a68-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="31a68-118">Ein Zeiger auf einen Zeiger auf die Datei, in der der Fehler erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="31a68-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a68-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31a68-119">Return value</span></span>

<span data-ttu-id="31a68-120">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **Jet \_ errsuccess** zurück; andernfalls wird eine nicht formatierte Meldung zurückgegeben, die die Ursache für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="31a68-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a68-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31a68-121">Remarks</span></span>

<span data-ttu-id="31a68-122">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="31a68-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a68-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a68-123">Requirements</span></span>



| <span data-ttu-id="31a68-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a68-124">Requirement</span></span> | <span data-ttu-id="31a68-125">Wert</span><span class="sxs-lookup"><span data-stu-id="31a68-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31a68-126">DLL</span><span class="sxs-lookup"><span data-stu-id="31a68-126">DLL</span></span><br/> | <dl> <span data-ttu-id="31a68-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a68-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
