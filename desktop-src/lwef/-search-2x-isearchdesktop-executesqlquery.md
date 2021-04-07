---
title: ISearchDesktop ExecuteSQLQuery-Methode
description: Nimmt einen Zeiger auf eine Zeichenfolge, die eine Structured Query Language (SQL)-Abfrage und deren Attribute enthält, und gibt einen Zeiger auf die Rückgabe Menge zurück.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- ExecuteSQLQuery-Methode ältere Windows-Umgebungs Features
- ExecuteSQLQuery-Methode Legacy-Windows-Umgebungs Features, ISearchDesktop-Schnittstelle
- ISearchDesktop Interface, ältere Windows-Umgebungs Funktionen, ExecuteSQLQuery-Methode
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724011"
---
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="30fe3-106">ISearchDesktop:: ExecuteSQLQuery-Methode</span><span class="sxs-lookup"><span data-stu-id="30fe3-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="30fe3-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="30fe3-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="30fe3-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="30fe3-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="30fe3-109">Nimmt einen Zeiger auf eine Zeichenfolge, die eine Structured Query Language (SQL)-Abfrage und deren Attribute enthält, und gibt einen Zeiger auf die Rückgabe Menge zurück.</span><span class="sxs-lookup"><span data-stu-id="30fe3-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="30fe3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="30fe3-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="30fe3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="30fe3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30fe3-112">*pdwattributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30fe3-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fe3-113">Typ: **LPCWSTR \***</span><span class="sxs-lookup"><span data-stu-id="30fe3-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="30fe3-114">Eine Zeichenfolge, die die anderen Attribute für die Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="30fe3-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="30fe3-115">*pwszurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30fe3-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fe3-116">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="30fe3-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="30fe3-117">Eine Zeichenfolge, die die SQL-Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="30fe3-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="30fe3-118">*ppidurl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30fe3-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30fe3-119">Typ: **ppidurl \***</span><span class="sxs-lookup"><span data-stu-id="30fe3-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="30fe3-120">Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie einen Zeiger auf das zurückgegebene Recordset.</span><span class="sxs-lookup"><span data-stu-id="30fe3-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30fe3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30fe3-121">Return value</span></span>

<span data-ttu-id="30fe3-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30fe3-122">Type: **HRESULT**</span></span>

<span data-ttu-id="30fe3-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="30fe3-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30fe3-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30fe3-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




