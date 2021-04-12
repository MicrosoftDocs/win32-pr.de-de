---
description: Definieren Sie für Anwendungen bekannte Funktionen mithilfe der Funktion "Zuordnungs-initializesid".
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Funktionsid-Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218829"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="c87a1-103">Funktionsid-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c87a1-103">Capability SID Constants</span></span>

<span data-ttu-id="c87a1-104">Die funktionsid-Konstanten definieren für Anwendungen bekannte Funktionen mithilfe der Funktion " [**Zuordnungs-initializesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) ".</span><span class="sxs-lookup"><span data-stu-id="c87a1-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="c87a1-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**Sicherheits \_ Funktion \_ Internet \_ Client**</span><span class="sxs-lookup"><span data-stu-id="c87a1-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-106">(0x00000001l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-107">Ein Konto hat Zugriff auf das Internet über einen Client Computer.</span><span class="sxs-lookup"><span data-stu-id="c87a1-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**Sicherheits \_ Funktion \_ Internet \_ Client \_ Server**</span><span class="sxs-lookup"><span data-stu-id="c87a1-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-109">(0x00000002l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-110">Ein Konto hat Zugriff auf das Internet über die Client-und Server Computer.</span><span class="sxs-lookup"><span data-stu-id="c87a1-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**Sicherheits \_ Funktion \_ privater \_ Netzwerk \_ Client \_ Server**</span><span class="sxs-lookup"><span data-stu-id="c87a1-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-112">(0x00000003l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-113">Ein Konto hat Zugriff auf das Internet über ein privates Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c87a1-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_ \_ Bild \_ Bibliothek für Sicherheitsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c87a1-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-115">(0x00000004l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-116">Ein Konto hat Zugriff auf die Bilderbibliothek.</span><span class="sxs-lookup"><span data-stu-id="c87a1-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_ \_ Video \_ Bibliothek zu Sicherheitsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c87a1-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-118">(0x00000005l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-119">Ein Konto hat Zugriff auf die Video Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c87a1-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_ \_ Musik \_ Bibliothek für Sicherheitsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c87a1-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-121">(0x00000006l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-122">Ein Konto hat Zugriff auf die Musikbibliothek.</span><span class="sxs-lookup"><span data-stu-id="c87a1-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**Bibliothek für Sicherheits \_ Funktionen- \_ Dokumente \_**</span><span class="sxs-lookup"><span data-stu-id="c87a1-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-124">(0x00000007l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-125">Ein Konto hat Zugriff auf die Dokumentationsbibliothek.</span><span class="sxs-lookup"><span data-stu-id="c87a1-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**Sicherheits \_ Funktion \_ Enterprise- \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="c87a1-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-127">(0x00000008l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-128">Ein Konto hat Zugriff auf die standardmäßigen Windows-Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="c87a1-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**Sicherheits \_ Funktionen für frei \_ gegebene \_ Benutzer \_ Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="c87a1-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-130">(0x00000009l)</span><span class="sxs-lookup"><span data-stu-id="c87a1-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-131">Ein Konto hat Zugriff auf die freigegebenen Benutzerzertifikate.</span><span class="sxs-lookup"><span data-stu-id="c87a1-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87a1-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**Wechselmedien für Sicherheits \_ Funktionen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c87a1-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87a1-133">(0x0000000al)</span><span class="sxs-lookup"><span data-stu-id="c87a1-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="c87a1-134">Ein Konto hat Zugriff auf den Wechsel Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c87a1-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c87a1-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c87a1-135">Remarks</span></span>

<span data-ttu-id="c87a1-136">Beim Erstellen einer Funktions-sid müssen Sie die Paket Zertifizierungsstelle, die Sicherheits- \_ App- \_ Paket- \_ Autorität {0,0,0,0,0,15} , in den Aufrufen der Funktion "" der Funktion " [**Zuweisung**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) " einschließen.</span><span class="sxs-lookup"><span data-stu-id="c87a1-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="c87a1-137">Darüber hinaus benötigen Sie die grundlegende RID-und RID-Anzahl für die integrierten Funktionen, die Sicherheits \_ Funktion " \_ \_ RID (0x00000003l)" und "Security \_ BuiltIn \_ Capability \_ RID \_ count (2L)".</span><span class="sxs-lookup"><span data-stu-id="c87a1-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="c87a1-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c87a1-138">Requirements</span></span>



| <span data-ttu-id="c87a1-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c87a1-139">Requirement</span></span> | <span data-ttu-id="c87a1-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c87a1-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c87a1-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c87a1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c87a1-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c87a1-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c87a1-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c87a1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c87a1-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c87a1-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c87a1-145">Header</span><span class="sxs-lookup"><span data-stu-id="c87a1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87a1-146"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c87a1-146"><dt>Winnt.h</dt></span></span> </dl> |



 

