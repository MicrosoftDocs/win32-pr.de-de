---
title: EAP- \_ Anmelde-e- \_ Mail-Anmeldung \_ (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur. | EAP- \_ Anmelde-e- \_ Mail-Anmeldung \_ (eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351885"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="5b107-105">EAP- \_ \_ Anmelde- \_ Anmeldedienst (e)</span><span class="sxs-lookup"><span data-stu-id="5b107-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="5b107-106">Die **EAP- \_ \_ Anmelde- \_** /Struktur-Anmeldeinformationen speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP-config- \_ \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5b107-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="5b107-107">**EAP- \_ \_ Anmelde- \_ Anmeldedienst (e)**</span><span class="sxs-lookup"><span data-stu-id="5b107-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="5b107-108">Die **EAP- \_ \_ Anmelde- \_** /Struktur-Anmeldungs-Struktur speichert EAP-Sicherheits Anmelde Informationen, auf die der *pbuidata* -Parameter der [**\_ interaktiven \_ Benutzeroberflächen \_ Datenstruktur von EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verweist, wenn der *dwDataType* -Parameter des [**interaktiven EAP-UI- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Anforderungstyp</span><span class="sxs-lookup"><span data-stu-id="5b107-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="5b107-109">Die Eingabefelder in dieser Struktur sind identisch mit den Eingabefeldern, die von [**eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b107-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="5b107-110">**EAP \_ Die \_ Anmelde \_** Informationen für die Anmelde Informationen werden in der ersten Anmelde Informationsanforderung verwendet, und EAP-Anmelde Informationen werden während einer Authentifizierung in der Wiederholungs Anforderung für Anmelde Informationen verwendet. [**\_ \_**](eap-cred-resp.md)</span><span class="sxs-lookup"><span data-stu-id="5b107-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b107-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b107-111">Remarks</span></span>

<span data-ttu-id="5b107-112">Die **EAP- \_ Anmelde- \_ /Struktur-Anmeldung \_** wird zur Unterstützung von einmaligem Anmelden (Single-Sign-on, SSO) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b107-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="5b107-113">Die **EAP- \_ \_ Anmelde- \_** /Struktur-Anmeldungs-Struktur ist identisch mit der [**EAP- \_ \_ Anmelde- \_ req-**](eap-cred-logon-req.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="5b107-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b107-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b107-114">Requirements</span></span>



| <span data-ttu-id="5b107-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b107-115">Requirement</span></span> | <span data-ttu-id="5b107-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5b107-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b107-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b107-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5b107-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b107-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b107-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b107-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5b107-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b107-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b107-121">Header</span><span class="sxs-lookup"><span data-stu-id="5b107-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b107-122"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b107-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b107-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b107-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b107-124">**Eaphostpeer-querykredentialinputfields**</span><span class="sxs-lookup"><span data-stu-id="5b107-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="5b107-125">**\_ \_ Eingabe \_ Feld \_ Array der EAP-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="5b107-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="5b107-126">**EAP- \_ \_ Anmelde- \_ req**</span><span class="sxs-lookup"><span data-stu-id="5b107-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="5b107-127">**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="5b107-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="5b107-128">**interaktiver EAP- \_ \_ UI- \_ \_ Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5b107-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





