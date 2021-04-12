---
description: Enthält die Methoden, die zum Aushandeln der Art des Tokens verwendet werden, das zum Authentifizieren des Endpunkts eines Diensts verwendet wird.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Iupdateendpointauthprovider-Schnittstelle (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526684"
---
# <a name="iupdateendpointauthprovider-interface"></a><span data-ttu-id="91f83-103">Iupdateendpointauthprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="91f83-103">IUpdateEndpointAuthProvider interface</span></span>

<span data-ttu-id="91f83-104">Die **iupdateendpointauthprovider** -Schnittstelle enthält die Methoden, die zum Aushandeln des Tokentyps verwendet werden, der zum Authentifizieren des Endpunkts eines Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91f83-104">The **IUpdateEndpointAuthProvider** interface contains the methods used for negotiating which type of token is used for authenticating the endpoint of a service.</span></span>

## <a name="members"></a><span data-ttu-id="91f83-105">Member</span><span class="sxs-lookup"><span data-stu-id="91f83-105">Members</span></span>

<span data-ttu-id="91f83-106">Die **iupdateendpointauthprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="91f83-106">The **IUpdateEndpointAuthProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91f83-107">**Iupdateendpointauthprovider** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91f83-107">**IUpdateEndpointAuthProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="91f83-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="91f83-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="91f83-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="91f83-109">Methods</span></span>

<span data-ttu-id="91f83-110">Die **iupdateendpointauthprovider** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="91f83-110">The **IUpdateEndpointAuthProvider** interface has these methods.</span></span>



| <span data-ttu-id="91f83-111">Methode</span><span class="sxs-lookup"><span data-stu-id="91f83-111">Method</span></span>                                                                                             | <span data-ttu-id="91f83-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91f83-112">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91f83-113">**Getendpointtoken**</span><span class="sxs-lookup"><span data-stu-id="91f83-113">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)                           | <span data-ttu-id="91f83-114">Fordern Sie ein Token für den Endpunkt des Diensts mit den angegebenen Anmelde Informationen an.</span><span class="sxs-lookup"><span data-stu-id="91f83-114">Request a token for the endpoint of the service using the specified credentials.</span></span><br/>    |
| [<span data-ttu-id="91f83-115">**Getpreferredendpointpokentype**</span><span class="sxs-lookup"><span data-stu-id="91f83-115">**GetPreferredEndpointTokenType**</span></span>](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | <span data-ttu-id="91f83-116">Gibt den bevorzugten Authentifizierungstyp für den Endpunkt des Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="91f83-116">Returns the preferred type of authentication token for the endpoint of the service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91f83-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91f83-117">Remarks</span></span>

<span data-ttu-id="91f83-118">WUA Ruft die [**getpreferredendpointdekentype**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) -Methode dieser Schnittstelle auf, um den Aushandlungs Prozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="91f83-118">WUA calls the [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) method of this interface to start the negotiation process.</span></span> <span data-ttu-id="91f83-119">Wenn der-Befehl durchgeführt wird, übergibt WUA den Dienst Bezeichner, den Typ des Endpunkts, der vom Dienst implementiert wird, und die verfügbaren Tokentypen.</span><span class="sxs-lookup"><span data-stu-id="91f83-119">When the call is made WUA passes in the service identifier, the type of endpoint implemented by the service, and the token types that are available.</span></span> <span data-ttu-id="91f83-120">Die Implementierung dieser Schnittstelle gibt dann die Tokentypen zurück, die für die Verwendung bevorzugt werden.</span><span class="sxs-lookup"><span data-stu-id="91f83-120">The implementation of this interface then returns the token types that it preferes to use.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f83-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91f83-121">Requirements</span></span>



| <span data-ttu-id="91f83-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91f83-122">Requirement</span></span> | <span data-ttu-id="91f83-123">Wert</span><span class="sxs-lookup"><span data-stu-id="91f83-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f83-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91f83-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91f83-125">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91f83-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="91f83-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91f83-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91f83-127">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91f83-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="91f83-128">Header</span><span class="sxs-lookup"><span data-stu-id="91f83-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="91f83-129"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="91f83-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="91f83-130">IDL</span><span class="sxs-lookup"><span data-stu-id="91f83-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91f83-131"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91f83-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="91f83-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91f83-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="91f83-133"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91f83-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="91f83-134">DLL</span><span class="sxs-lookup"><span data-stu-id="91f83-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91f83-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91f83-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
