---
title: Wiederherstellen gelöschter Objekte
description: Windows Server 2003 enthält die Datei \ 0034; gelöschte Objekte wiederherstellen \ 0034; befinden.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Wiederherstellen gelöschter Objekte AD
- Active Directory, verwenden, Wiederherstellen gelöschter Objekte
- Objekte AD, Wiederherstellen gelöschter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104516703"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="e19e5-106">Wiederherstellen gelöschter Objekte</span><span class="sxs-lookup"><span data-stu-id="e19e5-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="e19e5-107">Windows Server 2003 enthält das Feature "Gelöschte Objekte wiederherstellen".</span><span class="sxs-lookup"><span data-stu-id="e19e5-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="e19e5-108">Um die Wiederherstellung gelöschter Objekte zu aktivieren, muss mindestens ein Domänen Controller in der Domäne unter Windows Server 2003 oder einer höheren Version von Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="e19e5-109">Standardmäßig können nur Domänen Administratoren gelöschte Objekte wiederherstellen. Diese können jedoch an andere Personen delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="e19e5-110">Die folgenden Einschränkungen gelten für die Wiederherstellung von gelöschten Objekten:</span><span class="sxs-lookup"><span data-stu-id="e19e5-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="e19e5-111">Ein Objekt kann nicht wieder hergestellt werden, wenn die Tombstone-Lebensdauer für das Objekt abgelaufen ist, da das Objekt endgültig gelöscht wird, wenn die Tombstone-Lebensdauer abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="e19e5-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="e19e5-112">Objekte, die im Stamm des Namens Kontexts vorhanden sind, z. b. eine Domänen-oder Anwendungs Partition, können nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="e19e5-113">Schema Objekte können nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="e19e5-114">Schema Objekte sollten nie gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="e19e5-115">Es ist möglich, gelöschte Container wiederherzustellen, aber die Wiederherstellung der gelöschten Objekte, die sich vor dem Löschen im Container befanden, ist schwierig, da die Baumstruktur unter dem Container manuell rekonstruiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e19e5-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="e19e5-116">Erforderliche Berechtigungen zum Wiederherstellen eines gelöschten Objekts</span><span class="sxs-lookup"><span data-stu-id="e19e5-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="e19e5-117">Wenn ein Objekt gelöscht wird, wird die Objekt Sicherheits Beschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e19e5-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="e19e5-118">Obwohl der Besitzer von der Sicherheits Beschreibung identifiziert werden kann, können aus Sicherheitsgründen nur Domänen Administratoren gelöschte Objekte wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="e19e5-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="e19e5-119">Domänen Administratoren können die Berechtigung zum Wiederherstellen von Lösch Objekten für andere Benutzer und Gruppen erteilen, indem Sie dem Benutzer oder der Gruppe das Kontroll Zugriffsrecht für das reanimieren von Tombstones erteilen.</span><span class="sxs-lookup"><span data-stu-id="e19e5-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="e19e5-120">Das Kontroll Zugriffsrecht "reanimieren von Tombstones" wird im namens Kontext Stamm erteilt.</span><span class="sxs-lookup"><span data-stu-id="e19e5-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="e19e5-121">Nur Benutzer mit Lese Zugriffsberechtigung für ein Objekt und seine Attribute dürfen das Objekt und barrierefreie Attribute lesen, nachdem das Objekt gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="e19e5-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="e19e5-122">Das Erteilen eines Benutzers diese Berechtigung kann ein Sicherheitsrisiko darstellen, da der Benutzer ein Konto Objekt wiederherstellen kann, das Zugriff auf Ressourcen hat, auf die der Benutzer normalerweise keinen Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="e19e5-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="e19e5-123">Durch die Wiederherstellung eines Kontos erhält der Benutzer im Wesentlichen die Kontrolle über dieses Konto, da der Benutzer das anfängliche Kennwort für das Konto festlegen muss, wenn das Konto wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e19e5-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="e19e5-124">Zum vollständigen Wiederherstellen eines gelöschten Objekts muss der Benutzer folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="e19e5-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="e19e5-125">Sie haben oder sind Mitglied einer Gruppe, die über das Steuerelement Zugriffsrecht zum reanimieren von Tombstones verfügt.</span><span class="sxs-lookup"><span data-stu-id="e19e5-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="e19e5-126">Sie haben Schreibzugriff auf jedes obligatorische Attribut, das aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e19e5-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="e19e5-127">Sie haben Schreibzugriff auf den relativen Distinguished Name (RDN).</span><span class="sxs-lookup"><span data-stu-id="e19e5-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="e19e5-128">Sie haben Schreibzugriff auf jedes optionale Attribut, das aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e19e5-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="e19e5-129">Übergeordnete Erstellungs Rechte für den Zielcontainer für die Objektklasse des wiederhergestellten Objekts verfügen.</span><span class="sxs-lookup"><span data-stu-id="e19e5-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="e19e5-130">Das **isDeleted** -Attribut wird während des Wiederherstellungs Vorgangs nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="e19e5-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="e19e5-131">Weder die Delete-Child-Berechtigung für den Container "Deleted Objects" wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="e19e5-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="e19e5-132">Wiederherstellen eines gelöschten Objekts</span><span class="sxs-lookup"><span data-stu-id="e19e5-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="e19e5-133">Zum Wiederherstellen eines gelöschten Objekts muss sich das Objekt zuerst im Container Gelöschte Objekte befinden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="e19e5-134">Weitere Informationen zum Abrufen von gelöschten Objekten finden Sie unter [Abrufen gelöschter Objekte](retrieving-deleted-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e19e5-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="e19e5-135">Wenn das Objekt gefunden wurde, müssen die folgenden Vorgänge in einem einzelnen LDAP-Vorgang abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="e19e5-136">Dies erfordert die Verwendung der LDAP-Funktion zum [**\_ Ändern von Ext- \_ \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) mit dem [**LDAP-Server " \_ \_ \_ gelöschtes \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) -Steuerelement anzeigen"</span><span class="sxs-lookup"><span data-stu-id="e19e5-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="e19e5-137">Entfernen Sie den Wert des **isDeleted** -Attributs.</span><span class="sxs-lookup"><span data-stu-id="e19e5-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="e19e5-138">Der Wert des **isDeleted** -Attributs muss entfernt und nicht auf " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="e19e5-139">Ersetzen Sie den Distinguished Name des Objekts, sodass er in einen anderen als den Container für gelöschte Objekte verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e19e5-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="e19e5-140">Dies kann ein beliebiger Container sein, der normalerweise das-Objekt enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e19e5-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="e19e5-141">Der Distinguished Name des vorherigen Containers des-Objekts befindet sich im **lastKnownParent** -Attribut des gelöschten Objekts.</span><span class="sxs-lookup"><span data-stu-id="e19e5-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="e19e5-142">Das **lastKnownParent** -Attribut wird nur festgelegt, wenn das Objekt auf einem Windows Server 2003-Domänen Controller gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="e19e5-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="e19e5-143">Daher ist es möglich, dass der Inhalt des **lastKnownParent** -Attributs ungenau ist.</span><span class="sxs-lookup"><span data-stu-id="e19e5-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="e19e5-144">Stellen Sie die obligatorischen Attribute für das Objekt wieder her, die während des Löschvorgangs gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="e19e5-145">Das **objectCategory** -Attribut kann auch festgelegt werden, wenn das Objekt wieder hergestellt wird, jedoch nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e19e5-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="e19e5-146">Wenn kein **objectCategory** -Wert angegeben wird, wird die Standard- **objectCategory** für die **objectClass** des Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="e19e5-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="e19e5-147">Nachdem das Objekt wieder hergestellt wurde, kann es wie vor dem Löschen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="e19e5-148">An diesem Punkt sollten alle optionalen Attribute, die wichtig sind, wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="e19e5-149">Alle Verweise auf das Objekt aus anderen Objekten im Verzeichnis müssen ebenfalls wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="e19e5-150">Als Sicherheitsmaßnahme werden Benutzer Objekte deaktiviert, wenn Sie wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e19e5-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="e19e5-151">Benutzer Objekte müssen aktiviert werden, nachdem die optionalen Attribute wieder hergestellt wurden, damit das Benutzerobjekt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e19e5-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="e19e5-152">Weitere Informationen und ein Codebeispiel, das zeigt, wie ein gelöschtes Objekt wieder hergestellt wird, finden Sie unten in der Funktion restoredeletedobject.</span><span class="sxs-lookup"><span data-stu-id="e19e5-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="e19e5-153">Restoredeletedobject</span><span class="sxs-lookup"><span data-stu-id="e19e5-153">RestoreDeletedObject</span></span>

<span data-ttu-id="e19e5-154">Im folgenden C++-Codebeispiel wird gezeigt, wie ein gelöschtes Objekt wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e19e5-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 