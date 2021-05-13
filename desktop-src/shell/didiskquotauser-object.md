---
description: Ermöglicht es einem Client, die Kontingenteinstellungen für globale Datenträger eines NTFS-Volumes zu verwalten. Dieses Objekt stellt die grundlegende Funktionalität der DIDiskQuotaUser-Schnittstelle für Skripts und Microsoft Visual Basic-basierten Anwendungen zur Verfügung.
title: DIDiskQuotaUser-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843241"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="34c29-104">DIDiskQuotaUser-Objekt</span><span class="sxs-lookup"><span data-stu-id="34c29-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="34c29-105">Ermöglicht es einem Client, die Kontingenteinstellungen für globale Datenträger eines NTFS-Volumes zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="34c29-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="34c29-106">Dieses Objekt stellt die grundlegende Funktionalität der **DIDiskQuotaUser-Schnittstelle** für Skripts und Microsoft Visual Basic-basierten Anwendungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="34c29-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="34c29-107">Member</span><span class="sxs-lookup"><span data-stu-id="34c29-107">Members</span></span>

<span data-ttu-id="34c29-108">Das **DIDiskQuotaUser-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="34c29-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="34c29-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="34c29-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="34c29-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34c29-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34c29-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="34c29-111">Methods</span></span>

<span data-ttu-id="34c29-112">Das **DIDiskQuotaUser-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="34c29-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="34c29-113">Methode</span><span class="sxs-lookup"><span data-stu-id="34c29-113">Method</span></span>                                           | <span data-ttu-id="34c29-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34c29-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="34c29-115">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="34c29-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="34c29-116">Leert die zwischengespeicherten Benutzerinformationen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="34c29-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="34c29-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34c29-117">Properties</span></span>

<span data-ttu-id="34c29-118">Das **DIDiskQuotaUser-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34c29-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="34c29-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="34c29-119">Property</span></span>                                                                        | <span data-ttu-id="34c29-120">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="34c29-120">Access type</span></span>           | <span data-ttu-id="34c29-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34c29-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34c29-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="34c29-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="34c29-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-123">Read-only</span></span><br/>  | <span data-ttu-id="34c29-124">Ruft den Namen des Kontocontainers des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="34c29-125">**AccountStatus**</span><span class="sxs-lookup"><span data-stu-id="34c29-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="34c29-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-126">Read-only</span></span><br/>  | <span data-ttu-id="34c29-127">Ruft den Status des Benutzerkontos ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="34c29-128">**Displayname**</span><span class="sxs-lookup"><span data-stu-id="34c29-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="34c29-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-129">Read-only</span></span><br/>  | <span data-ttu-id="34c29-130">Ruft den Anzeigenamen des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="34c29-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="34c29-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="34c29-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-132">Read-only</span></span><br/>  | <span data-ttu-id="34c29-133">Ruft eine ID ab, die den Benutzer eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="34c29-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="34c29-134">**LogonName**</span><span class="sxs-lookup"><span data-stu-id="34c29-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="34c29-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-135">Read-only</span></span><br/>  | <span data-ttu-id="34c29-136">Ruft den Anmeldekontonamen des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="34c29-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="34c29-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="34c29-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34c29-138">Read/write</span></span><br/> | <span data-ttu-id="34c29-139">Legt das aktuelle [**Kontingentlimit**](diskquotacontrol-object.md)des Benutzers fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="34c29-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="34c29-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="34c29-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-141">Read-only</span></span><br/>  | <span data-ttu-id="34c29-142">Ruft die aktuelle [**Kontingentgrenze**](diskquotacontrol-object.md) des Benutzers als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="34c29-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="34c29-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="34c29-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="34c29-144">Read/write</span></span><br/> | <span data-ttu-id="34c29-145">Legt den Warnungsschwellenwert des Benutzers in Bytes fest oder ruft den Warnungsschwellenwert ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="34c29-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="34c29-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="34c29-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-147">Read-only</span></span><br/>  | <span data-ttu-id="34c29-148">Ruft den Warnungsschwellenwert des Benutzers als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="34c29-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="34c29-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="34c29-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-150">Read-only</span></span><br/>  | <span data-ttu-id="34c29-151">Ruft die aktuelle Datenträgerverwendung des Benutzers in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="34c29-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="34c29-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="34c29-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c29-153">Read-only</span></span><br/>  | <span data-ttu-id="34c29-154">Ruft die aktuelle Datenträgerverwendung des Benutzers als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="34c29-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="34c29-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34c29-155">Remarks</span></span>

<span data-ttu-id="34c29-156">Jedem Benutzer auf dem Volume, das vom [**DiskQuotaControl-Objekt**](diskquotacontrol-object.md) verwaltet wird, ist ein **DIDiskQuotaUser-Objekt** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="34c29-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="34c29-157">Mit diesem Objekt kann ein Client die Einstellungen eines einzelnen Benutzers verwalten.</span><span class="sxs-lookup"><span data-stu-id="34c29-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="34c29-158">Es gibt mehrere Möglichkeiten, das **DIDiskQuotaUser-Objekt** eines Benutzers abzurufen:</span><span class="sxs-lookup"><span data-stu-id="34c29-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="34c29-159">Die **DIDiskQuotaUser-Objekte** für alle Benutzer mit Kontingenten auf dem Volume werden als Sammlung verfügbar gemacht und können aufzählt werden.</span><span class="sxs-lookup"><span data-stu-id="34c29-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="34c29-160">Eine Erläuterung zum Aufzählen von **DIDiskQuotaUser-Objekten** finden Sie unten.</span><span class="sxs-lookup"><span data-stu-id="34c29-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="34c29-161">Wenn Sie einen neuen Benutzer hinzufügen, gibt die [**AddUser-Methode**](diskquotacontrol-adduser.md) das **DIDiskQuotaUser-Objekt** des Benutzers zurück.</span><span class="sxs-lookup"><span data-stu-id="34c29-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="34c29-162">Wenn Sie über den Namen des Benutzers verfügen, gibt die [**FindUser-Methode**](diskquotacontrol-finduser.md) das **DIDiskQuotaUser-Objekt** des Benutzers zurück.</span><span class="sxs-lookup"><span data-stu-id="34c29-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="34c29-163">Aufzählen von Datenträgerkontingentbenutzern</span><span class="sxs-lookup"><span data-stu-id="34c29-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="34c29-164">Die **DIDiskQuotaUser-Objekte** für alle Benutzer mit einem Kontingent auf dem Volume werden als Sammlung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="34c29-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="34c29-165">Das [**DiskQuotaControl-Objekt**](diskquotacontrol-object.md) exportiert eine Standardenumeratormethode, mit der Sie die Auflistung von **DIDiskQuotaUser-Objekten** aufzählen können.</span><span class="sxs-lookup"><span data-stu-id="34c29-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="34c29-166">Im folgenden Verfahren wird veranschaulicht, wie die Enumeration mit Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="34c29-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="34c29-167">Sie können ein ähnliches Verfahren mit Visual Basic oder Microsoft Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="34c29-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="34c29-168">Erstellen Sie ein neues [**DiskQuotaControl-Objekt.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="34c29-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="34c29-169">Initialisieren Sie es mit [**Initialize**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="34c29-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="34c29-170">Erstellen Sie ein neues **JScript-Enumeratorobjekt.**</span><span class="sxs-lookup"><span data-stu-id="34c29-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="34c29-171">Verwenden  Sie eine for-Schleife, um die **DIDiskQuotaUser-Objekte zu** aufzählen.</span><span class="sxs-lookup"><span data-stu-id="34c29-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="34c29-172">Es ist nicht notwendig, einen Startwert festlegen.</span><span class="sxs-lookup"><span data-stu-id="34c29-172">There is no need to set a starting value.</span></span> <span data-ttu-id="34c29-173">Die **moveNext-Methode** des Enumeratorobjekts benachrichtigt die **Item-Methode,** um das nächste **DIDiskQuotaUser-Objekt zurück** zu geben.</span><span class="sxs-lookup"><span data-stu-id="34c29-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="34c29-174">Die **atEnd-Methode** gibt **FALSE zurück,** wenn Sie das Ende der Liste erreichen.</span><span class="sxs-lookup"><span data-stu-id="34c29-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="34c29-175">Verwenden Sie bei Bedarf das **DIDiskQuotaUser-Objekt,** das von der **Item-Methode** des Enumerators zurückgegeben wird, um mindestens eine der Datenträgerkontingenteigenschaften des zugeordneten Benutzers abzurufen oder zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="34c29-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="34c29-176">Das folgende Codefragment veranschaulicht, wie **DIDiskQuotaUser-Objekte** mit JScript aufzählt werden.</span><span class="sxs-lookup"><span data-stu-id="34c29-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="34c29-177">Das **Volume \_ Label-Argument,** das an die **EnumUsers-Funktion** übergeben wird, ist ein Zeichenfolgenwert, der eine Volumebezeichnung wie "C: \\ \\ " enthält.</span><span class="sxs-lookup"><span data-stu-id="34c29-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="34c29-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34c29-178">Requirements</span></span>



| <span data-ttu-id="34c29-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34c29-179">Requirement</span></span> | <span data-ttu-id="34c29-180">Wert</span><span class="sxs-lookup"><span data-stu-id="34c29-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c29-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34c29-181">Minimum supported client</span></span><br/> | <span data-ttu-id="34c29-182">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34c29-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34c29-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34c29-183">Minimum supported server</span></span><br/> | <span data-ttu-id="34c29-184">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34c29-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="34c29-185">DLL</span><span class="sxs-lookup"><span data-stu-id="34c29-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34c29-186"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="34c29-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c29-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34c29-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c29-188">**Shell-Objekt**</span><span class="sxs-lookup"><span data-stu-id="34c29-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




