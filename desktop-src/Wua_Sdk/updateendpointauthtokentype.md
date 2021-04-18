---
description: Definiert den Typ der Token, die für die Authentifizierung mit einem Endpunkt verwendet werden können.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Updateendpointauthflkentype-Enumeration (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344035"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="683c9-103">Updateendpointauthflkentype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="683c9-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="683c9-104">Definiert den Typ der Token, die für die Authentifizierung mit einem Endpunkt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="683c9-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="683c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="683c9-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="683c9-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="683c9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="683c9-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattinvalidykentype**</span><span class="sxs-lookup"><span data-stu-id="683c9-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="683c9-108">Es ist kein Authentifizierungs Token erforderlich.</span><span class="sxs-lookup"><span data-stu-id="683c9-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="683c9-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="683c9-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="683c9-110">Das Authentifizierungs Token für den Endpunkt ist ein WS-Security SAML-Token (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="683c9-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="683c9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="683c9-111">Requirements</span></span>



| <span data-ttu-id="683c9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="683c9-112">Requirement</span></span> | <span data-ttu-id="683c9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="683c9-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="683c9-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="683c9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="683c9-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="683c9-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="683c9-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="683c9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="683c9-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="683c9-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="683c9-118">Header</span><span class="sxs-lookup"><span data-stu-id="683c9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="683c9-119"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="683c9-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="683c9-120">IDL</span><span class="sxs-lookup"><span data-stu-id="683c9-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="683c9-121"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="683c9-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




