---
description: Stellt die Methoden bereit, die WUA zum Erfassen von Informationen über das Endpunkt Token verwenden kann.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Iupdateendpointauthtoken-Schnittstelle (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485139"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="ef796-103">Iupdateendpointauthtoken-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ef796-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="ef796-104">Stellt die Methoden bereit, die WUA zum Erfassen von Informationen über das Endpunkt Token verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ef796-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="ef796-105">Member</span><span class="sxs-lookup"><span data-stu-id="ef796-105">Members</span></span>

<span data-ttu-id="ef796-106">Die **iupdateendpointauthtoken** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ef796-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ef796-107">**Iupdateendpointauthtoken** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ef796-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="ef796-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="ef796-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef796-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="ef796-109">Methods</span></span>

<span data-ttu-id="ef796-110">Die **iupdateendpointauthtoken** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ef796-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="ef796-111">Methode</span><span class="sxs-lookup"><span data-stu-id="ef796-111">Method</span></span>                                                                                | <span data-ttu-id="ef796-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef796-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef796-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="ef796-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="ef796-114">Ruft den Bezeichner des Dienstanbieter ab, der authentifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef796-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="ef796-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="ef796-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="ef796-116">Ruft den Schlüssel ab, der zum Signieren ausgehender Nachrichten zwischen dem Client Computer und dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef796-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="ef796-117">**Datenbankdaten**</span><span class="sxs-lookup"><span data-stu-id="ef796-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="ef796-118">Ruft die XML-Daten (über das Netzwerk gesendet) ab, die das Token darstellen.</span><span class="sxs-lookup"><span data-stu-id="ef796-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="ef796-119">**"An ' referenceattached"**</span><span class="sxs-lookup"><span data-stu-id="ef796-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="ef796-120">Ruft das XML-Format eines angefügten Verweises auf das Token ab.</span><span class="sxs-lookup"><span data-stu-id="ef796-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="ef796-121">**"" Zu "".**</span><span class="sxs-lookup"><span data-stu-id="ef796-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="ef796-122">Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.</span><span class="sxs-lookup"><span data-stu-id="ef796-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="ef796-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="ef796-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="ef796-124">Ruft den Typ des Endpunkt Tokens ab, z. b. ein WS-Security SAML-Token (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="ef796-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef796-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef796-125">Requirements</span></span>



| <span data-ttu-id="ef796-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef796-126">Requirement</span></span> | <span data-ttu-id="ef796-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ef796-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef796-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef796-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ef796-129">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef796-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="ef796-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef796-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ef796-131">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef796-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ef796-132">Header</span><span class="sxs-lookup"><span data-stu-id="ef796-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef796-133"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef796-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef796-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ef796-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef796-135"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef796-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef796-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef796-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef796-137"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef796-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef796-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ef796-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef796-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef796-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
