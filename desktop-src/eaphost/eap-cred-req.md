---
title: EAP- \_ Kred \_ req (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur. | EAP- \_ Kred \_ req (eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367320"
---
# <a name="eap_cred_req"></a><span data-ttu-id="ee2cc-105">EAP- \_ Kred- \_ req</span><span class="sxs-lookup"><span data-stu-id="ee2cc-105">EAP\_CRED\_REQ</span></span>

<span data-ttu-id="ee2cc-106">Die **EAP-Struktur " \_ \_ req req** " speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP- \_ config- \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ee2cc-106">The **EAP\_CRED\_REQ** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

<span data-ttu-id="ee2cc-107">**EAP- \_ Kred- \_ req**</span><span class="sxs-lookup"><span data-stu-id="ee2cc-107">**EAP\_CRED\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="ee2cc-108">Die **EAP-Struktur " \_ \_ req req** " speichert sowohl die alten als auch die neuen EAP-Sicherheits Anmelde Informationen, auf die durch den *pbuidata* -Parameter der [**interaktiven Datenstruktur der EAP- \_ \_ Benutzeroberfläche \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verwiesen wird, wenn der *dwDataType* -Parameter des [**interaktiven EAP-Benutzeroberflächen- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen</span><span class="sxs-lookup"><span data-stu-id="ee2cc-108">The **EAP\_CRED\_REQ** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee2cc-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee2cc-109">Remarks</span></span>

<span data-ttu-id="ee2cc-110">Die **EAP-Struktur " \_ \_ req req** " wird zur Unterstützung von einmaligem Anmelden (Single Sign-on, SSO) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee2cc-110">The **EAP\_CRED\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="ee2cc-111">Die **EAP-Struktur " \_ \_ req req** " ist identisch mit der " [**EAP" \_ - \_**](eap-cred-resp.md) Struktur "|".</span><span class="sxs-lookup"><span data-stu-id="ee2cc-111">The **EAP\_CRED\_REQ** structure is identical to the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2cc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee2cc-112">Requirements</span></span>



| <span data-ttu-id="ee2cc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee2cc-113">Requirement</span></span> | <span data-ttu-id="ee2cc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ee2cc-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2cc-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee2cc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2cc-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee2cc-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee2cc-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee2cc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2cc-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee2cc-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee2cc-119">Header</span><span class="sxs-lookup"><span data-stu-id="ee2cc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee2cc-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cc-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee2cc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee2cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2cc-122">EAPHost-Supplicant-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ee2cc-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="ee2cc-123">**EAP-Benutzer \_ -e/a \_**</span><span class="sxs-lookup"><span data-stu-id="ee2cc-123">**EAP\_CRED\_RESP**</span></span>](eap-cred-resp.md)
</dt> <dt>

[<span data-ttu-id="ee2cc-124">**EAP- \_ \_ ablaufungsablauf- \_ req**</span><span class="sxs-lookup"><span data-stu-id="ee2cc-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="ee2cc-125">[**EAP- \_ \_ Ablaufs Ablauf (e) \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee2cc-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ee2cc-126">**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="ee2cc-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="ee2cc-127">SSO und PLAP</span><span class="sxs-lookup"><span data-stu-id="ee2cc-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

