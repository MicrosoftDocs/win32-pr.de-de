---
title: Benutzerdefinierte WinNT-Benutzereigenschaften
description: Der WinNT-Anbieter stellt die folgenden benutzerdefinierten Eigenschaften für die User-Klasse zur Verfügung. Auf Sie kann über die Methoden "IADs. Get" und "IADs. Put" zugegriffen werden. Weitere Informationen finden Sie in der Benutzer \_ Info \_ 3-Struktur.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Benutzerdefinierte WinNT-Benutzereigenschaften ADSI
- WinNT-Anbieter ADSI, Benutzerobjekt, benutzerdefinierte Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949117"
---
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="f3068-107">Benutzerdefinierte WinNT-Benutzereigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3068-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="f3068-108">Der WinNT-Anbieter stellt die folgenden benutzerdefinierten Eigenschaften für die User-Klasse zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f3068-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="f3068-109">Auf Sie kann über die Methoden " [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) " und " [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) " zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="f3068-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="f3068-110">Weitere Informationen finden Sie in der [**Benutzer \_ Info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f3068-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="f3068-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3068-111">Property</span></span>            | <span data-ttu-id="f3068-112">type</span><span class="sxs-lookup"><span data-stu-id="f3068-112">Type</span></span>         | <span data-ttu-id="f3068-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3068-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3068-114">**Homedirdrive**</span><span class="sxs-lookup"><span data-stu-id="f3068-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="f3068-115">String</span><span class="sxs-lookup"><span data-stu-id="f3068-115">String</span></span>       | <span data-ttu-id="f3068-116">Das Basisverzeichnis des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f3068-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="f3068-117">Dies ist ein Zeiger auf eine Unicode-Zeichenfolge, die den Pfad des Basisverzeichnisses angibt.</span><span class="sxs-lookup"><span data-stu-id="f3068-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="f3068-118">Die Zeichenfolge kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f3068-118">The string can be **null**.</span></span> <span data-ttu-id="f3068-119">Siehe Beispiel in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="f3068-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="f3068-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="f3068-120">**ObjectSID**</span></span>       | <span data-ttu-id="f3068-121">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f3068-121">Octet String</span></span> | <span data-ttu-id="f3068-122">Objekt-SID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f3068-122">Object SID of the user.</span></span> <span data-ttu-id="f3068-123">Ein Beispiel zum Abrufen der Objekt-SID mithilfe des WinNT-Anbieters finden Sie unter [Objekt-sid (WinNT-Anbieter)](object-sid.md) .</span><span class="sxs-lookup"><span data-stu-id="f3068-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="f3068-124">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="f3068-124">**Parameters**</span></span>      | <span data-ttu-id="f3068-125">String</span><span class="sxs-lookup"><span data-stu-id="f3068-125">String</span></span>       | <span data-ttu-id="f3068-126">Parameter des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f3068-126">Parameters of the user.</span></span> <span data-ttu-id="f3068-127">Verweist auf eine Unicode-Zeichenfolge, die für die Verwendung durch Anwendungen reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="f3068-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="f3068-128">Diese Zeichenfolge kann eine NULL-Zeichenfolge oder eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="f3068-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="f3068-129">Microsoft-Produkte verwenden dieses Mitglied zum Speichern von Benutzer Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="f3068-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="f3068-130">Diese Eigenschaft kann nur von einer Anwendung während der Installation geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f3068-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="f3068-131">**PasswordAge**</span><span class="sxs-lookup"><span data-stu-id="f3068-131">**PasswordAge**</span></span>     | <span data-ttu-id="f3068-132">Time</span><span class="sxs-lookup"><span data-stu-id="f3068-132">Time</span></span>         | <span data-ttu-id="f3068-133">Die Zeitspanne des verwendeten Kennworts.</span><span class="sxs-lookup"><span data-stu-id="f3068-133">Time duration of the password in use.</span></span> <span data-ttu-id="f3068-134">Diese Eigenschaft gibt die Anzahl der Sekunden an, die seit der letzten Änderung des Kennworts verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="f3068-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="f3068-135">**Passwordexpired**</span><span class="sxs-lookup"><span data-stu-id="f3068-135">**PasswordExpired**</span></span> | <span data-ttu-id="f3068-136">Integer</span><span class="sxs-lookup"><span data-stu-id="f3068-136">Integer</span></span>      | <span data-ttu-id="f3068-137">Gibt an, wann das Kennwort abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="f3068-137">Tells when the password was expired.</span></span> <span data-ttu-id="f3068-138">Wenn Sie Get verwenden, wird NULL zurückgegeben, wenn das Kennwort nicht abgelaufen ist, oder ungleich 0 (null), wenn das Kennwort abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="f3068-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="f3068-139">Siehe Beispiel in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="f3068-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="f3068-140">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="f3068-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="f3068-141">Integer</span><span class="sxs-lookup"><span data-stu-id="f3068-141">Integer</span></span>      | <span data-ttu-id="f3068-142">Die primäre Gruppen-ID des Benutzers, z. b. Domänen-Benutzergruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="f3068-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="f3068-143">Siehe Beispiel in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="f3068-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f3068-144">**UserFlags**</span><span class="sxs-lookup"><span data-stu-id="f3068-144">**UserFlags**</span></span>       | <span data-ttu-id="f3068-145">Integer</span><span class="sxs-lookup"><span data-stu-id="f3068-145">Integer</span></span>      | <span data-ttu-id="f3068-146">Benutzerflag, das in [**ADS \_ User \_ Flag \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)-Aufzählung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3068-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="f3068-147">Ein Beispiel für die Verwendung von UserFlags finden Sie unter [Kennwort läuft nie ab (WinNT-Anbieter)](winnt-password-never-expires.md) .</span><span class="sxs-lookup"><span data-stu-id="f3068-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="f3068-148">In diesem Beispiel wird gezeigt, wie das Start Laufwerks Verzeichnis eines Benutzers festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f3068-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="f3068-149">Dieses Beispiel zeigt, wie Sie passwordexpired verwenden können, um einen Benutzer zu zwingen, das Kennwort bei der nächsten Anmeldung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f3068-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="f3068-150">Dieses Beispiel zeigt, wie Sie die primäre Gruppe des Benutzers erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3068-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 