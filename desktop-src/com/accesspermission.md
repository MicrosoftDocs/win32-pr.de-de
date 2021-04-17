---
title: Access spermission
description: Beschreibt die Access Control Liste (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können. Diese ACL wird nur von Anwendungen verwendet, die CoInitializeSecurity nicht aufzurufen.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Access spermission-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474301"
---
# <a name="accesspermission"></a><span data-ttu-id="b0486-105">Access spermission</span><span class="sxs-lookup"><span data-stu-id="b0486-105">AccessPermission</span></span>

<span data-ttu-id="b0486-106">Beschreibt die Access Control Liste (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="b0486-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="b0486-107">Diese ACL wird nur von Anwendungen verwendet, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b0486-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b0486-108">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="b0486-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="b0486-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0486-109">Remarks</span></span>

<span data-ttu-id="b0486-110">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="b0486-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="b0486-111">Es enthält Daten, die die Access Control Liste (ACL) der Prinzipale beschreiben, die auf Instanzen dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="b0486-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="b0486-112">Beim Empfang einer Anforderung zum Herstellen einer Verbindung mit einem vorhandenen Objekt dieser Klasse wird die ACL von der Anwendung geprüft, die aufgerufen wird, während die Identität des Aufrufers angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="b0486-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="b0486-113">Wenn die Zugriffs Überprüfung fehlschlägt, ist die Verbindung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b0486-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="b0486-114">Wenn dieser benannte Wert nicht vorhanden ist, wird die [**DefaultAccessPermission**](defaultaccesspermission.md) -ACL getestet, um zu bestimmen, ob die Verbindung zugelassen werden muss.</span><span class="sxs-lookup"><span data-stu-id="b0486-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="b0486-115">Für Anwendungen, die nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder nicht die [**iglobaloptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) -Schnittstelle verwenden, um die AppID anzugeben, muss die ausführbare Datei der Binärdatei der Anwendung der AppID der Anwendung zugeordnet werden, wie in [**AppID**](appid.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0486-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="b0486-116">Dies ist erforderlich, damit com die AppID der Anwendung finden kann.</span><span class="sxs-lookup"><span data-stu-id="b0486-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0486-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0486-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0486-118">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="b0486-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="b0486-119">**DefaultAccessPermission**</span><span class="sxs-lookup"><span data-stu-id="b0486-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="b0486-120">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="b0486-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 