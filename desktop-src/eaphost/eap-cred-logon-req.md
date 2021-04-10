---
title: EAP- \_ \_ Anmelde- \_ req (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur.
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040376"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="9bc79-104">EAP- \_ \_ Anmelde- \_ req</span><span class="sxs-lookup"><span data-stu-id="9bc79-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="9bc79-105">Die **EAP- \_ \_ Anmelde- \_ req-** Struktur speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP-config- \_ \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9bc79-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="9bc79-106">**EAP- \_ \_ Anmelde- \_ req**</span><span class="sxs-lookup"><span data-stu-id="9bc79-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="9bc79-107">Die **EAP- \_ \_ Anmelde- \_ req-** Struktur speichert EAP-Sicherheits Anmelde Informationen, auf die durch den *pbuidata* -Parameter der [**interaktiven Datenstruktur der EAP- \_ \_ Benutzeroberfläche \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verwiesen wird, wenn der *dwDataType* -Parameter des [**interaktiven EAP-UI- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Anforderungstyp</span><span class="sxs-lookup"><span data-stu-id="9bc79-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="9bc79-108">Die Eingabefelder in dieser Struktur sind identisch mit den Eingabefeldern, die von [**eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9bc79-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="9bc79-109">**EAP \_ Die \_ Anmelde \_** Informationen für die Anmelde Informationen werden in der anfänglichen Anmelde Informationsanforderung verwendet, und EAP-Anmelde Informationen werden während einer Authentifizierung in der Wiederholungs Anforderung für Anmelde Informationen verwendet. [**\_ \_**](eap-cred-req.md)</span><span class="sxs-lookup"><span data-stu-id="9bc79-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bc79-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bc79-110">Remarks</span></span>

<span data-ttu-id="9bc79-111">Die **EAP- \_ \_ Anmelde- \_ req-** Struktur wird zur Unterstützung von einmaligem Anmelden (Single-Sign-on, SSO) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bc79-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="9bc79-112">Die **EAP- \_ \_ Anmelde- \_ req-** Struktur ist identisch mit der [**EAP- \_ \_ Anmelde \_ -**](eap-cred-logon-resp.md) /Struktur-Anmeldungs-Struktur.</span><span class="sxs-lookup"><span data-stu-id="9bc79-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc79-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bc79-113">Requirements</span></span>



| <span data-ttu-id="9bc79-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bc79-114">Requirement</span></span> | <span data-ttu-id="9bc79-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9bc79-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc79-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bc79-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc79-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bc79-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bc79-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bc79-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc79-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bc79-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9bc79-120">Header</span><span class="sxs-lookup"><span data-stu-id="9bc79-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bc79-121"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc79-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc79-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bc79-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc79-123">**\_ \_ Eingabe \_ Feld \_ Array der EAP-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="9bc79-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="9bc79-124">**EAP- \_ Kred- \_ req**</span><span class="sxs-lookup"><span data-stu-id="9bc79-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="9bc79-125">**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="9bc79-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="9bc79-126">**interaktiver EAP- \_ \_ UI- \_ \_ Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9bc79-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="9bc79-127">**Eaphostpeer-querykredentialinputfields**</span><span class="sxs-lookup"><span data-stu-id="9bc79-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





