---
description: Ermöglicht es einem Administrator, die Datenträgerkontingenteigenschaften eines Volumes zu verwalten.
title: DiskQuotaControl-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841551"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="30dae-103">DiskQuotaControl-Objekt</span><span class="sxs-lookup"><span data-stu-id="30dae-103">DiskQuotaControl object</span></span>

<span data-ttu-id="30dae-104">Ermöglicht es einem Administrator, die Datenträgerkontingenteigenschaften eines Volumes zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="30dae-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="30dae-105">Mit dem NTFS-Dateisystem kann ein Administrator die Datenträgernutzung auf einem freigegebenen Volume verwalten, indem jedem Benutzer eine bestimmte Menge an Speicherplatz oder eine Kontingentgrenze zuteil wird.</span><span class="sxs-lookup"><span data-stu-id="30dae-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="30dae-106">Mit diesem Objekt können Sie die Standardkontingentgrenze festlegen, die allen neuen Benutzern automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="30dae-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="30dae-107">Member</span><span class="sxs-lookup"><span data-stu-id="30dae-107">Members</span></span>

<span data-ttu-id="30dae-108">Das **DiskQuotaControl-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="30dae-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="30dae-109">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="30dae-109">Events</span></span>](#events)
-   [<span data-ttu-id="30dae-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="30dae-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="30dae-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30dae-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="30dae-112">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="30dae-112">Events</span></span>

<span data-ttu-id="30dae-113">Das **DiskQuotaControl-Objekt** verfügt über diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="30dae-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="30dae-114">Ereignis</span><span class="sxs-lookup"><span data-stu-id="30dae-114">Event</span></span>                                                           | <span data-ttu-id="30dae-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30dae-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30dae-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="30dae-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="30dae-117">Tritt ein, wenn die Namensinformationen für ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) aufgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="30dae-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="30dae-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="30dae-118">Methods</span></span>

<span data-ttu-id="30dae-119">Das **DiskQuotaControl-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="30dae-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="30dae-120">Methode</span><span class="sxs-lookup"><span data-stu-id="30dae-120">Method</span></span>                                                                                    | <span data-ttu-id="30dae-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30dae-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30dae-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="30dae-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="30dae-123">Weist einem neuen Benutzer ein nicht standardmäßiges Datenträgerkontingent zu.</span><span class="sxs-lookup"><span data-stu-id="30dae-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="30dae-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="30dae-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="30dae-125">Löscht einen Benutzer aus dem Volume.</span><span class="sxs-lookup"><span data-stu-id="30dae-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="30dae-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="30dae-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="30dae-127">Sucht den Eintrag eines Benutzers nach Namen in der Kontingentdatei des Volumes.</span><span class="sxs-lookup"><span data-stu-id="30dae-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="30dae-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="30dae-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="30dae-129">Platziert das angegebene Benutzerobjekt als Nächstes in der Zeile für die Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="30dae-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="30dae-130">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="30dae-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="30dae-131">Öffnet ein angegebenes Volume und initialisiert das Kontingentsteuerobjekt.</span><span class="sxs-lookup"><span data-stu-id="30dae-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="30dae-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="30dae-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="30dae-133">Erklärt den Benutzernamencache der Sicherheits-ID für ungültig.</span><span class="sxs-lookup"><span data-stu-id="30dae-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="30dae-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="30dae-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="30dae-135">Fährt den Thread für die Auflösung des Benutzernamens herunter.</span><span class="sxs-lookup"><span data-stu-id="30dae-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="30dae-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="30dae-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="30dae-137">Übersetzt einen Anmeldenamen in die entsprechende Benutzersicherheits-ID im Zeichenfolgenformat.</span><span class="sxs-lookup"><span data-stu-id="30dae-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="30dae-138">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30dae-138">Properties</span></span>

<span data-ttu-id="30dae-139">Das **DiskQuotaControl-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="30dae-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="30dae-140">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="30dae-140">Property</span></span>                                                                                   | <span data-ttu-id="30dae-141">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="30dae-141">Access type</span></span>           | <span data-ttu-id="30dae-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30dae-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30dae-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="30dae-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="30dae-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30dae-144">Read/write</span></span><br/> | <span data-ttu-id="30dae-145">Legt das Standardkontingentlimit fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="30dae-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="30dae-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="30dae-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="30dae-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30dae-147">Read-only</span></span><br/>  | <span data-ttu-id="30dae-148">Ruft die Standardkontingentgrenze als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="30dae-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="30dae-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="30dae-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="30dae-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30dae-150">Read/write</span></span><br/> | <span data-ttu-id="30dae-151">Legt den Standardkontingentschwellenwert fest oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="30dae-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="30dae-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="30dae-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="30dae-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30dae-153">Read-only</span></span><br/>  | <span data-ttu-id="30dae-154">Ruft den Standardkontingentschwellenwert als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="30dae-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="30dae-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="30dae-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="30dae-156">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30dae-156">Read/write</span></span><br/> | <span data-ttu-id="30dae-157">Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer sein zugewiesenes Kontingentlimit überschreitet.</span><span class="sxs-lookup"><span data-stu-id="30dae-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="30dae-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="30dae-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="30dae-159">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30dae-159">Read/write</span></span><br/> | <span data-ttu-id="30dae-160">Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingentschwellenwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="30dae-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="30dae-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="30dae-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="30dae-162">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30dae-162">Read-only</span></span><br/>  | <span data-ttu-id="30dae-163">Ruft einen booleschen Wert ab, der angibt, ob die Kontingentdatei für das Volume abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="30dae-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="30dae-164">**QuotaFileRe building**</span><span class="sxs-lookup"><span data-stu-id="30dae-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="30dae-165">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30dae-165">Read-only</span></span><br/>  | <span data-ttu-id="30dae-166">Ruft einen booleschen Wert ab, der angibt, ob die Kontingentdatei für das Volume gerade neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="30dae-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="30dae-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="30dae-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="30dae-168">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30dae-168">Read/write</span></span><br/> | <span data-ttu-id="30dae-169">Legt den Status der Datenträgerkontingente des Volumes fest oder ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="30dae-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="30dae-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="30dae-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="30dae-171">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30dae-171">Read/write</span></span><br/> | <span data-ttu-id="30dae-172">Legt einen Wert fest, der steuert, wie die Benutzer-SID in Benutzernamen aufgelöst wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="30dae-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="30dae-173">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30dae-173">Remarks</span></span>

<span data-ttu-id="30dae-174">Ein Administrator kann das **DiskQuotaControl-Objekt** verwenden, um eine Reihe von Aufgaben auszuführen, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="30dae-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="30dae-175">Aktivieren und Deaktivieren des Datenträgerkontingentsystems des Volumes.</span><span class="sxs-lookup"><span data-stu-id="30dae-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="30dae-176">Abrufen des Status des Kontingentsystems auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="30dae-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="30dae-177">Verweigern von Speicherplatz für Benutzer, die ihre Kontingentgrenze überschreiten.</span><span class="sxs-lookup"><span data-stu-id="30dae-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="30dae-178">Angeben der Standardwerte für Warnungsschwellenwert und Kontingentgrenzwert, die neuen Benutzern zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="30dae-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="30dae-179">Hinzufügen und Entfernen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="30dae-179">Adding and removing users.</span></span>

<span data-ttu-id="30dae-180">Mit **dem DiskQuotaControl-Objekt** können Sie globale Standardwerte für das Volume für Eigenschaften wie Kontingentgrenzen festlegen.</span><span class="sxs-lookup"><span data-stu-id="30dae-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="30dae-181">Jeder Benutzer wird jedoch durch ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) dargestellt, das zum Angeben einzelner Kontingenteinstellungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="30dae-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="30dae-182">Es gibt mehrere Möglichkeiten, das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) eines Benutzers zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="30dae-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="30dae-183">Die [**DIDiskQuotaUser-Objekte**](didiskquotauser-object.md) für alle Benutzer mit Kontingenten auf dem Volume werden als Sammlung verfügbar gemacht und können aufzählt werden.</span><span class="sxs-lookup"><span data-stu-id="30dae-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="30dae-184">Eine Erläuterung zum Aufzählen von **DIDiskQuotaUser-Objekten** finden Sie unter **Aufzählen** von Datenträgerkontingentbenutzern im Abschnitt "Hinweise" von **DIDiskQuotaUser**.</span><span class="sxs-lookup"><span data-stu-id="30dae-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="30dae-185">Wenn Sie einen neuen Benutzer hinzufügen, gibt die [**AddUser-Methode**](diskquotacontrol-adduser.md) das [**DIDiskQuotaUser-Objekt des Benutzers**](didiskquotauser-object.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="30dae-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="30dae-186">Wenn Sie über den Namen des Benutzers verfügen, gibt die [**FindUser-Methode**](diskquotacontrol-finduser.md) das [**DIDiskQuotaUser-Objekt des Benutzers**](didiskquotauser-object.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="30dae-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="30dae-187">Dieses Objekt macht die grundlegenden Funktionen der IDiskQuotaControl-Schnittstelle für Skripts und Microsoft Visual Basic-basierten Anwendungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30dae-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="30dae-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30dae-188">Requirements</span></span>



| <span data-ttu-id="30dae-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30dae-189">Requirement</span></span> | <span data-ttu-id="30dae-190">Wert</span><span class="sxs-lookup"><span data-stu-id="30dae-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30dae-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30dae-191">Minimum supported client</span></span><br/> | <span data-ttu-id="30dae-192">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30dae-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30dae-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30dae-193">Minimum supported server</span></span><br/> | <span data-ttu-id="30dae-194">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30dae-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="30dae-195">DLL</span><span class="sxs-lookup"><span data-stu-id="30dae-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30dae-196"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="30dae-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30dae-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30dae-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dae-198">**Shell-Objekt**</span><span class="sxs-lookup"><span data-stu-id="30dae-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




