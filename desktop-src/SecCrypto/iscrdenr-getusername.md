---
description: Ruft den Namen des Benutzers ab, für den die Zertifikat Registrierung vorgesehen ist.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Iscrdenr:: getUserName-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348508"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="21d66-103">Iscrdenr:: getUserName-Methode</span><span class="sxs-lookup"><span data-stu-id="21d66-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="21d66-104">Die **GetUsername** -Methode ruft den Namen des Benutzers ab, für den die Zertifikat Registrierung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="21d66-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="21d66-105">Vor dem Aufrufen dieser Methode müssen Sie den Benutzernamen in einem Aufruf von [**iscrdenr:: selectusername**](iscrdenr-selectusername.md) oder [**iscrdenr:: setUserName**](iscrdenr-setusername.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="21d66-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="21d66-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="21d66-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="21d66-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="21d66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21d66-108">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21d66-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d66-109">Dieser Wert muss entweder NULL (0), der UPN-Name von "SCard \_ Enroll" \_ oder " \_ SCard \_ ENROLL \_ Sam \_ Compatible \_ Name" lauten.</span><span class="sxs-lookup"><span data-stu-id="21d66-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="21d66-110">Wenn dieser Wert "SCard \_ ENROLL \_ UPN \_ Name" ist, gibt **GetUsername** den universellen Prinzipal Namen (UPN) des Benutzers zurück, z someone@example.com . b. "".</span><span class="sxs-lookup"><span data-stu-id="21d66-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="21d66-111">Wenn dieser Wert "SCard \_ ENROLL \_ Sam \_ Compatible \_ Name" ist, gibt die Methode den SAM-Namen (Security Access Manager) des Benutzers im Format "Domänen \\ Benutzer" zurück.</span><span class="sxs-lookup"><span data-stu-id="21d66-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="21d66-112">Wenn dieser Wert 0 (null) ist, gibt die Methode den UPN-Namen des Benutzers zurück, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="21d66-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="21d66-113">Wenn der Benutzer keinen UPN-Namen hat, gibt die Methode den SAM-Namen des Benutzers zurück.</span><span class="sxs-lookup"><span data-stu-id="21d66-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="21d66-114">*pbstrusername* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21d66-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21d66-115">Ein Zeiger auf eine Zeichenfolge, die den Namen des Benutzers zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="21d66-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21d66-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21d66-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="21d66-117">C++</span><span class="sxs-lookup"><span data-stu-id="21d66-117">C++</span></span>

<span data-ttu-id="21d66-118">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="21d66-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="21d66-119">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="21d66-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="21d66-120">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="21d66-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="21d66-121">VB</span><span class="sxs-lookup"><span data-stu-id="21d66-121">VB</span></span>

<span data-ttu-id="21d66-122">Eine Zeichenfolge, die den Namen des Benutzers darstellt.</span><span class="sxs-lookup"><span data-stu-id="21d66-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="21d66-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21d66-123">Remarks</span></span>

<span data-ttu-id="21d66-124">Sie können den Namen des Benutzers angeben, für den die [*Smartcard*](../secgloss/s-gly.md) ausgestellt wird, indem Sie entweder [**iscrdenr:: setUserName**](iscrdenr-setusername.md) oder [**iscrdenr:: selectusername**](iscrdenr-selectusername.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21d66-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="21d66-125">Nachdem ein Benutzername angegeben wurde, kann der zugehörige Wert durch Aufrufen von **GetUsername** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="21d66-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d66-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21d66-126">Requirements</span></span>



| <span data-ttu-id="21d66-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21d66-127">Requirement</span></span> | <span data-ttu-id="21d66-128">Wert</span><span class="sxs-lookup"><span data-stu-id="21d66-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21d66-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21d66-129">Minimum supported client</span></span><br/> | <span data-ttu-id="21d66-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="21d66-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="21d66-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21d66-131">Minimum supported server</span></span><br/> | <span data-ttu-id="21d66-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21d66-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21d66-133">DLL</span><span class="sxs-lookup"><span data-stu-id="21d66-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21d66-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21d66-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="21d66-135">IID</span><span class="sxs-lookup"><span data-stu-id="21d66-135">IID</span></span><br/>                      | <span data-ttu-id="21d66-136">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="21d66-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="21d66-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21d66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d66-138">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="21d66-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="21d66-139">**Iscrdenr:: resetuser**</span><span class="sxs-lookup"><span data-stu-id="21d66-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="21d66-140">**Iscrdenr:: selectusername**</span><span class="sxs-lookup"><span data-stu-id="21d66-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="21d66-141">**Iscrdenr:: setUserName**</span><span class="sxs-lookup"><span data-stu-id="21d66-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
