---
title: Konstanten auf Authentifizierungs Ebene (rpcdce. h)
description: Diese Werte geben eine Authentifizierungs Ebene an, die angibt, welche Menge an Authentifizierung zur Verfügung steht, um die Integrität der Daten zu schützen. Jede Ebene enthält den Schutz, der von den vorherigen Ebenen bereitgestellt wird.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519063"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="0fa09-104">Konstanten auf Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="0fa09-104">Authentication Level Constants</span></span>

<span data-ttu-id="0fa09-105">Diese Werte geben eine Authentifizierungs Ebene an, die angibt, welche Menge an Authentifizierung zur Verfügung steht, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="0fa09-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="0fa09-106">Jede Ebene enthält den Schutz, der von den vorherigen Ebenen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0fa09-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="0fa09-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="0fa09-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="0fa09-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fa09-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="0fa09-109"><dt>**RPC \_ \_ \_ \_ Standardwert für C-authn-Ebene**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="0fa09-110">Weist DCOM an, die Authentifizierungs Ebene mithilfe des normalen sicherheitspausierungsalgorithmus auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0fa09-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="0fa09-111">Weitere Informationen finden Sie unter [sicherheitspauschere Aushandlung](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="0fa09-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="0fa09-112"><dt>**RPC \_ C \_ authn \_ Level \_ None**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="0fa09-113">Führt keine Authentifizierung durch.</span><span class="sxs-lookup"><span data-stu-id="0fa09-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="0fa09-114"><dt>**RPC \_ C \_ authn \_ Level \_ Connect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="0fa09-115">Authentifiziert die Anmelde Informationen des Clients nur, wenn der Client eine Beziehung mit dem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="0fa09-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="0fa09-116">Datagramm-Transporte verwenden \_ stattdessen immer RPC authn \_ Level \_ Pkt.</span><span class="sxs-lookup"><span data-stu-id="0fa09-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="0fa09-117"><dt>**RPC \_ C \_ authn \_ Level \_**</dt> -Befehl <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="0fa09-118">Authentifiziert sich nur zu Beginn jedes Remote Prozedur Aufrufes, wenn der Server die Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="0fa09-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="0fa09-119">Datagramm-Transporte \_ verwenden \_ stattdessen RPC C authn \_ Level \_ Pkt.</span><span class="sxs-lookup"><span data-stu-id="0fa09-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="0fa09-120"><dt>**RPC \_ C \_ authn \_ Level \_ Pkt**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="0fa09-121">Authentifiziert, dass alle empfangenen Daten vom erwarteten Client stammen.</span><span class="sxs-lookup"><span data-stu-id="0fa09-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="0fa09-122"><dt>**RPC \_ \_ \_ \_ Pkt- \_ Integrität der C-authn-Ebene**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="0fa09-123">Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0fa09-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="0fa09-124"><dt>**RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="0fa09-125">Authentifiziert alle vorherigen Ebenen und verschlüsselt den Argument Wert jedes Remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="0fa09-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="0fa09-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fa09-126">Requirements</span></span>



| <span data-ttu-id="0fa09-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fa09-127">Requirement</span></span> | <span data-ttu-id="0fa09-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0fa09-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa09-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fa09-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa09-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fa09-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fa09-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fa09-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa09-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fa09-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0fa09-133">Header</span><span class="sxs-lookup"><span data-stu-id="0fa09-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fa09-134"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fa09-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





