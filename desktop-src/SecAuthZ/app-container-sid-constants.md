---
description: Legen Sie die Anwendungspaket Autorität an.
ms.assetid: 047439EA-789B-41CF-87C2-66CFB3F20908
title: App-Container-sid-Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300b5ed110bbdc88d32efb76b20f5ec0f8454970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363280"
---
# <a name="app-container-sid-constants"></a><span data-ttu-id="cc1b7-103">App-Container-sid-Konstanten</span><span class="sxs-lookup"><span data-stu-id="cc1b7-103">App Container SID Constants</span></span>

<span data-ttu-id="cc1b7-104">Die Anwendungspaket Zertifizierungsstelle wird von den App-Container spezifischen sid-Konstanten vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-104">The app container specific SID constants dictate the application package authority.</span></span> <span data-ttu-id="cc1b7-105">Obwohl ein Entwickler diese Konstanten direkt verwenden kann, müssen die meisten Entwickler diese APP-Container-SIDs nicht definieren.</span><span class="sxs-lookup"><span data-stu-id="cc1b7-105">While a developer can use these constants directly, most developers do not need to define these app container SIDs.</span></span>

<dl> <span data-ttu-id="cc1b7-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**Sicherheit \_ APP- \_ Paket \_ Autorität** ( {0,0,0,0,0,15} ) Sicherheits-App-Paket <span id="SECURITY_APP_PACKAGE_BASE_RID"></span> <span id="security_app_package_base_rid"></span> **\_ \_ \_ Basis \_ RID** (0x00000002l) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span> <span id="security_builtin_app_package_rid_count"></span> **Sicherheit \_ BuiltIn \_ App- \_ Paket Rid- \_ \_ Anzahl** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span> <span id="security_app_package_rid_count"></span> **Sicherheits-APP- \_ \_ Paket Rid- \_ \_ Anzahl** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span> <span id="security_capability_base_rid"></span> **Sicherheits \_ Funktion \_ Basis \_ RID** (0x00000003l) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span> <span id="security_builtin_capability_rid_count"></span> **\_ sicherheitsbuildefähigkeits- \_ RID- \_ \_ Anzahl** <span id="SECURITY_CAPABILITY_RID_COUNT"></span> <span id="security_capability_rid_count"></span> **\_ \_ \_** <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span> <span id="security_builtin_package_any_package"></span> **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc1b7-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**SECURITY\_APP\_PACKAGE\_AUTHORITY** ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span><span id="security_app_package_base_rid"></span>**SECURITY\_APP\_PACKAGE\_BASE\_RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span><span id="security_builtin_app_package_rid_count"></span>**SECURITY\_BUILTIN\_APP\_PACKAGE\_RID\_COUNT** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span><span id="security_app_package_rid_count"></span>**SECURITY\_APP\_PACKAGE\_RID\_COUNT** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span><span id="security_capability_base_rid"></span>**SECURITY\_CAPABILITY\_BASE\_RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span><span id="security_builtin_capability_rid_count"></span>**SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT** (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span><span id="security_capability_rid_count"></span>**SECURITY\_CAPABILITY\_RID\_COUNT** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span><span id="security_builtin_package_any_package"></span>**SECURITY\_BUILTIN\_PACKAGE\_ANY\_PACKAGE** (0x00000001L)</span></span>
</dl>

## <a name="requirements"></a><span data-ttu-id="cc1b7-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc1b7-107">Requirements</span></span>



| <span data-ttu-id="cc1b7-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc1b7-108">Requirement</span></span> | <span data-ttu-id="cc1b7-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cc1b7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1b7-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc1b7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1b7-111">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc1b7-111">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cc1b7-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc1b7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1b7-113">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc1b7-113">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cc1b7-114">Header</span><span class="sxs-lookup"><span data-stu-id="cc1b7-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc1b7-115"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1b7-115"><dt>Winnt.h</dt></span></span> </dl> |



 

 




