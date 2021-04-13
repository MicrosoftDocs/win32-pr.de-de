---
description: Die folgenden Konstanten werden von der CNG-Datenschutz-API verwendet.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: CNG-DPAPI-Konstanten (ncryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484291"
---
# <a name="cng-dpapi-constants"></a><span data-ttu-id="b47f2-103">CNG-DPAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b47f2-103">CNG DPAPI Constants</span></span>

<span data-ttu-id="b47f2-104">Die folgenden Konstanten werden von der CNG-Datenschutz-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="b47f2-104">The following constants are used by the CNG Data Protection API.</span></span>

<dl> <dt>

<span data-ttu-id="b47f2-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**ncrypt \_ descr \_ -Trennzeichen \_ und**</span><span class="sxs-lookup"><span data-stu-id="b47f2-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT\_DESCR\_DELIMITER\_AND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-106">L "und"</span><span class="sxs-lookup"><span data-stu-id="b47f2-106">L" AND "</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-107">Kann verwendet werden, um eine Schutz Deskriptorzeichenfolge für ein-und-Trennzeichen zu testen.</span><span class="sxs-lookup"><span data-stu-id="b47f2-107">Can be used to test a protection descriptor string for an AND delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**ncrypt \_ descr \_ gleich**</span><span class="sxs-lookup"><span data-stu-id="b47f2-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT\_DESCR\_EQUAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-109">L "="</span><span class="sxs-lookup"><span data-stu-id="b47f2-109">L"="</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-110">Kann verwendet werden, um eine Schutz Deskriptorzeichenfolge für ein Gleichheitszeichen zu testen.</span><span class="sxs-lookup"><span data-stu-id="b47f2-110">Can be used to test a protection descriptor string for an equals sign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**ncrypt- \_ descr- \_ Trennzeichen \_ oder**</span><span class="sxs-lookup"><span data-stu-id="b47f2-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT\_DESCR\_DELIMITER\_OR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-112">L "or"</span><span class="sxs-lookup"><span data-stu-id="b47f2-112">L" OR "</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-113">Kann verwendet werden, um eine Schutz Deskriptorzeichenfolge für ein-oder-Trennzeichen zu testen.</span><span class="sxs-lookup"><span data-stu-id="b47f2-113">Can be used to test a protection descriptor string for an OR delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="b47f2-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-115">„LOCAL“</span><span class="sxs-lookup"><span data-stu-id="b47f2-115">"LOCAL"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-116">Der lokale Schutz Deskriptor schützt Inhalte für die Anmelde Sitzung, den aktuellen Benutzer oder den lokalen Computer, wie durch die folgenden Konstanten identifiziert:</span><span class="sxs-lookup"><span data-stu-id="b47f2-116">The LOCAL protection descriptor protects content to the logon session, the current user, or the local machine as identified by the following constants:</span></span>

-   <span data-ttu-id="b47f2-117">**lokale Anmeldung mit NCrypt- \_ Schlüssel \_ Schutz \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b47f2-117">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
-   <span data-ttu-id="b47f2-118">**ncrypt- \_ Schlüssel \_ Schutz \_ lokaler \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b47f2-118">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
-   <span data-ttu-id="b47f2-119">**ncrypt- \_ Schlüssel \_ Schutz- \_ lokaler \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="b47f2-119">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="b47f2-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-121">SDDL</span><span class="sxs-lookup"><span data-stu-id="b47f2-121">"SDDL"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-122">Schützt Inhalte in einer SDDL-Zeichenfolge (Security Deskriptor Definition Language), die Sicherheits Deskriptorinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b47f2-122">Protects content to an SDDL (Security Descriptor Definition Language) string that contains security descriptor information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**ncrypt- \_ Schlüssel \_ Schutz Algorithmus- \_ \_ sid**</span><span class="sxs-lookup"><span data-stu-id="b47f2-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-124">SID</span><span class="sxs-lookup"><span data-stu-id="b47f2-124">"SID"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-125">Der SID-Schutz Deskriptor enthält eine Gruppen-oder Prinzipal Identität.</span><span class="sxs-lookup"><span data-stu-id="b47f2-125">The SID protection descriptor contains a group or principal identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**webanmelde Informationen für den NCrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_**</span><span class="sxs-lookup"><span data-stu-id="b47f2-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-127">"Webanmelde Informationen"</span><span class="sxs-lookup"><span data-stu-id="b47f2-127">"WEBCREDENTIALS"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-128">Schützt die Anmelde Informationen für das Webkonto eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b47f2-128">Protects to a user's web account credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**lokale Anmeldung mit NCrypt- \_ Schlüssel \_ Schutz \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b47f2-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-130">Melden</span><span class="sxs-lookup"><span data-stu-id="b47f2-130">"logon"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-131">Schützt Inhalte in der aktuellen Anmelde Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b47f2-131">Protects content to the current logon session.</span></span> <span data-ttu-id="b47f2-132">Benutzer können den geschützten Inhalt nach dem Abmelden oder Neustart nicht entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b47f2-132">Users will not be able to decrypt the protected content after logoff or reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**ncrypt- \_ Schlüssel \_ Schutz- \_ lokaler \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="b47f2-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-134">Computer</span><span class="sxs-lookup"><span data-stu-id="b47f2-134">"machine"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-135">Schützt Inhalt auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="b47f2-135">Protects content to the local computer.</span></span> <span data-ttu-id="b47f2-136">Alle Benutzer auf dem lokalen Computer können den geschützten Inhalt entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b47f2-136">All users on the local computer can decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**ncrypt- \_ Schlüssel \_ Schutz \_ lokaler \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b47f2-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-138">Bedienungs</span><span class="sxs-lookup"><span data-stu-id="b47f2-138">"user"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-139">Schützt Inhalt in der aktuellen Benutzersitzung.</span><span class="sxs-lookup"><span data-stu-id="b47f2-139">Protects content to the current user session.</span></span> <span data-ttu-id="b47f2-140">Nur dieser Benutzer auf dem lokalen Computer ist in der Lage, den geschützten Inhalt zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b47f2-140">Only this user on the local computer will be able to decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS- \_ Schlüssel \_ Schutz \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="b47f2-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-142">"Microsoft Key Protection Provider"</span><span class="sxs-lookup"><span data-stu-id="b47f2-142">"Microsoft Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-143">Stellt den Microsoft-Schlüsselschutz Anbieter dar, der Formate unterstützt, die durch die folgenden Konstanten dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="b47f2-143">Represents the Microsoft key protection provider which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="b47f2-144">**ncrypt- \_ Schlüssel \_ Schutz Algorithmus- \_ \_ sid**</span><span class="sxs-lookup"><span data-stu-id="b47f2-144">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
-   <span data-ttu-id="b47f2-145">**ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="b47f2-145">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
-   <span data-ttu-id="b47f2-146">**ncrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="b47f2-146">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b47f2-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**Windows- \_ Client- \_ Schlüssel \_ Schutz \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="b47f2-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS\_CLIENT\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b47f2-148">"Windows-Client-Schlüsselschutz Anbieter"</span><span class="sxs-lookup"><span data-stu-id="b47f2-148">"Windows Client Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="b47f2-149">Stellt den Microsoft-Schlüsselschutz Anbieter dar, der nur auf dem Client verfügbar ist und die durch die folgenden Konstanten dargestellten Formate unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b47f2-149">Represents the Microsoft key protection provider that is available only on the client and which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="b47f2-150">**webanmelde Informationen für den NCrypt- \_ Schlüssel \_ Schutz \_ Algorithmus \_**</span><span class="sxs-lookup"><span data-stu-id="b47f2-150">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b47f2-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b47f2-151">Requirements</span></span>



| <span data-ttu-id="b47f2-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b47f2-152">Requirement</span></span> | <span data-ttu-id="b47f2-153">Wert</span><span class="sxs-lookup"><span data-stu-id="b47f2-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47f2-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b47f2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b47f2-155">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b47f2-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b47f2-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b47f2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b47f2-157">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b47f2-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b47f2-158">Header</span><span class="sxs-lookup"><span data-stu-id="b47f2-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="b47f2-159"><dt>Ncryptprotect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b47f2-159"><dt>NCryptprotect.h</dt></span></span> </dl> |



 

 




