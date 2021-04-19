---
description: Gibt den Namen des Benutzers an, für den die Zertifikat Registrierung vorgesehen ist.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Iscrdenr:: setUserName-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373366"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="d0f56-103">Iscrdenr:: setUserName-Methode</span><span class="sxs-lookup"><span data-stu-id="d0f56-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="d0f56-104">Die **setUserName** -Methode gibt den Namen des Benutzers an, für den die Zertifikat Registrierung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="d0f56-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0f56-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="d0f56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0f56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f56-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f56-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f56-108">Bei diesem Wert muss es sich um den Namen der "SCard \_ ENROLL \_ UPN" \_ (definiert als 1) oder "SCard \_ Enroll" \_ Sam- \_ kompatiblen \_ namens (definiert als 2) handeln.</span><span class="sxs-lookup"><span data-stu-id="d0f56-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="d0f56-109">Legen Sie diesen Wert auf \_ "SCard ENROLL \_ UPN Name" fest \_ , wenn der in *bstrUsername* angegebene Name der universelle Prinzipal Name des Benutzers (z. b. "") ist someone@example.com .</span><span class="sxs-lookup"><span data-stu-id="d0f56-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="d0f56-110">Der UPN-Name des Benutzers muss einem vorhandenen Sam-Namen (Security Access Manager) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d0f56-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="d0f56-111">Legen Sie diesen Wert auf \_ "SCard ENROLL \_ Sam \_ Compatible Name" fest \_ , wenn der in *bstrUsername* angegebene Name dem Sam-Namen des Benutzers im Format "Domänen \\ Benutzer" entspricht.</span><span class="sxs-lookup"><span data-stu-id="d0f56-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="d0f56-112">*bstrUsername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f56-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f56-113">Name des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d0f56-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f56-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0f56-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="d0f56-115">VB</span><span class="sxs-lookup"><span data-stu-id="d0f56-115">VB</span></span>

<span data-ttu-id="d0f56-116">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="d0f56-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="d0f56-117">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="d0f56-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d0f56-118">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="d0f56-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f56-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0f56-119">Remarks</span></span>

<span data-ttu-id="d0f56-120">Mit dieser Methode können Sie den Benutzernamen angeben, der als [*Smartcard*](../secgloss/s-gly.md)ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0f56-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d0f56-121">Eine Alternative zu " **setUserName** " ist " [**iscrdenr:: selectusername**](iscrdenr-selectusername.md)".</span><span class="sxs-lookup"><span data-stu-id="d0f56-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="d0f56-122">Nachdem ein Benutzername angegeben wurde, kann der zugehörige Wert durch Aufrufen von [**GetUsername**](iscrdenr-getusername.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d0f56-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f56-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0f56-123">Requirements</span></span>



| <span data-ttu-id="d0f56-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0f56-124">Requirement</span></span> | <span data-ttu-id="d0f56-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d0f56-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f56-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0f56-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f56-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d0f56-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d0f56-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0f56-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f56-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0f56-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0f56-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f56-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0f56-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f56-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0f56-132">IID</span><span class="sxs-lookup"><span data-stu-id="d0f56-132">IID</span></span><br/>                      | <span data-ttu-id="d0f56-133">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="d0f56-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d0f56-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0f56-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f56-135">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="d0f56-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="d0f56-136">**Iscrdenr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="d0f56-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="d0f56-137">**Iscrdenr:: resetuser**</span><span class="sxs-lookup"><span data-stu-id="d0f56-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="d0f56-138">**Iscrdenr:: selectusername**</span><span class="sxs-lookup"><span data-stu-id="d0f56-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
