---
description: Zeigt eine Benutzeroberfläche zum auswählen an, sodass ein Benutzername ausgewählt werden kann.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Iscrdenr:: selectusername-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353887"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="824c4-103">Iscrdenr:: selectusername-Methode</span><span class="sxs-lookup"><span data-stu-id="824c4-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="824c4-104">Die **selectusername** -Methode zeigt eine Benutzeroberfläche zum **auswählen** an, sodass ein Benutzername ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="824c4-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="824c4-105">Der Benutzername gilt für den Benutzer, für den die Zertifikat Registrierung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="824c4-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="824c4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="824c4-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="824c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="824c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="824c4-108">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="824c4-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824c4-109">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="824c4-109">Reserved for future use.</span></span> <span data-ttu-id="824c4-110">Legen Sie diesen Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="824c4-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="824c4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="824c4-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="824c4-112">VB</span><span class="sxs-lookup"><span data-stu-id="824c4-112">VB</span></span>

<span data-ttu-id="824c4-113">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="824c4-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="824c4-114">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="824c4-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="824c4-115">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="824c4-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="824c4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="824c4-116">Remarks</span></span>

<span data-ttu-id="824c4-117">Verwenden Sie diese Methode, um den Namen des Benutzers auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="824c4-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="824c4-118">Nachdem ein Benutzername ausgewählt wurde, kann der zugehörige Wert durch Aufrufen der [**iscrdenr:: GetUserName**](iscrdenr-getusername.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="824c4-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="824c4-119">Eine Alternative zum Verwenden der Benutzeroberfläche "Select User" ist das Angeben eines Benutzers durch Aufrufen der [**iscrdenr:: setUserName**](iscrdenr-setusername.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="824c4-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="824c4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="824c4-120">Requirements</span></span>



| <span data-ttu-id="824c4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="824c4-121">Requirement</span></span> | <span data-ttu-id="824c4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="824c4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="824c4-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="824c4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="824c4-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="824c4-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="824c4-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="824c4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="824c4-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="824c4-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="824c4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="824c4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="824c4-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="824c4-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="824c4-129">IID</span><span class="sxs-lookup"><span data-stu-id="824c4-129">IID</span></span><br/>                      | <span data-ttu-id="824c4-130">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="824c4-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="824c4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="824c4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824c4-132">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="824c4-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="824c4-133">**Iscrdenr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="824c4-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="824c4-134">**Iscrdenr:: resetuser**</span><span class="sxs-lookup"><span data-stu-id="824c4-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="824c4-135">**Iscrdenr:: setUserName**</span><span class="sxs-lookup"><span data-stu-id="824c4-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




